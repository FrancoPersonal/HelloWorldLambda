# Hello World c# Serverless

## Prerequisitos

- [Permisos](policies.md)
- [dependencias](aws-dependences_windows.md)



El siguiente curso introductorio esta basado en el ejemplo de serverless de aws

https://serverless.com/framework/docs/providers/aws/examples/hello-world/csharp/

## Procemiento

1. Crear la carpeta serverlesssample con el comando:

 ```bat
md serverlesssample
cd serverlesssample
```

2. Generar el ejemplo basado en el template con el comando: 

 ```bat
sls create --template aws-csharp --path helloServerless

```
3. Ingresar en la carpeta creada y compilar la lanbda
 ```bat
 cd helloServerless
build
```

3. desplegar la lambda
 ```bat
sls deploy --env dev --verbose

```

4. probar que la lambda esta corriendo correctamente

 ```bat
sls invoke -f hello
```

5. se mostrara el siguiente mensaje:

 ```json
{
    "Message": "Go Serverless v1.0! Your function executed successfully!",
    "Request": {
        "Key1": null,
        "Key2": null,
        "Key3": null
    }
}
```

cual es la magia:

 ```yml

service: helloserverless #Nombre del stack

provider:
  name: aws              #en donde se despliega el serverless
  runtime: dotnetcore2.1 #el codigo en que sera desplegado

package:
  individually: true     #indica si el paquete sera generico para todas las funciones o uno por funcion

functions:
  hello:    # nombre de la funcion
    handler: CsharpHandlers::AwsDotnetCsharp.Handler::Hello  #nombre del ensamblado::namespace.clase::metodo 
    package:
      artifact: bin/release/netcoreapp2.1/hello.zip #nombre del zip que se genero la funcion

```
# Prerrequisitos

## Software necesario 

### [Visual studio code](https://code.visualstudio.com/download#)

1. descargarlo de la ruta: https://code.visualstudio.com/docs/?dv=win64user
2. Instalarlo con las opciones por default

### [Node js](https://nodejs.org/en/download/)

1. verificar que no lo tienen instalado. En una consola teclear la siguiente instrucccion:

```bash
node --version
```

2. Si no aparece nada descargarlo de la ruta [https://nodejs.org/dist/v12.13.0/node-v12.13.0-x64.msi](https://nodejs.org/dist/v12.13.0/node-v12.13.0-x64.msi)

3. Instalarlo con las opciones por default

### [Serverless](https://serverless.com/framework/docs/providers/aws/guide/installation/)

1. En una consola ejecutar el siguiente comando:

 ```bash
npm install -g serverless
```
2. Verificar que se ha instalado correctamente:
 ```bash
serverless --version
```

### [awscli](https://docs.aws.amazon.com/es_es/cli/latest/userguide/install-windows.html)


1. descargar el cliente de la ruta https://s3.amazonaws.com/aws-cli/AWSCLI64PY3.msi
2. instalar con los valores default 
3. comprobar que se instalo correctamente con el commando

 ```bash
aws --version
```
4. Ingresar tus credenciales del archivo generado al crear el usuario[(Ver la seccion de permios)](policies.md) para la region us-east-1 con el commando:

 ```bash
aws configure 
```







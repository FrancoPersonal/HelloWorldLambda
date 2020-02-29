# Permisos

Para el curso se requiere crear un perfil de usuario el cual nos servira para poder desplegar la lambda


1. Entrar en la [consola de administracion de aws](https://console.aws.amazon.com/?nc2=h_m_mc) e ingresar con sus credenciales
2. Ingresar al modulo de [IAM](https://console.aws.amazon.com/iam/home?#/home)
3. Crear un grupo en Grupos / crear grupo con el nombre de **LambdaDeployGroup**
4. En las politicas seleccionar los roles:
- **AWSLambdaFullAccess** 
- **IAMFullAccess**
- **AmazonS3FullAccess**
- **CloudWatchLogsFullAccess**
- **AWSCodeDeployRoleForLambda** 
- **AWSCloudFormationFullAccess**
 
5. Crear unusuario seleccionando Usuarios / añadir usuario(s) **LambdaDeployUser** seleccionando acceso mediante programacion y seleccionar el grupo **LambdaDeployGroup**
6. cuando se cree el usuario oprimir el boton descargar .csv












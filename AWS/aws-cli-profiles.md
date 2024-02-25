# PERFILES DE AWS CLI

La AWS Command Line Interface (CLI) permite administrar servicios de AWS y recursos. Usando perfiles, puedes gestionar fácilmente múltiples cuentas de AWS desde la línea de comandos.

## Prerrequisitos

- Tener AWS CLI instalado.
- Acceso a las credenciales de AWS (Access Key ID y Secret Access Key).

## Configuración de Perfiles en AWS CLI

### 1. Configuración Inicial

Para configurar tu primer perfil, ejecuta:

```bash
aws configure
```


Ingresa los detalles solicitados:
- AWS Access Key ID
- AWS Secret Access Key
- Default region name
- Default output format

Esto configura el perfil predeterminado.

### 2. Crear Perfiles Adicionales
Para crear un perfil adicional, usa:

```bash
aws configure --profile nombre_del_perfil
```


### 3. Listar Perfiles Configurados

```bash
cat ~/.aws/config
cat ~/.aws/credentials
```
### 4. Usar un Perfil Específico
Para usar un perfil en un comando específico, usa la opción --profile:

```bash
aws s3 ls --profile nombre_del_perfil
```

5. Cambiar el Perfil Predeterminado
Si deseas cambiar el perfil predeterminado para la sesión actual, puedes exportar la variable de entorno AWS_PROFILE:

```bash
export AWS_PROFILE=nombre_del_perfil
```
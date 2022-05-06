# SQL

Práctica de introducción a sql con Postgresql

Launch X Mission NodeJs

## Pasos

### Instalar Postgresql

El motor de base de datos de Postgresql se descarga desde el siguiente sitio oficial de [postgres](https://www.postgresql.org/download). Seleccioanar el binario correspondiente al sistema operativo y arquitectura que posees.

### Iniciar sesión
![login](/images/login.PNG)

### Mostrar bases de datos disponibles
![Bases Datos](/images/ListadoBaseDatos.PNG)

### Crear base de datos launchx_nodejs
![Crear base datos launchx_nodejs](/images/CreacionBaseDatos.PNG)

### Seleccionar como base de datos de trabajo a la nueva base de datos creada
![Seleccionar launchx_nodejs](/images/ConexionNuevaBaseDatos.PNG)

### Crear una nueva tabla explorers
![Crear nueva tabla explorers](/images/CrearTabla.PNG)

### Agregar registros a la tabla explorers
![Insertar registros en la tabla explorers](/images/InsertarDatosTabla.PNG)

### Seleccionar todos los registros
![Seleccionar todos los registros](/images/SeleccionarDatosInsertados.PNG)

### Seleccionar los nombres de los explorers
![Seleccionar nombres de los exploeres](/images/SeleccionarNombresInsertados.PNG)

### Actualizar el nombre de los exploeres cuando su id sea 1
![Actulizar nombre explorers](/images/ActualizarNombre.PNG)

### Eliminar los explorers con id igual a 1
![Eliminar explorers](/images/EliminarRegistro.PNG)

## Resumen

```mermaid
stateDiagram-v2
state "Instalar postgress" as InstalarPostgres
state "Iniciar sesion" as IniciarSesion
state "Crear base de datos launchx_nodejs" as CrearBaseDatos
state "Establecer launchx_nodejs como base datos actual"  as EstablecerBaseDatos
state "Crear tabla explorers" as CrearTabla
state "Insertar registros en la nueva tabla" as InsertarRegistros
state "Seleccionar todos los registros" as SeleccionarRegistros
state "Seleccionar los nombres de los explorers" as SeleccionarNombres
state "Actualizar nombre de las explorers que tengan id = 1" as ActualizarNombre
state "Eliminar explorers con id = 1" as EliminarExplorers

InstalarPostgres --> IniciarSesion
IniciarSesion --> CrearBaseDatos
CrearBaseDatos --> EstablecerBaseDatos
EstablecerBaseDatos --> CrearTabla
CrearTabla --> InsertarRegistros
InsertarRegistros --> SeleccionarRegistros
SeleccionarRegistros --> SeleccionarNombres
SeleccionarNombres --> ActualizarNombre
ActualizarNombre --> EliminarExplorers


```
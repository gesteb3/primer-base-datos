# Creando una base de datos en PostgreSQL usando Docker y DataGrip
## Ejecutando Docker con PostgreSQL

### Para iniciar un contenedor de PostgreSQL usando Docker:
##### docker run --name postgres-db -e POSTGRES_PASSWORD=yourpassword -p 5432:5432 -d postgres
#### docker ps
- Para verificar si está activo
####Funciones:                  
- docker run: Ejecuta un nuevo contenedor.
- --name postgres-db: Asigna el nombre postgres-db al contenedor.
- -e POSTGRES_PASSWORD=yourpassword: Define la contraseña del usuario postgres.
- -p 5432:5432: Mapea el puerto 5432 del contenedor al puerto 5432 del host.
- -d: Ejecuta el contenedor en segundo plano (modo "detached").
- postgres :	Imagen oficial de PostgreSQL desde Docker Hub.

### 🛠️Pasos para configurar DataGrip
- Abrir DataGrip.

- Haz clic en + (Add) en el panel izquierdo > Data Source > PostgreSQL.

- Completa los campos de conexión:

#### Host	--> localhost
#### Port	--> 5432
#### User	--> postgres
#### Password --> 	yourpassword
#### Database--> postgres

Haz clic en Test Connection  para verificar la conexi{on Entre el contenedor de docker y Data.
Si es necesario, permite la descarga de los drivers.
Finalmente, haz clic en OK.

### 🛠️ Creación de la base de datos PostgreSQL desde DataGrip

- Haz clic derecho sobre postgres (la base de datos predeterminada).

- Selecciona: New > Database.

- Escribe el nombre de la nueva base de datos (por ejemplo: mibase o BaseDatos).

- Haz clic en OK.
- Abre una nueva **Consola SQL** conectada al servidor PostgreSQL.
- Ejecuta el siguiente comando SQL para crear tu base de datos:

```sql
CREATE DATABASE nombre_de_tu_base_de_datos;

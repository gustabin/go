```markdown
# Sistema de Gestión de Empleados en Go

Este proyecto es un sistema de gestión de empleados desarrollado en Go. Permite realizar operaciones básicas de CRUD (Crear, Leer, Actualizar y Borrar) sobre una base de datos MySQL. Utiliza el paquete `net/http` para manejar solicitudes HTTP y el paquete `text/template` para renderizar plantillas HTML.

## Estructura del Proyecto

- `main.go`: El archivo principal que contiene el código del servidor.
- `go.mod`: Archivo de módulos de Go que define las dependencias del proyecto.
- `go.sum`: Archivo que contiene las sumas de verificación de las dependencias del proyecto.
- `plantillas/`: Directorio que contiene las plantillas HTML.

## Instalación y Configuración

### Requisitos

- Go 1.22.5 o superior
- MySQL

### Configuración de la Base de Datos

Crea una base de datos MySQL llamada `go` y una tabla `empleados` con la siguiente estructura:

```sql
CREATE DATABASE go;
USE go;

CREATE TABLE empleados (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(255) NOT NULL,
    correo VARCHAR(255) NOT NULL
);
```

### Clonar el Repositorio

```bash
git clone https://github.com/tu_usuario/go_sistema.git
cd go_sistema
```

### Instalar Dependencias

```bash
go mod tidy
```

## Ejecución

Para ejecutar el servidor, usa el siguiente comando:

```bash
go run main.go
```

El servidor se ejecutará en `http://localhost:8080`.

## Funcionalidades

### Rutas

- `/`: Muestra la lista de empleados.
- `/crear`: Muestra un formulario para crear un nuevo empleado.
- `/insertar`: Inserta un nuevo empleado en la base de datos (maneja solicitudes POST).
- `/borrar`: Elimina un empleado de la base de datos basado en su ID.
- `/editar`: Muestra un formulario para editar un empleado existente.
- `/actualizar`: Actualiza los datos de un empleado en la base de datos (maneja solicitudes POST).

### Plantillas

- `cabecera.html`: Contiene la cabecera común para todas las páginas.
- `pie.html`: Contiene el pie de página común para todas las páginas.
- `inicio.html`: Plantilla para la página principal que muestra la lista de empleados.
- `crear.html`: Plantilla para la página de creación de empleados.
- `editar.html`: Plantilla para la página de edición de empleados.

## Contribuciones

Las contribuciones son bienvenidas. Para contribuir, sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza los cambios necesarios y haz commits (`git commit -am 'Agregar nueva funcionalidad'`).
4. Envía los cambios a tu fork (`git push origin feature/nueva-funcionalidad`).
5. Abre un Pull Request en GitHub.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más información.
```

Este archivo `README.md` proporciona una descripción general del proyecto, instrucciones de configuración y ejecución, y detalles sobre las funcionalidades del sistema. También incluye una sección sobre cómo contribuir al proyecto.

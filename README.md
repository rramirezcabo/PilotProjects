# PilotProjects

Portal de visores HTML de proyectos, publicado en Azure Static Web Apps.

## Estructura

```
index.html                  Portal con la lista de proyectos
staticwebapp.config.json    Login obligatorio y acceso por rol
sin-acceso.html             Página para usuarios sin permiso
<proyecto>/<entregable>/    Un visor por carpeta (index.html)
```

## Proyectos

| Carpeta | Contenido | Rol requerido |
|---|---|---|
| `costa-palmas/geotecnia/` | Información Geotécnica Costa Palmas | `costa-palmas` o `admin` |

## Agregar un proyecto

1. Crear la carpeta `<proyecto>/<entregable>/index.html` (minúsculas, sin acentos ni espacios).
2. Agregar la regla de la carpeta en `staticwebapp.config.json` **antes** de la regla `/*`.
3. Agregar la tarjeta en `index.html` y la fila en este README.
4. Invitar usuarios con el rol del proyecto en Azure → Static Web App → Role management.

## Acceso

- Inicio de sesión con cuenta Microsoft (los usuarios con Gmail crean una cuenta Microsoft gratuita con su mismo correo).
- Cada usuario recibe solo el rol de su proyecto; `admin` ve todo.

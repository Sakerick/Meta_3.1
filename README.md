📝 API de Gestión de Tareas (Task Manager)
Una API RESTful sencilla construida con Node.js y Express siguiendo el patrón de diseño MVC (Modelo-Vista-Controlador). 
Este proyecto permite gestionar una lista de tareas almacenadas en memoria, ofreciendo funcionalidades de búsqueda y diferentes formatos de respuesta.

🚀 Requisitos Previos
Node.js (v14 o superior recomendado)npm (instalado junto con Node.js)🛠️ InstalaciónClona este repositorio o descarga los archivos.
Abre una terminal en la carpeta raíz del proyecto.Instala las dependencias necesarias:Bashnpm install

🏃 Ejecución
Para iniciar el servidor en modo de desarrollo (utilizando nodemon si lo tienes configurado o node por defecto):Bashnpm run dev
El servidor se ejecutará normalmente en: http://localhost:3000📑 Endpoints de la API
La base de todos los endpoints es /api/tareas.

🔍 Consultas (GET)EndpointDescripciónParámetros Opcionales

GET /api/tareas

Obtiene todas las tareas

titulo: Filtra por coincidencia de texto.formato: json (default) o text.

GET /api/tareas/:idObtiene una tarea específica por su ID numérico-

Ejemplos de búsqueda:

GET /api/tareas?titulo=Express (Busca tareas que contengan "Express")
GET /api/tareas?formato=text (Devuelve la lista en texto plano)

✍️ Modificaciones (POST, PUT, PATCH, DELETE)

MétodoEndpointCuerpo (JSON)DescripciónPOST/api/tareas{"titulo": "Nueva Tarea"}

Crea una tarea.PUT/api/tareas/:id{"titulo": "Update", "completada": true}

Actualización total.PATCH/api/tareas/:id{"completada": true}
Actualización parcial.

DELETE/api/tareas/:id
  -Elimina una tarea por ID.

📂 Estructura del Proyecto

src/routes/: Definición de rutas y endpoints
.src/controllers/:  Lógica de manejo de peticiones y respuestas 
HTTP.src/models/: Gestión de datos y lógica de negocio (Base de datos en memoria).

<img width="1278" height="457" alt="Screenshot from 2026-03-12 12-04-45" src="https://github.com/user-attachments/assets/dbacb339-9fdb-4a5e-bb32-7bfc2b044dcb" />
<img width="1278" height="457" alt="Screenshot from 2026-03-12 12-03-44" src="https://github.com/user-attachments/assets/b73f7ae6-8e1d-4203-bc2b-d699f2d7862a" />
<img width="1278" height="457" alt="Screenshot from 2026-03-12 12-03-02" src="https://github.com/user-attachments/assets/5624c557-145f-45e2-9c11-2de6055da062" />
<img width="1278" height="457" alt="Screenshot from 2026-03-12 12-02-48" src="https://github.com/user-attachments/assets/d2fff16e-3af3-49b6-adbe-71f136054f2c" />

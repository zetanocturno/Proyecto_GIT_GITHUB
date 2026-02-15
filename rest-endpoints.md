\# Diseño de Endpoints REST - API de Sistema de Gestión



\## Descripción General

API RESTful para un sistema de gestión de usuarios y recursos.



\## Endpoints Principales



\### Usuarios

\- `GET /api/v1/usuarios` - Listar todos los usuarios

\- `GET /api/v1/usuarios/{id}` - Obtener usuario específico

\- `POST /api/v1/usuarios` - Crear nuevo usuario

\- `PUT /api/v1/usuarios/{id}` - Actualizar usuario

\- `DELETE /api/v1/usuarios/{id}` - Eliminar usuario



\### Productos

\- `GET /api/v1/productos` - Listar productos

\- `GET /api/v1/productos/{id}` - Obtener producto

\- `POST /api/v1/productos` - Crear producto

\- `PUT /api/v1/productos/{id}` - Actualizar producto

\- `DELETE /api/v1/productos/{id}` - Eliminar producto



\### Pedidos

\- `GET /api/v1/pedidos` - Listar pedidos

\- `GET /api/v1/pedidos/{id}` - Obtener pedido

\- `POST /api/v1/pedidos` - Crear pedido

\- `PUT /api/v1/pedidos/{id}/estado` - Actualizar estado del pedido



\## Códigos de Respuesta

\- 200: Éxito

\- 201: Recurso creado

\- 400: Error de cliente

\- 401: No autorizado

\- 404: Recurso no encontrado

\- 500: Error del servidor


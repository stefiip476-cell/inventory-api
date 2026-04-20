API de Inventario Tecnológico
Descripción

Esta API permite gestionar dispositivos tecnológicos como laptops, routers y otros equipos. Permite registrar, visualizar, actualizar y eliminar dispositivos, además de generar un conteo por tipo.

Tecnologías
Python
FastAPI
Uvicorn
Instalación
pip install -r requirements.txt
Ejecución
uvicorn main:app --reload
Endpoints
GET / → Verifica que la API está activa
GET /devices → Lista todos los dispositivos
POST /devices → Agrega un dispositivo
PUT /devices/{id} → Actualiza el estado
DELETE /devices/{id} → Elimina un dispositivo
GET /devices/count → Conteo por tipo
Evidencia

Se incluyen capturas de la API funcionando en Swagger:
http://127.0.0.1:8000/docs

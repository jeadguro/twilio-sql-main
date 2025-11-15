# 📲 Sistema de Envío Masivo de WhatsApp con Twilio + FastAPI + PostgreSQL

Este proyecto permite cargar un archivo Excel con datos de clientes y
enviar mensajes personalizados de WhatsApp utilizando **Twilio**, con
backend en **FastAPI** y almacenamiento en **PostgreSQL**.\
Incluye vista previa, barra de progreso en tiempo real y simulación de
envío para pruebas.

------------------------------------------------------------------------

## 🚀 Características principales

-   Carga de archivos Excel desde una interfaz web.
-   Vista previa de los registros antes de enviar mensajes.
-   Envío masivo de WhatsApp con Twilio (o modo simulación).
-   API construida con FastAPI.
-   Base de datos PostgreSQL para guardar clientes, autos y servicios.
-   Barra de progreso en tiempo real.
-   Sanitización de datos y validaciones.
-   Uso de `.env` para credenciales sensibles.

------------------------------------------------------------------------

## 📦 Requisitos

### **Backend**

-   Python 3.10+
-   FastAPI
-   Uvicorn
-   SQLAlchemy
-   Psycopg2
-   Pandas
-   python-dotenv
-   Twilio SDK

### **Base de datos**

-   PostgreSQL 14+

### **Frontend**

-   Navegador web (HTML + JS)

------------------------------------------------------------------------

## 🔧 Instalación del entorno

### **1️⃣ Crear y activar entorno virtual**

``` bash
python -m venv venv
```

**Windows**

``` bash
venv\Scripts\activate
```

**Linux/Mac**

``` bash
source venv/bin/activate
```

### **2️⃣ Instalar dependencias**

``` bash
pip install -r requirements.txt
```

------------------------------------------------------------------------

## 🔐 Archivo `.env`

Crea el archivo:

    twilio.env

Contenido:

    TWILIO_ACCOUNT_SID=xxxxxxxxxxxxxxxx
    TWILIO_AUTH_TOKEN=xxxxxxxxxxxxxxxx
    TWILIO_PHONE_NUMBER=whatsapp:+14155238886
    SIMULATE_TWILIO=true

> Si `SIMULATE_TWILIO=true`, no se envía ningún mensaje real.

------------------------------------------------------------------------

## 🗄 Configuración de PostgreSQL

Crear base de datos:

``` sql
CREATE DATABASE taller;
```

Variables configuradas en `database.py`.

------------------------------------------------------------------------

## ▶️ Ejecutar FastAPI

``` bash
uvicorn main:app --reload
```

La API inicia en:

    http://127.0.0.1:8000

Documentación automática:

    http://127.0.0.1:8000/docs

------------------------------------------------------------------------

## 🌐 Frontend (HTML)

El archivo `index.html` permite:

-   Subir archivo Excel
-   Mostrar vista previa
-   Iniciar envíos
-   Mostrar progreso en tiempo real

Endpoints utilizados:

-   `POST /upload-excel/`
-   `POST /send-messages/`
-   `GET /progress/`

------------------------------------------------------------------------

## 📁 Estructura del Proyecto

    twilio-sql/
    │── main.py
    │── models.py
    │── crud.py
    │── database.py
    │── requirements.txt
    │── index.html
    │── twilio.env
    │── README.md

------------------------------------------------------------------------

## 📬 Endpoints de la API

### **1. Cargar Excel**

`POST /upload-excel/`

### **2. Enviar mensajes**

`POST /send-messages/`

### **3. Progreso**

`GET /progress/`

------------------------------------------------------------------------

## 💬 Mensaje enviado

Ejemplo:

    👋 Hola {nombre},
    Le recordamos que ya corresponde el servicio/revisión de su {vehiculo}. 🚗

    Por favor comuníquese con nosotros para agendar su cita. ✅

------------------------------------------------------------------------

## 🧪 Modo Simulación

Activa:

    SIMULATE_TWILIO=true

En consola verás:

    📢 Simulación: whatsapp:+521XXXXXXXXXX → Hola Juan...

------------------------------------------------------------------------

## 🛠 Autor

**Adrián Rocha**\
Proyecto para automatizar recordatorios de servicio automotriz.

------------------------------------------------------------------------

¡Listo! Tu proyecto queda documentado profesionalmente 🔥
=======
# twilio-sql-main
Automatiza el envío de WhatsApp a tus clientes con Twilio. Carga Excel, envía recordatorios de servicio, monitorea progreso en tiempo real y gestiona datos en PostgreSQL. Configuración fácil vía .env.
>>>>>>> d343aaae31d6f933f46ca67d83d17b8b48197da4

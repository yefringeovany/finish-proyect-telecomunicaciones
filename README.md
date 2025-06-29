# 🌱 Sistema IoT de Monitoreo de Temperatura para Control de Riego

Este proyecto tiene como objetivo aplicar tecnologías IoT para resolver una problemática real del sector agrícola: el uso eficiente del agua en sistemas de riego. 

El sistema permite monitorear la temperatura y humedad en tiempo real, activando automáticamente una bomba de agua cuando las condiciones ambientales lo requieren. También se ofrece control manual a través de una aplicación conectada a internet.

---

## 🚀 Descripción General

El sistema de riego automatizado con monitoreo ambiental está diseñado para pequeños cultivos, permitiendo un uso responsable del recurso hídrico. Usa sensores para capturar información, dispositivos para automatizar acciones, y tecnologías modernas para ofrecer control remoto y análisis de datos.

### 🎯 Objetivo del Proyecto
Desarrollar una solución IoT que:

- Monitoree la temperatura y humedad del entorno agrícola.
- Active automáticamente una bomba de riego si la temperatura supera un umbral definido.
- Permita el control remoto de la bomba mediante una aplicación web.
- Notifique eventos importantes mediante mensajes al servidor MQTT.

---

## ⚙️ Tecnologías y Herramientas Utilizadas

### 🔌 Hardware

- **ESP32**: Módulo principal para conectividad WiFi y lectura del sensor DHT22.
- **Arduino Uno**: Controla el relé y la activación física de la bomba de agua.
- **Sensor DHT22**: Detecta temperatura y humedad del ambiente.
- **Relé de 5V**: Controla el encendido/apagado de la bomba.
- **Mini Bomba de Agua**: Ejecuta el riego del cultivo.
- **Protoboard, cables y batería portátil**: Infraestructura básica del sistema.

### 💻 Software

- **Arduino IDE**: Programación del Arduino Uno y ESP32.
- **Node.js**: Backend que maneja la lógica del sistema y conexión con Firebase.
- **PM2**: Para mantener el servidor Node.js activo en producción.
- **React.js**: Interfaz web para el control manual de la bomba y visualización de datos.
- **Firebase**: Almacenamiento de datos de sensores y estado del sistema.
- **Broker MQTT (broker.emqx.io)**: Comunicación en tiempo real entre dispositivos y el servidor.
- **Render**: Despliegue del frontend y backend del sistema web.

### Figura 1:
![Image](https://github.com/user-attachments/assets/69bc890b-7c9d-4081-85ca-8fc044ed4fde)

## 🔧 Instalación del Backend (Node.js + MQTT + Firebase)

### 1. Clona el repositorio

Abre tu terminal y ejecuta los siguientes comandos:

```bash
git clone [https://github.com/usuario/proyecto-riego-iot.git](https://github.com/yefringeovany/finish-proyect-telecomunicaciones.git)
cd (name-proyect)
```
### Instalacion de Dependencias
```bash
npm install
```

### Variables de entorno (.env)
```bash
MQTT_BROKER=mqtt://broker.emqx.io
MQTT_TOPIC_SENSOR=sensor/temperatura
MQTT_TOPIC_HUMEDAD=sensor/humedad
MQTT_TOPIC_CONTROL=bomba/control
MQTT_TOPIC_STATUS=bomba/status

FIREBASE_API_KEY=tu_api_key
FIREBASE_AUTH_DOMAIN=tu_auth_domain
FIREBASE_DATABASE_URL=tu_database_url
FIREBASE_PROJECT_ID=tu_project_id
FIREBASE_STORAGE_BUCKET=tu_storage_bucket
FIREBASE_MESSAGING_SENDER_ID=tu_sender_id
FIREBASE_APP_ID=tu_app_id

```
### Ejecutar el servidor de desarrollo
```bash
node index.js
```

### Iniciar PM2 
```bash
npm install -g pm2
pm2 start index.js
```








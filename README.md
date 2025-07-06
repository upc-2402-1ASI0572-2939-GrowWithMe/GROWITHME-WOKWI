# 🌱 Sistema IoT para Monitoreo de Cultivos con ESP32, DHT22 y LCD

Este proyecto implementa un sistema de monitoreo ambiental para cultivos utilizando un **ESP32**, un sensor **DHT22**, una pantalla **LCD I2C**, y conexión Wi-Fi. El sistema mide **temperatura** y **humedad**, muestra los valores en una LCD y los envía a un servidor mediante peticiones HTTP. Además, activa una alerta visual con un **LED** si las lecturas están fuera de los rangos definidos para la planta monitoreada.

## 🔧 Componentes utilizados

- ESP32
- Sensor DHT22 (Temperatura y Humedad)
- Pantalla LCD I2C (16x2)
- LED de alerta
- Conexión WiFi a `Wokwi-GUEST`
- API REST en Azure (simulación en Wokwi)

## 📡 Funcionalidades

- 📶 Conexión a red WiFi (Wokwi-GUEST)
- 🌡 Lectura de temperatura y humedad con DHT22
- 📺 Visualización de datos en pantalla LCD
- ☁️ Comunicación con API REST:
  - Obtener información del dispositivo y planta.
  - Enviar temperatura y humedad actual.
- 🚨 Alerta en LCD y encendido de LED cuando:
  - La temperatura está fuera del rango permitido.
  - La humedad está fuera del rango permitido.

## 🌐 Endpoints utilizados

```http
GET  /api/v1/iot-service/devices/{deviceId}
GET  /api/v1/iot-service/plants/{plantId}
PATCH /api/v1/iot-service/devices/patch/temperature/{deviceId}/{temp}
PATCH /api/v1/iot-service/devices/patch/humidity/{deviceId}/{hum}

URL: https://wokwi.com/projects/435721151320217601

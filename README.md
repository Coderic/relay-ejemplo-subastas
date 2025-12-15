# 🔨 Sistema de Subastas en Tiempo Real - React + Relay Gateway

Sistema de subastas estilo eBay/MercadoLibre construido con **React** y **[Relay Gateway](https://github.com/Coderic/Relay)**.

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)
![Vite](https://img.shields.io/badge/Vite-5-646CFF?logo=vite)
![Relay](https://img.shields.io/badge/Relay-Gateway-blueviolet)

## 📖 Sobre este Ejemplo

Este ejemplo funcional demuestra cómo construir un sistema de subastas en tiempo real, similar a plataformas como eBay o MercadoLibre. Este ejemplo muestra:

- 🔨 **Subastas en vivo** - Pujas en tiempo real con actualización instantánea
- ⏰ **Countdown en tiempo real** - Temporizador sincronizado entre todos los usuarios
- 💰 **Sistema de pujas** - Los usuarios pueden hacer ofertas que se actualizan instantáneamente
- 📊 **Historial de pujas** - Registro completo de todas las ofertas realizadas
- 🔔 **Notificaciones** - Alertas cuando alguien supera tu puja o cuando una subasta está por terminar
- 👥 **Múltiples usuarios** - Varios usuarios pueden pujar simultáneamente

Este ejemplo pertenece a la colección de ejemplos de **[Relay Gateway](https://github.com/Coderic/Relay)**, un gateway de comunicación en tiempo real diseñado para ser inmutable y agnóstico.

## 🚀 Inicio Rápido

### Prerrequisitos

- Node.js 18+ o Docker
- Relay Gateway ejecutándose (ver [documentación de Relay](https://relay.coderic.net))

### Instalación

```bash
# Clonar el repositorio
git clone https://github.com/Coderic/subastas.git
cd subastas

# Instalar dependencias
npm install
```

### Configuración

Asegúrate de tener Relay Gateway ejecutándose. Puedes usar el endpoint público para pruebas:

```javascript
// En tu código, el conector se conecta a:
const relay = new RelayConector('http://demo.relay.coderic.net');
```

O ejecuta Relay localmente:

```bash
# Opción 1: Con npx (recomendado para pruebas)
npx @coderic/relay

# Opción 2: Con Docker Compose
docker compose up -d
```

### Desarrollo

```bash
# Iniciar servidor de desarrollo
npm run dev
```

Abre tu navegador en `http://localhost:5173` (o el puerto que Vite asigne).

### Producción

```bash
# Construir para producción
npm run build

# Los archivos estarán en la carpeta dist/
```

## 🎯 Uso

1. **Abrir múltiples pestañas** para simular diferentes usuarios
2. **Identificarse** con un nombre de usuario único
3. **Ver subastas activas** - Explora los productos en subasta
4. **Hacer pujas** - Ofrece un precio y observa cómo se actualiza en tiempo real
5. **Monitorear** - Observa cómo otros usuarios hacen pujas y el temporizador cuenta hacia atrás

## 🔗 Enlaces

- 📦 [Repositorio](https://github.com/Coderic/subastas)
- 🐛 [Issues](https://github.com/Coderic/subastas/issues)
- 🌐 [Demo en línea](https://coderic.org/subastas/)
- 📚 [Documentación de Relay](https://relay.coderic.net)
- ⚡ [Relay Gateway](https://github.com/Coderic/Relay)

## 🛠️ Tecnologías

- **React** - Biblioteca JavaScript para construir interfaces de usuario
- **Vite** - Build tool y dev server
- **Relay Gateway** - Gateway de comunicación en tiempo real
- **Socket.io** - Comunicación WebSocket

## 📝 Licencia

MIT

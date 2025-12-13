# 🔨 Sistema de Subastas en Tiempo Real - React + Pasarela Gateway

Sistema de subastas estilo eBay/MercadoLibre construido con **React** y [Pasarela Gateway](https://github.com/Coderic/Pasarela).

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)
![Vite](https://img.shields.io/badge/Vite-5-646CFF?logo=vite)
![Pasarela](https://img.shields.io/badge/Pasarela-Gateway-blueviolet)

## 🚀 Inicio Rápido

### Prerrequisitos

Pasarela Gateway ejecutándose en `http://localhost:5000`:

```bash
npx pasarela-gateway
```

### Usar este template

1. Haz clic en **"Use this template"** en GitHub
2. Crea tu nuevo repositorio
3. Clona y ejecuta:

```bash
git clone tu-repositorio
cd tu-repositorio
npm install
npm run dev
```

## 📖 Características

- **Subastas en tiempo real**: Pujas instantáneas con sincronización automática
- **Contador regresivo**: Timer en tiempo real para cada subasta
- **Historial de pujas**: Ver todas las pujas realizadas
- **Notificaciones**: Alertas cuando alguien más puja
- **Panel de creación**: Crear nuevas subastas fácilmente
- **Pujas automáticas**: Puja con incremento mínimo o personalizada

## 🎯 Casos de Uso

- 🛒 E-commerce con subastas
- 🎨 Subastas de arte y antigüedades
- 🚗 Subastas de vehículos
- 📱 Subastas de productos tecnológicos
- 🏠 Subastas inmobiliarias

## 💻 Uso del Hook

```jsx
import { usePasarela } from './hooks/usePasarela';

function MiComponente() {
  const { connected, enviarATodos, onMensaje } = usePasarela('mi-usuario-id');

  useEffect(() => {
    const unsubscribe = onMensaje((data) => {
      if (data.tipo === 'nueva_puja') {
        // ¡Nueva puja recibida!
      }
    });
    return unsubscribe;
  }, [onMensaje]);
}
```

## 📁 Estructura

```
src/
├── hooks/
│   └── usePasarela.js    # Hook React para Pasarela
├── App.jsx               # Componente principal
├── App.css               # Estilos
└── main.jsx              # Entry point
```

## 🔗 Enlaces

- [Pasarela Gateway](https://github.com/Coderic/Pasarela)
- [Documentación](https://coderic.github.io/Pasarela/)
- [Otros ejemplos](https://github.com/Coderic?q=pasarela-ejemplo)

## 📄 Licencia

MIT © [Coderic](https://github.com/Coderic)

# TikTok TV (Sleppify)

Un wrapper de TikTok optimizado para Android TV que lleva la experiencia completa de escritorio a la pantalla grande, con soporte mejorado para control remoto, correcciones de diseño y autenticación de Google fluida.

## 🚀 Funciones Principales

### 🎮 Soporte Avanzado para Control Remoto
- **Navegación D-Pad**: Navegación optimizada para desplazarse por el feed (Arriba/Abajo) e interactuar con los menús laterales (Derecha/Izquierda).
- **Mouse Virtual (Estilo Magic Remote)**: Mantén presionado el botón **OK** para activar un cursor basado en física. Permite interactuar con elementos que no son accesibles mediante el enfoque estándar del D-Pad.
- **Enfoque Inteligente de Panel Lateral**: Detección inteligente del video que está actualmente centrado en la pantalla para asegurar que los botones de "Like", "Comentarios" y "Compartir" siempre afecten al video correcto.

### 🔐 Corrección de Inicio de Sesión de Google
- Implementación personalizada de WebView que maneja la autenticación de Google de forma elegante, cambiando dinámicamente entre User Agents y suprimiendo scripts de interferencia durante el flujo de OAuth. Dile adiós al error de "Navegador no compatible".

### 🖼️ Optimizaciones de Diseño y Pantalla
- **Interfaz de Escritorio Forzada**: Obliga a TikTok a cargar la versión completa de escritorio para una experiencia premium en TV, evitando las limitaciones del sitio móvil.
- **Escalado de Viewport**: Ajuste automático de reglas CSS para evitar recortes en la interfaz y asegurar que los botones tengan el tamaño adecuado para pantallas de TV.
- **Correcciones de Pantalla Negra**: Inyecciones de CSS que manejan casos específicos de aceleración de hardware en Android TV.

## 🛠️ Tecnologías Utilizadas
- **Android Nativo**: `MainActivity` basada en Kotlin que gestiona el ciclo de vida del `WebView` y el despacho de eventos de entrada.
- **Puente JavaScript**: Puente personalizado (`tiktok_tv_bridge.js`) que inyecta diseños, gestiona los estados de desplazamiento y proporciona contexto para el control remoto.
- **Motor de Física**: Lógica de aceleración y fricción suave para el movimiento del mouse virtual.

## 📂 Estructura del Proyecto
- `app/src/main/java/.../MainActivity.kt`: Punto de entrada, manejo de entradas y configuración de WebView.
- `app/src/main/assets/tiktok_tv_bridge.js`: El "cerebro" inyectado en TikTok para habilitar comportamientos específicos de TV.
- `app/src/main/res/layout/activity_main.xml`: Contenedor de WebView a pantalla completa.

## ⚙️ Instalación
1. Clona el repositorio.
2. Ábrelo con Android Studio.
3. Compila y despliega en un dispositivo o emulador de Android TV.

---
Creado con ❤️ por [juliots21](https://github.com/juliots21)

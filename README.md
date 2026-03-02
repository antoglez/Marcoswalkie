# MarcosWalkie PTT 🎙️

MarcosWalkie es una aplicación de comunicación estilo **Push-to-Talk (PTT)** desarrollada en Flutter. Permite a los usuarios comunicarse mediante un sistema de transmisión activado por pulsación, con soporte para perfiles personalizados y una interfaz de "bola flotante" (overlay).

## 📥 Descarga Directa (APK)

Puedes encontrar la versión lista para instalar en el directorio raíz de este repositorio:
👉 **[marcoswalkie.apk](./marcoswalkie.apk)**

## 🚀 Guía de Uso y Configuración

Para que la aplicación funcione correctamente, es necesario configurar ciertos permisos y entender cómo funcionan los "Intents".

### 1. Configuración de la Bola Flotante (Overlay) 🟡
La "bola flotante" permite usar el PTT mientras estás en otras aplicaciones (como Zello, navegadores o juegos).
- **Permiso de Superposición**: Al abrir la app por primera vez, te pedirá permiso para "Mostrar sobre otras aplicaciones". **Debes concederlo** para que aparezca el botón flotante.
- **Uso**: Una vez concedido, aparecerá un botón naranja en pantalla. Mantén pulsado para transmitir y suelta para detener.

### 2. Configuración de Intents (Acciones) ⚡
La app funciona enviando "órdenes" (Intents) al sistema o a otras aplicaciones. En la sección de **Gestión de Perfiles**, puedes configurar:

- **Acción de Inicio (Start Action)**: Qué orden enviar al pulsar el botón.
- **Acción de Parada (Stop Action)**: Qué orden enviar al soltar el botón.

#### Ejemplos de Configuración de Intents:
- **Zello (PTT Estilo Walkie)**:
  - Start Action: `com.zello.ptt.down`
  - Stop Action: `com.zello.ptt.up`
- **Acciones del Sistema (Pruebas)**:
  - Abrir Ajustes Wi-Fi: `android.settings.WIFI_SETTINGS`
  - Buscar en Web: `android.intent.action.WEB_SEARCH`

### 3. Permisos Especiales 🛡️
Además del permiso de superposición, si el dispositivo tiene capas de personalización agresivas (Xiaomi, Huawei, etc.), asegúrate de:
- Permitir el **Inicio Automático**.
- Desactivar el **Ahorro de Batería** para MarcosWalkie para evitar que el sistema cierre el servicio del overlay.

## 🛠️ Desarrollo

### Instalación de dependencias
```bash
flutter pub get
```

### Compilación de APK (Manual)
```bash
flutter build apk --release
```

## 🤝 Créditos
Desarrollado con ❤️ por **PGM** y **PEDROAI**.
*Dominación intelectual y control total.*

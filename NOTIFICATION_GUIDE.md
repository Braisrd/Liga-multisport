# 🔔 Guía Maestra de Notificaciones (v3)

## ✅ Estado Actual

1. **Configuración Firebase**: Actualizada con tus datos exactos (incluido `measurementId`).
2. **Service Worker**: Unificado. Ahora un solo archivo (`firebase-messaging-sw.js`) maneja tanto el funcionamiento offline como las notificaciones.
3. **Token**: Arreglado el error 404.

---

## 🔑 La Clave VAPID (¡Importante!)

Para que el botón de "Obtener Token" funcione, necesitas una "Llave VAPID" pública.
Yo he puesto una por defecto, pero **si no es la de tu proyecto, no funcionará**.

### Cómo conseguir TU clave VAPID

1. Ve a [Firebase Console > Configuración del Proyecto > Cloud Messaging](https://console.firebase.google.com/u/0/project/liga-multisport/settings/cloudmessaging).
2. Baja hasta **"Configuración web"**.
3. Si no hay nada, dale a "Generate key pair" (Generar par de claves).
4. Copia la clave larga que empieza por algo como `BcP...` o `AI...`.

### ¿Dónde la pongo?

Si la que tienes es diferente a la que está en el código, avísame y te digo dónde cambiarla (es en `index.html`, buscando "vapidKey").

---

## 🔄 ¿Cómo se actualiza la App?

La aplicación PWA se actualiza sola.

1. **Cierra** la app de la multitarea.
2. **Abre** la app.
3. Espera unos segundos y repite si es necesario.
*Si has cambiado el fondo a azul, significa que ya se ha actualizado.*

---

## 🚀 Resumen del Proceso (El "Método YouTube")

Para enviar un aviso a toda la liga:

1. **Panel Admin > Buzón**: Escribe el mensaje y dale a "Publicar".
    * *(Esto pone el punto rojo en la app)*
2. **Firebase Console > Campaña**: Copia el mismo mensaje, elige "Aplicación web" en Target y envíalo.
    * *(Esto hace vibrar los móviles)*

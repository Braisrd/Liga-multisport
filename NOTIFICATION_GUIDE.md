# 🔔 Guía Maestra de Notificaciones

Esta guía explica **cómo funciona** el sistema de notificaciones de tu app y qué tienes que hacer para enviar avisos como un profesional (estilo YouTube).

---

## 📱 Dos Tipos de Notificaciones

Tu app tiene un sistema híbrido, igual que apps grandes como YouTube o Instagram.

### 1. El Buzón (In-App) 🔴

* **Qué es:** El mensaje que se queda guardado dentro de la app.
* **Dónde se ve:** En la campana de la esquina superior derecha.
* **Efecto:** Aparece un **Punto Rojo** 🔴 en la campana hasta que el usuario lo abre.
* **Duración:** El mensaje permanece ahí para que puedan leerlo más tarde.
* **Cómo se envía:** Desde tu propio **Panel de Admin > Pestaña Buzón**.

### 2. La Notificación Push (Móvil) 📲

* **Qué es:** El aviso que vibra y suena en el móvil, incluso si la app está cerrada.
* **Dónde se ve:** En la pantalla de bloqueo o barra de estado del móvil.
* **Efecto:** "Despierta" al usuario para que entre a la app.
* **Cómo se envía:** Desde **Firebase Console** (Google).

---

## 🚀 Cómo Enviar una Notificación (Paso a Paso)

Para hacerlo perfecto (que vibre el móvil Y se quede el mensaje guardado), debes hacer los dos pasos:

### PASO 1: Guardar el Mensaje (El Buzón)

1. Abre tu App y entra como Admin (candado 🔒).
2. Ve a la pestaña **Buzón**.
3. Escribe el **Título** y el **Mensaje**.
4. Dale a **"Publicar en la App"**.
    * *Resultado*: Todos verán el punto rojo 🔴 la próxima vez que abran la app.

### PASO 2: Despertar a la Gente (Push)

1. Ve a [Firebase Console > Messaging](https://console.firebase.google.com/u/0/project/liga-multisport/notification/compose).
2. Dale a **"Nueva campaña"** -> **"Notificaciones"**.
3. Copia el MISMO título y texto que pusiste en el Buzón.
4. **Destinatario (Target)**: Selecciona tu aplicación web (identificador: `web:a86d9e...`).
5. Dale a **Revisar** y **Publicar**.
    * *Resultado*: Les vibrará el móvil a quienes hayan dado permiso 🔔.

---

## 💡 Preguntas Frecuentes

### ¿Por qué tengo que hacer dos cosas?

Porque Google cobra dinero si queremos automatizar esto (requiere "Cloud Functions"). Al hacerlo manual, **es gratis para siempre** y tienes control total.

### ¿Qué pasa si solo hago el Paso 1 (Buzón)?

El mensaje se guarda, pero nadie se entera hasta que abren la app por su cuenta. Es como subir un vídeo a YouTube sin avisar a los suscriptores.

### ¿Qué pasa si solo hago el Paso 2 (Push)?

El móvil vibra, el usuario lee "Torneo Mañana"... pero si la borran sin querer y entran a la app, **no verán nada en el buzón** y se les puede olvidar.

---

## 🎓 Consejo Pro (Estilo YouTube)

YouTube hace lo mismo:

1. Te manda la notificación al móvil (Push).
2. Cuando entras, tienes el número rojo en la campana (Buzón) para que veas el historial.

**Tu app ahora funciona exactamente igual.**

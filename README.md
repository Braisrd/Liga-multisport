# Liga Multisport - README

## Descripción

Aplicación web para la gestión de la Liga Multisport del Paso de Ecuador 25/26.
Diseñada para ser ejecutada directamente en el navegador sin necesidad de servidores complejos.

## Instrucciones de Uso

### 1. Iniciar la Aplicación

Simplemente hz **doble click** en el archivo `liga_multisport.html`. Se abrirá en tu navegador predeterminado (Chrome, Edge, etc.).

> **Nota**: Asegúrate de tener conexión a Internet, ya que la aplicación carga librerías (React, Tailwind) desde servidores CDN.

### 2. Modo Administrador

- Accede al modo administrador pulsando el candado en la parte superior derecha o escribiendo la contraseña en el campo invisible al final de la página.
- **Contraseña por defecto**: `4321`
- Desde el panel de control puedes:
  - Añadir Jugadores
  - Registrar Torneos
  - Cambiar la contraseña
  - Editar el texto de información

### 3. Puntuación

El sistema calcula los puntos automáticamente:

- **Ganador**: +5 puntos
- **Segundo**: +3 puntos
- **Participante**: +1 punto (se suma automáticamente a todos los jugadores listados que NO sean ni el primero ni el segundo).

### 4. Backup de Datos

Los datos se guardan en el "Almacenamiento Local" (LocalStorage) de tu navegador.

- **⚠️ Importante**: Si borras la caché del navegador, perderás los datos.
- Para hacer una copia de seguridad, puedes pedirle a un técnico que exporte el `localStorage` o simplemente no borrar el historial de ese navegador.

# clase_20241028

### Paso 1: Crear el Proyecto Node.js con Express
1. **Instala Node.js y npm** (si aún no lo tienes instalado):
   - Visita la [página oficial de Node.js](https://nodejs.org/) y descarga la versión LTS.
   - Completa el proceso de instalación para tu sistema operativo.

2. **Genera un nuevo proyecto con Express usando `npx`**:
   - Abre una terminal y navega hasta el directorio donde deseas crear el proyecto.
   - Ejecuta el siguiente comando para generar el proyecto con `npx`, sin necesidad de instalar el generador globalmente:
     ```bash
     npx express-generator nombre_proyecto --view=ejs
     ```
   - Esto creará una carpeta con el nombre que elijas (`nombre_proyecto`) y configurará la estructura de archivos usando EJS como motor de plantillas.

3. **Crea un archivo `.gitignore` para ignorar `node_modules`**:
   - En el directorio de tu proyecto, crea un archivo `.gitignore` y agrega `node_modules` para que Git ignore esta carpeta:
     ```bash
     echo "node_modules" > .gitignore
     ```

4. **Instala las dependencias**:
   - Accede a la carpeta de tu proyecto y ejecuta:
     ```bash
     cd nombre_proyecto
     npm install
     ```

### Paso 2: Implementar la Página Inicial
1. **Edita la Ruta Inicial**:
   - En tu proyecto, abre `routes/index.js` y asegúrate de que la ruta inicial (`/`) renderice la página `index` con la información que deseas mostrar.

2. **Edita la Plantilla EJS**:
   - Abre el archivo `views/index.ejs`.
   - Modifica el contenido para mostrar tu nombre completo, número de cédula y sección inscrita. Por ejemplo:
     ```html
     <h1>Hola Mundo</h1>
     <p>Nombre: Tu Nombre Completo</p>
     <p>Cédula: Tu Número de Cédula</p>
     <p>Sección: Tu Sección Inscrita</p>
     ```

3. **Prueba la Aplicación Localmente**:
   - Ejecuta tu aplicación:
     ```bash
     npm start
     ```
   - Abre `http://localhost:3000` en tu navegador para ver la página.

### Paso 3: Subir el Código a GitHub
1. **Inicia un Repositorio Git en tu Proyecto**:
   ```bash
   git init
   git add .
   git commit -m "Primera versión del proyecto Hola Mundo"
   ```

2. **Crea un Repositorio en GitHub**:
   - Visita [GitHub](https://github.com/) y crea un nuevo repositorio llamado `P2_CEDULA` (reemplazando `CEDULA` con tu número de cédula).

3. **Sube el Proyecto a GitHub**:
   - Sigue las instrucciones de GitHub para conectar tu proyecto local al repositorio y subir los archivos:
     ```bash
     git remote add origin https://github.com/tu_usuario/P2_CEDULA.git
     git push -u origin main
     ```

### Paso 4: Crear un Proyecto en Render.com
1. **Crea una Cuenta en Render.com** (si aún no la tienes):
   - Ve a [Render.com](https://render.com/) y regístrate.

2. **Configura un Nuevo Proyecto**:
   - En el panel de Render, selecciona **New Web Service**.
   - Elige **Connect to a Git Repository** y conecta tu cuenta de GitHub.
   - Selecciona el repositorio `P2_CEDULA` que creaste en el paso anterior.
   - Configura el proyecto para que se despliegue automáticamente cada vez que realices cambios en el repositorio.

3. **Configura los Detalles del Servicio**:
   - En las opciones de configuración, selecciona **Node** como entorno, y en el campo de comando de inicio ingresa:
     ```bash
     npm start
     ```

4. **Despliega la Aplicación**:
   - Render.com se encargará de construir y desplegar tu aplicación. Al finalizar, te proporcionará una URL pública.

### Paso 5: Asegurar la Visualización de la Página
1. **Verifica el Despliegue**:
   - Accede a la URL proporcionada por Render.com para comprobar que tu página inicial se muestra correctamente con el mensaje de "Hola Mundo" y tu información personal.

### Paso 6: Entrega de la Tarea
1. **En Google Classroom**:
   - Copia el enlace de tu repositorio en GitHub.
   - Copia el enlace de tu aplicación en Render.com.
   - Pega ambos enlaces en la tarea correspondiente en Google Classroom.

Recuerda revisar y documentar tu código antes de subirlo. ¡Suerte!

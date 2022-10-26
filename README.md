# Curso de Vue.js: Componentes y Composition API

🚀 Lo que verás a continuación son mis apuntes del curso. Si ves algún error o punto de mejora no dudes en hcer tus contribuciones 💚

Conoce el funcionamiento a profundidad de los componentes de Vue.js. Descubre qué son los componentes dinámicos y asíncronos así como el manejo de transiciones y teleports dentro de esta librería. Explora cómo funciona Composition API dentro de Vue.js junto con tu profesora Diana Martínez.

- Aprender el uso de Vue CLI.
- Comprender las diferencias entre Option y Composition API.
- Entender cómo funciona Composition API.
- Conocer el ciclo de vida de Vue.js.

# Introducción

## Instalación
```bash
npm install -g @vue/cli
```

## Creacion de proyecto con Vue CLI

Para la creación de nuestro primer proyecto ejecutaremos los siguientes comandos

```bash
vue create options
```
Las configuraciones elegidas fueron:
features: Babel, Linter
Version: 3.x
formatter: Prettier

Luego:
```bash
cd options
npm run serve
```
Si queremos generar código para prodcción ejecutamos
```bash
npm run build
```
Con `vue ui` se puede generar una interfaz para administrar todas las opciones del proyecto

## Estructura del proyecto

- **package.json** → Tiene nuestras dependencias, nuestros scripts que correremos con npm, nos prepara el terreno para poder trabajar.
- **README.md** → Podemos ver los distintos comandos para poder instalar dependencias, ejecutar el servidor de desarrollo, compilar para producción, eslinter, documentación oficial.
- **babel.config.js** → Configuración de babel. Es pequeño debido a que el equipo de desarrollo detrás de este proyecto ya se encargó de generar un preset de babel js, que ya lo tiene instalado nuestro proyecto.
- **.gitignore** → Ignorar archivos para no subirlos al repositorio.
- **.eslintrc.js** → Archivo para configurar eslint, este archivo agrega dos reglas, cuando se tenga activado el modo productivo se va a pedir que no se tengan console.log() y que no hayan debugger.
- **.browserslistrc** → Le indicamos con que versiones de navegadores debe trabajar.
- **node_modules** → En esta carpeta van a estar todos los módulos y dependencias que tiene nuestro proyecto.
- **public/** → Esta carpeta contiene un favicon.ico y un index.html, corre en un servidor de archivos estáticos.
- **src/** → La carpeta más importante, vamos a colocar todos los archivos en los que de verdad vamos a estar trabajando durante el desarrollo del proyecto. El archivo main.js es el archivo que va a encontrar el proyecto de webpack y lo va a utilizar para inicializar todo lo que tiene que ver con JavaScript en nuestro proyecto.
- **src/App.vue** → Componente principal, es en el que se creará la App en main.js.
- **src/assets** → Contendrá archivos estáticos, la diferencia entre src/assets y public/ es que assets se va a empaquetar junto con los archivos del proyecto, es decir, se va adjuntar todo el código javascript, css y html que se genere y también se van a incluir estos archivos estáticos en la carpeta dist (Creada con npm run build), lo que pasa con public es que esto no pasa a la carpeta dist, sin embargo, quedaría más del lado del servido, mientras que assets queda del lado del cliente.
- **src/components** → Esta carpeta contendrá todos los componentes hechos en Vue.js que utilizaremos en nuestro proyecto. Esta carpeta se puede estructurar como sea, se pueden tener subcarpetas, por ejemplo.


# Built-in Components

Para aplicar estilos css específicos para cada componente generalmente lo que se hace es separarlos en archivos Vue distintos y usar la propiedad `scoped`. `style scoped`

`<!-- Add "scoped" attribute to limit CSS to this component only -->`

Así se pueden hacer clases con el mismo nombre o editar tags predeterminados sin afectar los demás componente

Los estilos que se escriben en el archivo `App.vue` aplican de forma global para todo el proyecto

# Fuentes de información

- [Installation | Vue CLI](https://cli.vuejs.org/guide/installation.html)
- [Configuration Reference](https://cli.vuejs.org/config/).
- [Creating a Project | Vue CLI](https://cli.vuejs.org/guide/creating-a-project.html)

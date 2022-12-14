# Curso de Vue.js: Componentes y Composition API

馃殌 Lo que ver谩s a continuaci贸n son mis apuntes del curso. Si ves alg煤n error o punto de mejora no dudes en hcer tus contribuciones 馃挌

Conoce el funcionamiento a profundidad de los componentes de Vue.js. Descubre qu茅 son los componentes din谩micos y as铆ncronos as铆 como el manejo de transiciones y teleports dentro de esta librer铆a. Explora c贸mo funciona Composition API dentro de Vue.js junto con tu profesora Diana Mart铆nez.

- Aprender el uso de Vue CLI.
- Comprender las diferencias entre Option y Composition API.
- Entender c贸mo funciona Composition API.
- Conocer el ciclo de vida de Vue.js.

# Introducci贸n

## Instalaci贸n
```bash
npm install -g @vue/cli
```

## Creacion de proyecto con Vue CLI

Para la creaci贸n de nuestro primer proyecto ejecutaremos los siguientes comandos

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
Si queremos generar c贸digo para prodcci贸n ejecutamos
```bash
npm run build
```
Con `vue ui` se puede generar una interfaz para administrar todas las opciones del proyecto

## Estructura del proyecto

- **package.json** 鈫? Tiene nuestras dependencias, nuestros scripts que correremos con npm, nos prepara el terreno para poder trabajar.
- **README.md** 鈫? Podemos ver los distintos comandos para poder instalar dependencias, ejecutar el servidor de desarrollo, compilar para producci贸n, eslinter, documentaci贸n oficial.
- **babel.config.js** 鈫? Configuraci贸n de babel. Es peque帽o debido a que el equipo de desarrollo detr谩s de este proyecto ya se encarg贸 de generar un preset de babel js, que ya lo tiene instalado nuestro proyecto.
- **.gitignore** 鈫? Ignorar archivos para no subirlos al repositorio.
- **.eslintrc.js** 鈫? Archivo para configurar eslint, este archivo agrega dos reglas, cuando se tenga activado el modo productivo se va a pedir que no se tengan console.log() y que no hayan debugger.
- **.browserslistrc** 鈫? Le indicamos con que versiones de navegadores debe trabajar.
- **node_modules** 鈫? En esta carpeta van a estar todos los m贸dulos y dependencias que tiene nuestro proyecto.
- **public/** 鈫? Esta carpeta contiene un favicon.ico y un index.html, corre en un servidor de archivos est谩ticos.
- **src/** 鈫? La carpeta m谩s importante, vamos a colocar todos los archivos en los que de verdad vamos a estar trabajando durante el desarrollo del proyecto. El archivo main.js es el archivo que va a encontrar el proyecto de webpack y lo va a utilizar para inicializar todo lo que tiene que ver con JavaScript en nuestro proyecto.
- **src/App.vue** 鈫? Componente principal, es en el que se crear谩 la App en main.js.
- **src/assets** 鈫? Contendr谩 archivos est谩ticos, la diferencia entre src/assets y public/ es que assets se va a empaquetar junto con los archivos del proyecto, es decir, se va adjuntar todo el c贸digo javascript, css y html que se genere y tambi茅n se van a incluir estos archivos est谩ticos en la carpeta dist (Creada con npm run build), lo que pasa con public es que esto no pasa a la carpeta dist, sin embargo, quedar铆a m谩s del lado del servido, mientras que assets queda del lado del cliente.
- **src/components** 鈫? Esta carpeta contendr谩 todos los componentes hechos en Vue.js que utilizaremos en nuestro proyecto. Esta carpeta se puede estructurar como sea, se pueden tener subcarpetas, por ejemplo.


# Built-in Components

Para aplicar estilos css espec铆ficos para cada componente generalmente lo que se hace es separarlos en archivos Vue distintos y usar la propiedad `scoped`. `style scoped`

`<!-- Add "scoped" attribute to limit CSS to this component only -->`

As铆 se pueden hacer clases con el mismo nombre o editar tags predeterminados sin afectar los dem谩s componente

Los estilos que se escriben en el archivo `App.vue` aplican de forma global para todo el proyecto

# Fuentes de informaci贸n

- [Installation | Vue CLI](https://cli.vuejs.org/guide/installation.html)
- [Configuration Reference](https://cli.vuejs.org/config/).
- [Creating a Project | Vue CLI](https://cli.vuejs.org/guide/creating-a-project.html)

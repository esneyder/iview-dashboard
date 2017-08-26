# Iview-Dashboard
Un ejemplo sencillo de dashboard basada en Vue2 + iView2.0.
[Demo](https://iview-dashboard.herokuapp.com)

----------------

### Instalacion
```
npm install          // instala las dependencias
npm run dev          // desarrollo
npm run build        // producción
```
----------------

### Estructura de directorios
  |-- build                        // archivo de configuración de webpack
  |-- config                       // ruta del paquete del proyecto
  |-- static                       // directorio de archivos estáticos
  |-- src                          // directorio de fuentes
  |  |-- componentes               // componentes
  |      |-- common                // globales
  |          |-- about.vue         // acerca de
  |          |-- index             // inicio
  |          |-- login.vue         // inicio de sesión
  |     |-- page                   //Paginas
  |       |-- Eharts.vue           // baidu echarts
  |       |-- form.vue             // formulario
  |       |-- rtf.vue              // cuadro de texto enriquecido
  |       |-- Markdown-viewer.vue  // exhibición de markdown
  |       |-- markdown-editor.vue  // editor de markdown
  |       |-- tablas               // tablas
  |       |-- upload.vue           // archivo de carga
  |   |-- App.vue                  // entrada de página
  |   |-- main.js                  // entrada del programa
  |-- .babelrc                     // ES6 Configuración de la compilación de sintaxis
  |-- .editorconfig                // código para escribir especificaciones
  |-- .gitignore                   // push Ignora los archivos
  |-- index.html                   // entrada página html
  |-- package.json                 // dependencias y configuración
  |-- README.md                    // Introducción

----------------

### Capturas de pantalla

![1](/static/screenshots/s1.png)
![2](/static/screenshots/s2.png)
![3](/static/screenshots/s3.png)
![4](/static/screenshots/s4.png)

----------------

### Dependencias
- [x] página: [iView2.0](https://github.com/iview/iview)
- [x] Visualización de Markdown: [VueMarkdown](https://github.com/miaolz123/vue-markdown)
- [x] Editor de Markdown: [MarkdownEditor](https://github.com/alecgorge/MarkdownEditor) y [Vue-SimpleMDE](https://github.com/Float/vue-simplemde)
- [x] cuadro de texto enriquecido: [quillEditor](https://github.com/surmon-china/vue-quill-editor)
- [x] Gráfico: [Eqarts Baidu](http://echarts.baidu.com) y [Vue-Echarts](https://github.com/xlsdg/vue-echarts-v3)
- [x] carga de archivo: [uso iView propio componente de carga de archivos](https://www.iviewui.com/components/upload)

----------------

### Licencia
[MIT](https://opensource.org/licenses/MIT)

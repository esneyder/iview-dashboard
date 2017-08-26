# Iview2-manage-system

Un ejemplo sencillo de una solución de sistema de gestión de fondo basada en Vue2 + iView2.0.

Acceso en línea (no es compatible con el teléfono / ha sido lento para reparar el problema): [acceso a computadora] (http://139.199.33.111/dist)

--------------

### Aviso
* 6.4 porque la energía es limitada, decidió dejar de mantener el proyecto, pero todavía está disponible, para aplicaciones prácticas, por favor, preste atención a iview sitio web oficial para comprender los cambios API. ¡Lo siento!

--------------

### La implementación actual de la función y el uso de componentes
- [x] página: [iView2.0] (https://github.com/iview/iview)
- [x] Visualización de Markdown: [VueMarkdown] (https://github.com/miaolz123/vue-markdown)
- [x] Editor de Markdown: [MarkdownEditor] (https://github.com/alecgorge/MarkdownEditor) y [Vue-SimpleMDE] (https://github.com/F-loat/vue-simplemde)
- [x] cuadro de texto enriquecido: [quillEditor] (https://github.com/surmon-china/vue-quill-editor)
- [x] Gráfico: [Eqarts Baidu] (http://echarts.baidu.com) y [Vue-Echarts] (https://github.com/xlsdg/vue-echarts-v3)
- [x] carga de archivo: [uso iView propio componente de carga de archivos] (https://www.iviewui.com/components/upload)

--------------

### uso
¡Bienvenido!
Npm i // instala dependencias
Npm run dev // desarrollo local
Npm run build // implementación de producción
¡Bienvenido!
--------------

### estructura de directorios
| - build // archivo de configuración de webpack
| --config // ruta del paquete del proyecto
Directorio estático de archivos estáticos
| - src // directorio de fuentes
| - componentes // componentes
| - comunes // globales
Acerca de la página
| -.
| - login.vue // página de inicio de sesión
La página principal
Eharts.vue // baidu echarts
Forma - form.vue // formulario
| Rtf.vue // cuadro de texto enriquecido
| Markdown-viewer.vue // exhibición de markdown
- markdown-editor.vue // editor de markdown
| - tablas
| - upload.vue // archivo de carga
| - App.vue // entrada de página
| - main.js // entrada del programa
| - .babelrc // ES6 Configuración de la compilación de sintaxis
| .editorconfig // código para escribir especificaciones
| - .gitignore // push Ignora los archivos
| - index.html // entrada página html
| - package.json // dependencias y configuración
| - README.md // Introducción
Al mismo tiempo que
--------------

### Capturas de pantalla

![1](/static/screenshots/s1.png)
![2](/static/screenshots/s2.png)
![3](/static/screenshots/s3.png)
![4](/static/screenshots/s4.png)

----------------
### Problemas y instrucciones de mantenimiento
1. La ruta de la fuente es incorrecta y la próxima actualización será fija

2. Este proyecto es sólo un ejemplo simple, la aplicación real también debe agregar la necesidad de lograr la función

3. Parte de la referencia a [Vue2 backstage management system solutions] (https://github.com/lin-xin/manage-system)

---------------

### otro
Tenga cualquier pregunta o sugerencia bienvenida a la edición del problema.

---------------

### Licencia
[MIT](https://opensource.org/licenses/MIT)

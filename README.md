# Define que es un componente y al crearlo que elementos lo forman.
Un componente es un elemento reutilizable. Puede ser desde un elemento HTML como un <button> hasta una lista , un header, un section, o un conjunto de etiquetas o elementos div que tengan una funcionalidad en particular.
Un componente en Angular es un elemento que está compuesto por:
Un archivo que será nuestro Template (app.component.html), el cual es nuestro HTML, que es el que se va a visualizar en la interfaz de usuario, la vista o en términos más simples lo que vas a ver en la página. 
Un archivo de lógica, la cual es la que pondremos en un archivo .ts (como por ejemplo app.component.ts), ese archivo debe incluir una clase y esta es la que va a contener las propiedades que se van a usar en la vista (HTML) y los métodos que será las acciones que se ejecutarán en la vista. En este archivo de lógica también se incluye una metadata, que es definida con un decorador, que identifica a Angular como un componente.
Un archivo para el CSS (podemos usar un preprocesador como SASS o LESS), donde incluiremos los estilos, lo que nos ayuda a hacer bonita nuestra aplicación.
# Define que es un módulo y que función tiene el patrón de diseño decorator.
Las aplicaciones Angular son modulares y Angular tiene su propio sistema de modularidad llamado NgModules. Los NgModules son contenedores para un bloque cohesivo de código dedicado a un dominio de aplicación, un flujo de trabajo o un conjunto de capacidades estrechamente relacionadas. Pueden contener componentes, proveedores de servicios y otros archivos de código cuyo alcance está definido por el NgModule que los contiene. Pueden importar la funcionalidad que se exporta desde otros NgModules y exportar la funcionalidad seleccionada para que la utilicen otros NgModules.
# Menciona y describe los elementos importantes de un @NgModule
 Un NgModule está definido por una clase decorada con @NgModule(). El decorador @NgModule() es una función que toma un único objeto de metadatos, cuyas propiedades describen el módulo. Las propiedades más importantes son las siguientes.
- declarations: Los componentes, directivas, y pipes que pertenecen a este NgModule.
- exports: El subconjunto de declaraciones que deberían ser visibles y utilizables en las plantillas de componentes de otros NgModules.
- imports: Otros módulos cuyas clases exportadas son necesarias para las plantillas de componentes declaradas en este NgModule.
- providers: Creadores de servicios que este NgModule aporta a la colección global de servicios; se vuelven accesibles en todas las partes de la aplicación. (También puedes especificar proveedores a nivel de componente, que a menudo es preferido).
- bootstrap: La vista principal de la aplicación, llamado el componente raíz, que aloja todas las demás vistas de la aplicación. Sólo el NgModule raíz debe establecer la propiedad bootstrap.


El sistema de model view controller es un patron en donde podemos organizar nuestro software en donde tenemos 3 categorias 

Modelo quien es responsable de presentar la informacion y la logica de negocio de la aplicacion. Es el encargado de manejar los datos y la interaccion de la base de datos y proporciona una interfaz para acceder y modificar los datos almacenados 

**La vista** es la responsable de presentar la informacion al usuario de manera clara y organizada. 
Me encantaría que pudiesemos empezar con una nueva manera de escribir 
primero seria escribiendo con todos los dedos correctamente posisionados en el teclado y mirandolo lo menos posible 

Probablemente tengas muchos errores en un principio debido a malos habitos que hay que comenzar a evitar 


Controlador: Actuia como intermediario entre el modelo y la vista, gestionando la comunicacion y coordinando las acciones. Procesa la entrada, interactúa con el modelo para realizar cambios y actualiza la vista según sea necesario.

El patrón MVC promueve la separación de las responsabilidades y facilita la mantenibilidad, escalabilidaday reutilizacion del código en aplicaciónes de software.



## MVC a Clean MVC 

La arquitectura limpia, también conocida como arquitectura hexagonal, capas concéntricas o el enfoque de "cebolla", se basa en la idea de separar los aspectos más esenciales y de alto nivel de la lógica de negocio (las reglas del negocio) de los detalles menos esenciales y de bajo nivel (interfaz de usuario, bases de datos, frameworks, etc.).

Podemos tomar el patrón MVC como punto de partida y adaptarlo a una arquitectura limpia de la siguiente manera:

1.  **Entidades (Núcleo de la arquitectura limpia)**: Estas serían equivalentes a los Modelos en MVC. Son las clases que contienen las reglas de negocio de alto nivel y no dependen de ninguna otra capa.
    
2.  **Casos de uso**: Aquí es donde se aplican las reglas de negocio de alto nivel sobre las entidades. En MVC, esto podría ser parte del trabajo que hace un Controlador, aunque en una arquitectura limpia, esta lógica se mantendría separada y pura, sin mezclarla con la lógica de la interfaz de usuario o la lógica de acceso a datos.
    
3.  **Controladores y Presentadores**: Esta sería una ampliación del papel del Controlador en MVC. El Controlador maneja la entrada del usuario, la cual usa para interactuar con los Casos de Uso. Luego, el Presentador recibe los resultados de los Casos de Uso y los transforma en una forma adecuada para la Vista.
    
4.  **Vista**: Similar a la Vista en MVC, este componente se encarga de presentar la información al usuario. Sin embargo, en una arquitectura limpia, la Vista sería aún más delgada y menos inteligente, con la mayoría de la lógica de presentación manejada por el Presentador.
    
5.  **Capa de infraestructura**: Esta capa no tiene un equivalente directo en MVC y maneja detalles de bajo nivel como acceso a bases de datos, redes, y otras operaciones que no se relacionan directamente con las reglas de negocio. En una arquitectura limpia, las dependencias siempre apuntan hacia adentro, lo que significa que las capas de nivel superior no dependen de esta capa de infraestructura.
    

El objetivo de la arquitectura limpia es hacer que el sistema sea más mantenible, flexible y escalable, y menos dependiente de detalles específicos de la infraestructura, marcos de trabajo o interfaces de usuario.

Hexagonal architecture, also known as Ports and Adapters, is an architectural pattern that promotes separation of concerns, testability, and maintainability. It is based on layers like an onion and proposes three base layers: Domain, Application, and Infrastructure. The core of the layers is the Domain, which does not couple to anything external. Instead, it relies on the principle of inversion of dependencies [dev.to](https://dev.to/esaraviam/hexagonal-architecture-applied-to-typescript-react-project-enn).

To apply hexagonal architecture in a React microfrontend, you can follow these steps:

1.  **Domain Layer**: Define your domain entities, value objects, and domain services. This layer should not have any dependencies on external libraries, frameworks, or infrastructure [dev.to](https://dev.to/esaraviam/hexagonal-architecture-applied-to-typescript-react-project-enn).

2.  **Application Layer**: Implement use cases, which contain the business logic and orchestrate domain services. This layer should not depend on specific UI frameworks or data sources [dev.to](https://dev.to/esaraviam/hexagonal-architecture-applied-to-typescript-react-project-enn)    
3.  **Infrastructure Layer**: Implement adapters for external systems, such as APIs, databases, or third-party services. This layer should translate external data formats and protocols into domain objects [dev.to](https://dev.to/esaraviam/hexagonal-architecture-applied-to-typescript-react-project-enn).

4.  **React Components**: Create your React components, which will act as the UI layer. These components should only depend on the Application Layer, calling use cases to interact with the system [medium.com](https://medium.com/swlh/inside-out-hexagonal-architecture-in-react-de0642a31e63).    
 
5.  **Microfrontend Architecture**: Organize your application into smaller, independent units, each responsible for a specific feature or functionality. This allows for better scalability, maintainability, and flexibility [sitepoint.com](https://www.sitepoint.com/a-beginners-guide-to-the-micro-front-end-architecture/).

Pros and cons of applying hexagonal architecture to a React microfrontend:
**Pros**:

-   Separation of concerns: Each layer has a specific responsibility, making it easier to understand and modify the code.
-   Testability: Since dependencies are inverted, it is easier to mock external systems and test the application in isolation.
-   Flexibility: Changing external systems or swapping UI frameworks is less painful, as the business logic is decoupled from the implementation details.

**Cons**:

-   Complexity: Introducing hexagonal architecture can increase the complexity of the project, making it harder to understand for newcomers.
-   Over-engineering: For smaller projects or prototypes, implementing hexagonal architecture might be overkill and may not provide significant benefits.



![[hexagon_layer.png]]

La arquitectura hexagonal, también conocida como "puertos y adaptadores", es un patrón de diseño que promueve la separación de preocupaciones y la abstracción de las dependencias. La idea central es dividir la aplicación en tres capas principales:

1.  Capa de dominio: Contiene la lógica de negocio y las entidades del dominio.
2.  Capa de aplicación: Gestiona los casos de uso y coordina las interacciones entre la capa de dominio y la capa de infraestructura.
3.  Capa de infraestructura: Implementa detalles técnicos como acceso a bases de datos, comunicación con servicios externos y adaptadores para la capa de presentación.

Para implementar la arquitectura hexagonal en una aplicación React Hooks-Redux, sigue estos pasos:

1.  Organiza tu proyecto en carpetas que representen las capas de la arquitectura hexagonal. Por ejemplo:
    
    -   `src/domain`: Contiene la lógica de negocio y las entidades del dominio.
    -   `src/application`: Contiene los casos de uso y la coordinación entre las capas.
    -   `src/infrastructure`: Contiene adaptadores y detalles técnicos como la configuración de Redux.
2.  Define las interfaces (puertos) en la capa de aplicación para abstraer las dependencias externas de la lógica de negocio. Por ejemplo, crea interfaces para los repositorios de datos y servicios externos.
    
3.  Implementa adaptadores en la capa de infraestructura para conectarse a recursos externos (bases de datos, APIs) y para interactuar con la capa de presentación (React Hooks-Redux).
    
4.  Utiliza Redux para gestionar el estado de la aplicación y conectar la capa de aplicación con la capa de presentación. Define acciones y reducers para representar las interacciones del usuario y las actualizaciones del estado.
    
5.  Implementa componentes de React utilizando Hooks para manejar el estado local y los efectos secundarios. Conecta estos componentes a Redux usando `useSelector` y `useDispatch` para acceder al estado global y disparar acciones.
    
6.  Inyecta las dependencias (adaptadores) en la capa de aplicación utilizando el patrón de Inversión de Control (IoC) o contenedores de inyección de dependencias. Esto permite cambiar fácilmente las implementaciones de los adaptadores sin modificar la lógica de negocio.



'''
my-app/
├── public/
├── src/
│   ├── common/
│   │   ├── components/
│   │   ├── hooks/
│   │   ├── utils/
│   │   └── styles/
│   ├── features/
│   │   ├── FeatureA/
│   │   │   ├── domain/
│   │   │   │   ├── entities/
│   │   │   │   └── interfaces/
│   │   │   ├── application/
│   │   │   │   └── useCases/
│   │   │   ├── infrastructure/
│   │   │   │   ├── api/
│   │   │   │   ├── repositories/
│   │   │   │   └── redux/
│   │   │   │       ├── actions/
│   │   │   │       ├── reducers/
│   │   │   │       └── store.js
│   │   │   └── presentation/
│   │   │       ├── components/
│   │   │       └── pages/
│   │   └── FeatureB/
│   │       ├── ... (similar a FeatureA)
│   └── index.js
├── .env
├── .gitignore
└── package.json
'''

´´´
my-app/
  ├── src/
  │   ├── application/
  │   │   ├── useCases/
  │   │   │   ├── useCase1.js
  │   │   │   ├── useCase2.js
  │   │   │   └── ...
  │   │   ├── ports/
  │   │   │   ├── IRepository.js
  │   │   │   ├── IService.js
  │   │   │   └── ...
  │   │   └── ...
  │   ├── domain/
  │   │   ├── entities/
  │   │   │   ├── Entity1.js
  │   │   │   ├── Entity2.js
  │   │   │   └── ...
  │   │   └── ...
  │   ├── infrastructure/
  │   │   ├── adapters/
  │   │   │   ├── RepositoryAdapter.js
  │   │   │   ├── ServiceAdapter.js
  │   │   │   └── ...
  │   │   ├── api/
  │   │   │   ├── index.js
  │   │   │   └── ...
  │   │   ├── redux/
  │   │   │   ├── actions/
  │   │   │   │   ├── action1.js
  │   │   │   │   ├── action2.js
  │   │   │   │   └── ...
  │   │   │   ├── reducers/
  │   │   │   │   ├── reducer1.js
  │   │   │   │   ├── reducer2.js
  │   │   │   │   └── ...
  │   │   │   ├── store.js
  │   │   │   └── ...
  │   │   └── ...
  │   ├── presentation/
  │   │   ├── components/
  │   │   │   ├── Component1/
  │   │   │   │   ├── index.js
  │   │   │   │   └── styles.css
  │   │   │   ├── Component2/
  │   │   │   │   ├── index.js
  │   │   │   │   └── styles.css
  │   │   │   └── ...
  │   │   ├── pages/
  │   │   │   ├── Page1/
  │   │   │   │   ├── index.js
  │   │   │   │   └── styles.css
  │   │   │   ├── Page2/
  │   │   │   │   ├── index.js
  │   │   │   │   └── styles.css
  │   │   │   └── ...
  │   │   ├── App.js
  │   │   ├── index.js
  │   │   └── ...
  │   ├── utils/
  │   │   ├── utility1.js
  │   │   ├── utility2.js
  │   │   └── ...
  │   └── ...
  ├── public/
  │   ├── index.html
  │   ├── favicon.ico
  │   └── ...
  ├── .gitignore
  ├── package.json
  ├── README.md
  └── ...
´´´
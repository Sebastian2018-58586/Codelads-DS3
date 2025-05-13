# codelab sobre Clean Architecture

### 1. ¿Qué problema busca resolver Clean Architecture en el desarrollo de software?
Clean Architecture busca resolver el problema del acoplamiento entre la lógica de negocio y la infraestructura, permitiendo que las aplicaciones sean más mantenibles, escalables y testeables.
Los problemas específicos que resuelve incluyen:
- Dificultad para cambiar de framework o tecnología sin afectar la lógica de negocio.
- Código difícil de probar debido a dependencias directas con bases de datos o frameworks.
- Poca reutilización de la lógica de negocio en diferentes contextos (como en aplicaciones web, móviles o de escritorio).

### 2. ¿Cuáles son las principales capas de Clean Architecture y qué responsabilidad tiene cada una?
Clean Architecture se basa en cuatro capas concéntricas, donde las dependencias siempre apuntan hacia el núcleo:

- **Entidad (Domain Layer)**: Contiene la lógica de negocio central. Define entidades con reglas inmutables del negocio. Independiente de frameworks y tecnología.
- **Casos de Uso (Application Layer)**: Implementa la lógica específica de aplicación. Orquesta las entidades y define casos de uso (UseCases). Independiente de infraestructura.
- **Adaptadores (Interface Layer)**: Expone interfaces para interactuar con la aplicación. Contiene controladores (controllers), APIs REST, vistas, etc. Se comunica con la capa de Aplicación mediante interfaz de servicios.
- **Infraestructura (Frameworks & Drivers Layer)**: Contiene la implementación concreta de bases de datos, frameworks y herramientas externas. No debe contener lógica de negocio.

### 3. ¿Qué relación tiene Clean Architecture con el principio de Inversión de Dependencias (DIP) en SOLID?
Clean Architecture aplica el principio de Inversión de Dependencias (DIP) al estructurar el software de tal manera que:
- Las capas externas dependen de las internas, y no al revés.
- La lógica de negocio no depende de la infraestructura, sino de abstracciones.

### 4. ¿Por qué es importante desacoplar la lógica de negocio de la infraestructura en una aplicación?
Beneficios del desacoplamiento:
- **Flexibilidad**: Puedes cambiar de base de datos, framework o tecnología sin afectar la lógica de negocio.
- **Testabilidad**: La lógica de negocio puede probarse unitariamente sin depender de la base de datos.
- **Mantenibilidad**: Facilita la evolución del sistema sin afectar todas las capas.

Si la lógica de negocio está mezclada con la infraestructura (por ejemplo, consultas SQL en controladores), los cambios tecnológicos generan cascadas de refactorización.

### 5. ¿Cómo Clean Architecture facilita la escalabilidad y mantenibilidad de un sistema?
- **Escalabilidad**:
  - Se pueden agregar nuevas funcionalidades sin afectar el código existente.
  - Permite dividir la aplicación en módulos independientes.
  - Facilita balanceo de carga y distribución eficiente de procesos.
- **Mantenibilidad**:
  - El código está bien organizado y separado por responsabilidades.
  - Los cambios en una capa (ejemplo: cambiar de JPA a MongoDB) no afectan la lógica de negocio.
  - Facilita la reutilización del código.

### 6. ¿Qué diferencia hay entre la capa de dominio y la capa de aplicación en Clean Architecture?
- **Dominio**: Define las reglas del negocio mediante entidades, agregados y lógica inmutable.
- **Aplicación**: Orquesta los casos de uso y define la forma en que interactúan las entidades.

### 7. ¿Por qué los controladores (controllers) y la base de datos deben estar en la capa de infraestructura?
Porque son detalles de implementación y pueden cambiar sin afectar la lógica de negocio.
Ejemplo: Si un controlador está en la capa de Aplicación y se cambia de REST a GraphQL, toda la lógica del caso de uso podría verse afectada. En cambio, si está en la infraestructura, solo se cambia la forma en que se expone la API.

### 8. ¿Qué ventajas tiene usar una interfaz en la capa de dominio para definir repositorios en lugar de usar directamente JpaRepository?
Ventajas de definir interfaces en la capa de dominio:
- **Desacoplamiento**: La lógica de negocio no depende de la base de datos ni de JPA.
- **Flexibilidad**: Puedes cambiar de tecnología sin afectar los casos de uso.
- **Testabilidad**: Permite mockear repositorios en pruebas unitarias.

### 9. ¿Cómo interactúan los casos de uso (UseCases) con las entidades de dominio en Clean Architecture?
Los casos de uso (Capa de Aplicación) coordinan la ejecución de reglas de negocio sobre las entidades de dominio.

### 10. ¿Cómo se puede aplicar Clean Architecture en una aplicación de microservicios con Spring Boot?
- Dividir la aplicación en microservicios con Clean Architecture en cada uno.
- Cada microservicio tiene sus propias capas (Dominio, Aplicación, Infraestructura).
- Usar interfaces en la capa de Dominio para desacoplar la infraestructura.
- Comunicar microservicios mediante eventos o API REST sin exponer la lógica de negocio.
- Usar contenedores (Docker, Kubernetes) para desplegar cada microservicio independientemente.

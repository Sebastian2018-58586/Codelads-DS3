# codelab agregando Clean Architecture

## 1. ¿Qué es Attribute-Driven Design (ADD) y cuál es su propósito en el diseño de software?
Attribute-Driven Design (ADD) es un método de diseño arquitectónico basado en atributos de calidad. Su propósito es tomar decisiones arquitectónicas de manera estructurada, asegurando que el diseño cumpla con los requisitos del negocio y del sistema.

### ¿Qué resuelve ADD?
- Define la arquitectura en función de atributos de calidad como rendimiento, escalabilidad, seguridad y mantenibilidad.
- Facilita la toma de decisiones basadas en necesidades del negocio y restricciones tecnológicas.
- Reduce la incertidumbre en el diseño de software.

## 2. ¿Cómo se relaciona ADD con Clean Architecture en el proceso de diseño de sistemas?
ADD proporciona un enfoque basado en calidad para tomar decisiones arquitectónicas.
Clean Architecture estructura el código asegurando separación de responsabilidades.

### Relación clave:
- ADD define los atributos de calidad que la arquitectura debe cumplir.
- Clean Architecture ayuda a implementar esos atributos mediante la separación de capas y la inversión de dependencias.

## 3. ¿Cuáles son los pasos principales del método ADD para definir una arquitectura de software?
ADD sigue un enfoque iterativo basado en los siguientes pasos:

1. Identificar los requisitos del sistema (funcionales y atributos de calidad).
2. Seleccionar el módulo a diseñar (puede ser un microservicio, un componente o una capa).
3. Elegir tácticas arquitectónicas (como patrones de diseño o técnicas para mejorar atributos de calidad).
4. Definir la estructura del módulo (clases, interfaces, capas y relaciones).
5. Documentar las decisiones arquitectónicas (racionalidad detrás de cada elección).
6. Evaluar la arquitectura (mediante revisiones, prototipos o pruebas).

## 4. ¿Cómo se identifican los atributos de calidad en ADD y por qué son importantes?
Los atributos de calidad son criterios que definen el desempeño de la arquitectura.

### Ejemplo de atributos de calidad y cómo afectan el diseño:

| Atributo de calidad | Impacto en el diseño |
|--------------------|---------------------|
| **Rendimiento**   | Uso de caching, balanceo de carga |
| **Escalabilidad** | Microservicios, colas de mensajes |
| **Disponibilidad** | Replicación, failover, circuit breaker |
| **Seguridad**     | Encriptación, autenticación OAuth |
| **Mantenibilidad** | Separación de capas, Clean Architecture |

## 5. ¿Por qué Clean Architecture complementa ADD en la implementación de una solución?
- Clean Architecture implementa principios de diseño que ADD recomienda para mejorar atributos de calidad.
- ADD establece la estrategia, mientras que Clean Architecture define la estructura del código para cumplir con los atributos definidos.

## 6. ¿Qué criterios se deben considerar al definir las capas en Clean Architecture dentro de un proceso ADD?
Para definir las capas en Clean Architecture usando ADD, se deben considerar:

- Atributos de calidad del sistema (rendimiento, seguridad, etc.).
- Separación de responsabilidades (Evitar que la infraestructura afecte la lógica de negocio).
- Modularidad (Facilitar cambios en una capa sin afectar otras).
- Inversión de dependencias (Las capas internas no dependen de las externas).

## 7. ¿Cómo ADD ayuda a tomar decisiones arquitectónicas basadas en necesidades del negocio?
ADD traduce las necesidades del negocio en decisiones arquitectónicas concretas.

## 8. ¿Cuáles son los beneficios de combinar ADD con Clean Architecture en un sistema basado en microservicios?
### Ventajas clave:
- **Arquitectura basada en calidad**: ADD garantiza que se prioricen los atributos correctos.
- **Bajo acoplamiento**: Clean Architecture evita dependencias innecesarias entre microservicios.
- **Escalabilidad optimizada**: Se pueden desplegar microservicios de forma independiente.
- **Fácil mantenimiento**: Cada microservicio sigue una estructura clara y desacoplada.
- **Pruebas más eficientes**: Se pueden probar las capas internas sin necesidad de infraestructura real.

## 9. ¿Cómo se asegura que la arquitectura resultante cumpla con los atributos de calidad definidos en ADD?
- **Revisiones arquitectónicas periódicas** (Evaluar si se cumplen los atributos de calidad).
- **Pruebas de carga y estrés** (Para evaluar rendimiento y escalabilidad).
- **Prototipos y pruebas de concepto** (Validar decisiones antes de implementarlas a gran escala).
- **Revisiones de código** (Para verificar que Clean Architecture se siga correctamente).
- **Uso de métricas y monitoreo** (Tiempo de respuesta, consumo de recursos, etc.).

## 10. ¿Qué herramientas o metodologías pueden ayudar a validar una arquitectura diseñada con ADD y Clean Architecture?
### Herramientas y enfoques útiles:
- **SonarQube**: Para evaluar calidad del código y seguir principios de Clean Architecture.
- **Arquillian o JUnit**: Para pruebas unitarias y de integración.
- **JMeter o Gatling**: Para pruebas de carga y rendimiento.
- **Architectural Decision Records (ADR)**: Para documentar decisiones arquitectónicas.
- **C4 Model**: Para visualizar la arquitectura de forma clara.

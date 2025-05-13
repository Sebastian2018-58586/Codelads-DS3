# codelab sobre Attribute-Driven Design (ADD)

## 1. ¿Cuál es el propósito principal de la metodología ADD en el diseño de arquitecturas de software?
El propósito principal de Attribute-Driven Design (ADD) es guiar el diseño arquitectónico basándose en atributos de calidad y requisitos del sistema. ADD proporciona un enfoque estructurado para tomar decisiones arquitectónicas considerando trade-offs y asegurando que la arquitectura soporte los objetivos del negocio y las necesidades técnicas.

## 2. ¿Qué atributos de calidad se consideran en ADD y por qué son importantes en el proceso de diseño?
Los atributos de calidad son fundamentales en ADD porque determinan cómo el sistema debe comportarse más allá de sus funcionalidades básicas. Algunos de los más importantes son:
- **Rendimiento**: Asegura tiempos de respuesta adecuados.
- **Escalabilidad**: Permite que el sistema maneje más carga sin degradarse.
- **Mantenibilidad**: Facilita la evolución del software con menor costo.
- **Disponibilidad**: Garantiza que el sistema esté operativo cuando se necesita.
- **Seguridad**: Protege los datos y la integridad del sistema.

Estos atributos influyen directamente en las decisiones de diseño, como la elección de patrones arquitectónicos y tácticas.

## 3. Explica la importancia de la selección del módulo a diseñar en ADD. ¿Cuáles son los criterios principales para elegir un módulo?
En ADD, el diseño arquitectónico se realiza de manera incremental, por lo que la selección del módulo a diseñar es clave para gestionar la complejidad.

Los criterios principales para elegir un módulo incluyen:
- **Impacto en los atributos de calidad**: Se priorizan módulos críticos para el rendimiento, la seguridad o la escalabilidad.
- **Dependencias**: Se eligen módulos con muchas dependencias para definir interfaces clave antes que otros componentes los usen.
- **Riesgos**: Se diseñan primero los módulos más inciertos o desafiantes para mitigar riesgos tempranamente.
- **Requisitos del negocio**: Se priorizan módulos esenciales para cumplir con objetivos empresariales clave.

## 4. ¿Cómo influyen las tácticas arquitectónicas en la toma de decisiones dentro de ADD? Menciona dos ejemplos de tácticas y su aplicación.
Las tácticas arquitectónicas son estrategias específicas para alcanzar atributos de calidad en el diseño. En ADD, estas tácticas influyen en la forma en que se estructuran los módulos y los patrones arquitectónicos elegidos.

Ejemplos:
- **Caché (para rendimiento)**: Reducir el tiempo de respuesta almacenando datos en memoria en lugar de hacer consultas repetidas a la base de datos.
- **Circuit Breaker (para disponibilidad y resiliencia)**: Evitar fallas en cascada desconectando temporalmente servicios que están fallando.

Las tácticas ayudan a tomar decisiones fundamentadas y a diseñar una arquitectura que cumpla con los atributos de calidad requeridos.

## 5. ¿Cuál es la relación entre los escenarios de calidad y la evaluación de la arquitectura en ADD?
Los escenarios de calidad son descripciones específicas de cómo debe comportarse el sistema en ciertas condiciones. Estos escenarios se utilizan en ADD para:
- **Guiar decisiones de diseño** asegurando que la arquitectura cumpla los requisitos no funcionales.
- **Evaluar la arquitectura** mediante pruebas y simulaciones que validen que los atributos de calidad están siendo alcanzados.
- **Comparar alternativas arquitectónicas** en función de su capacidad para satisfacer estos escenarios.

## 6. Describe los principales pasos del proceso ADD y cómo se interrelacionan.
El proceso ADD sigue un flujo estructurado que se interconecta iterativamente:
1. **Identificar los requerimientos**: Se definen los atributos de calidad y escenarios clave.
2. **Seleccionar el módulo a diseñar**: Se prioriza el módulo más crítico según impacto, dependencias y riesgos.
3. **Elegir tácticas y patrones arquitectónicos**: Se aplican estrategias para cumplir con los atributos de calidad.
4. **Definir la estructura y los componentes**: Se crean módulos, interfaces y relaciones entre ellos.
5. **Evaluar la arquitectura**: Se validan las decisiones con escenarios de calidad y se ajusta el diseño si es necesario.
6. **Documentar las decisiones**: Se registran las opciones elegidas y las razones detrás de ellas para futuras referencias.

Cada iteración refina la arquitectura y asegura que se adapta a los requisitos en constante evolución.

## 7. ¿Por qué es crucial documentar las decisiones arquitectónicas en ADD? Menciona al menos tres elementos que deben incluirse en la documentación.
La documentación en ADD es esencial para:
- Mantener la trazabilidad de decisiones.
- Facilitar la comunicación entre equipos.
- Permitir la evolución del sistema con base en fundamentos claros.

Tres elementos clave que deben incluirse en la documentación:
1. **Motivación de las decisiones**: Explicación de por qué se eligió una solución sobre otra.
2. **Atributos de calidad abordados**: Cómo la decisión impacta en rendimiento, escalabilidad, seguridad, etc.
3. **Alternativas consideradas y trade-offs**: Opciones evaluadas y razones para descartar algunas.

## 8. En un proyecto real, ¿cómo se puede evaluar si una arquitectura diseñada con ADD cumple con los atributos de calidad esperados?
Para evaluar si una arquitectura cumple con los atributos de calidad esperados, se pueden utilizar los siguientes enfoques:
- **Pruebas de carga y rendimiento**: Validar tiempos de respuesta y capacidad de procesamiento.
- **Análisis de trade-offs (ATAM - Architecture Tradeoff Analysis Method)**: Evaluar el impacto de las decisiones arquitectónicas en diferentes atributos de calidad.
- **Prototipos y pruebas piloto**: Implementar versiones reducidas del sistema para evaluar su comportamiento en escenarios reales.
- **Simulación de fallos**: Evaluar la resiliencia aplicando pruebas de caos o de recuperación ante fallos.

## 9. ¿Cuáles son los beneficios de utilizar ADD en comparación con otros enfoques de diseño arquitectónico?
ADD ofrece ventajas significativas en el diseño arquitectónico:
- **Orientado a calidad**: Asegura que el sistema cumpla con atributos clave desde el inicio.
- **Decisiones estructuradas**: Reduce la incertidumbre al tomar decisiones informadas.
- **Iterativo y adaptable**: Permite ajustes progresivos sin bloquear el desarrollo.
- **Fomenta la documentación**: Mantiene un registro claro de por qué se tomaron ciertas decisiones.

En comparación con enfoques más tradicionales, ADD es más flexible y basado en evidencia, lo que lo hace ideal para sistemas complejos y en evolución.

## 10. ¿Qué desafíos pueden surgir al aplicar ADD en un equipo de desarrollo y cómo podrían abordarse?
Algunos desafíos comunes al aplicar ADD incluyen:
- **Falta de experiencia en atributos de calidad**  **Solución**: Capacitar al equipo en arquitectura de software y trade-offs.
- **Resistencia al proceso iterativo** **Solución**: Demostrar cómo los ciclos iterativos mejoran la calidad y reducen errores a largo plazo.
- **Complejidad en la documentación**  **Solución**: Usar herramientas colaborativas y plantillas estándar para documentar decisiones de forma eficiente.
- **Dificultad en la evaluación temprana de la arquitectura** 
 **Solución**: Implementar prototipos y simulaciones para validar decisiones antes del desarrollo completo.

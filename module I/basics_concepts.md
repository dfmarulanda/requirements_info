# Sesión 1: Conceptos básicos de gestión de requerimientos

## Objetivos de aprendizaje
- Comprender en profundidad los fundamentos de la ingeniería de requisitos
- Identificar y explicar la importancia de la gestión de requerimientos en el desarrollo de software
- Reconocer y aplicar los conceptos clave en la gestión de requerimientos
- Practicar la identificación y redacción de requerimientos a partir de descripciones detalladas de sistemas
- Comparar y contrastar el levantamiento de requerimientos en metodologías Waterfall y Agile

## Contenido teórico

### 1. Introducción a la ingeniería de requisitos

#### 1.1 Definición de ingeniería de requisitos
La ingeniería de requisitos es el proceso sistemático de desarrollar requisitos a través de un proceso iterativo y cooperativo de analizar el problema, documentar las observaciones resultantes en una variedad de formatos de representación, y verificar la precisión de la comprensión adquirida.

#### 1.2 Importancia en el ciclo de vida del desarrollo de software
- Establece la base para el diseño, implementación y pruebas: Los requisitos bien definidos guían todo el proceso de desarrollo.
- Reduce costos y tiempo de desarrollo: Identificar y corregir problemas en la fase de requisitos es mucho menos costoso que hacerlo más adelante.
- Mejora la calidad del producto final: Un entendimiento claro de los requisitos lleva a un producto que satisface mejor las necesidades del usuario.
- Aumenta la satisfacción del cliente: Asegura que el producto final cumpla con las expectativas del cliente.

#### 1.3 Relación con otras disciplinas de la ingeniería de software
- Diseño de software: Los requisitos informan directamente las decisiones de diseño.
- Gestión de proyectos: Los requisitos son la base para la planificación y estimación del proyecto.
- Aseguramiento de la calidad: Los requisitos son la base contra la cual se mide la calidad del software.
- Pruebas de software: Los casos de prueba se derivan de los requisitos.

### 2. Conceptos fundamentales

#### 2.1 Definición de requerimiento
Un requerimiento es una condición o capacidad que debe estar presente en un sistema o componentes de sistema para satisfacer un contrato, estándar, especificación u otro documento formalmente impuesto (IEEE 610.12-1990).

#### 2.2 Tipos de requerimientos

##### 2.2.1 Requerimientos funcionales
Describen lo que el sistema debe hacer, las funciones que el sistema debe realizar.

Ejemplo detallado:
RF1: Sistema de autenticación de usuarios
- El sistema debe permitir a los usuarios registrarse proporcionando un nombre de usuario único, dirección de correo electrónico y contraseña.
- La contraseña debe tener al menos 8 caracteres, incluyendo al menos una letra mayúscula, una letra minúscula, un número y un carácter especial.
- El sistema debe enviar un correo electrónico de verificación después del registro.
- Los usuarios deben poder iniciar sesión utilizando su nombre de usuario o correo electrónico y contraseña.
- El sistema debe proporcionar una función de "Olvidé mi contraseña" que envíe un enlace de restablecimiento al correo electrónico registrado.

##### 2.2.2 Requerimientos no funcionales
Describen cómo el sistema debe ser, especifican criterios para evaluar la operación del sistema.

Ejemplo detallado:
RNF1: Rendimiento del sistema
- El tiempo de respuesta para cualquier operación de búsqueda no debe exceder los 2 segundos bajo una carga de 1000 usuarios concurrentes.
- El sistema debe ser capaz de manejar al menos 10,000 transacciones por minuto.
- La interfaz de usuario debe cargarse completamente en menos de 3 segundos en una conexión de internet estándar (10 Mbps).
- El sistema debe tener un tiempo de actividad de al menos 99.9% (menos de 8.76 horas de inactividad por año).
- Las copias de seguridad de la base de datos deben completarse en menos de 1 hora sin afectar el rendimiento del sistema.

##### 2.2.3 Requerimientos de dominio
Reflejan características y restricciones del dominio de aplicación del sistema.

Ejemplo detallado:
RD1: Cumplimiento normativo para un sistema de gestión de salud
- El sistema debe cumplir con todas las regulaciones de la Ley de Portabilidad y Responsabilidad del Seguro Médico (HIPAA) de EE.UU.
- Toda la información de salud protegida (PHI) debe ser encriptada en reposo y en tránsito utilizando algoritmos aprobados por FIPS 140-2.
- El sistema debe mantener registros de auditoría detallados de todos los accesos y modificaciones a la PHI.
- Se debe implementar un mecanismo de cierre de sesión automático después de 15 minutos de inactividad.
- El sistema debe permitir a los pacientes acceder y descargar sus registros médicos en un formato legible por máquina, según lo requerido por la regla de Interoperabilidad y Acceso a la Información de Salud.

#### 2.3 Características de un buen requerimiento (SMART)
- Específico (Specific): Claro y no ambiguo
- Medible (Measurable): Se puede verificar su cumplimiento
- Alcanzable (Achievable): Realista y posible de implementar
- Relevante (Relevant): Alineado con los objetivos del proyecto
- Temporal (Time-bound): Con un plazo definido para su implementación

Ejemplo de un requerimiento SMART:
"El sistema debe ser capaz de procesar y confirmar un pedido en línea en menos de 30 segundos para el 95% de las transacciones, medido durante las horas pico de operación (de 18:00 a 22:00), y debe implementarse antes del lanzamiento de la versión 2.0 programada para el 15 de septiembre de 2023."

Este requerimiento es:
- Específico: Define claramente qué se debe lograr (procesar y confirmar un pedido).
- Medible: Establece un tiempo específico (menos de 30 segundos) y un porcentaje de cumplimiento (95%).
- Alcanzable: Es un objetivo realista para un sistema de comercio electrónico moderno.
- Relevante: Es importante para la eficiencia del sistema y la satisfacción del cliente.
- Temporal: Tiene una fecha límite clara (antes del lanzamiento de la versión 2.0 el 15 de septiembre de 2023).

### 3. Proceso de gestión de requerimientos

#### 3.1 Elicitación
Es el proceso de recolección de requerimientos de diversas fuentes. Incluye técnicas como:
- Entrevistas con stakeholders
- Cuestionarios
- Observación directa
- Análisis de documentos existentes
- Prototipos
- Talleres de requisitos

Ejemplo detallado de una sesión de elicitación:
Entrevista con el gerente de ventas para un nuevo CRM:

Entrevistador: "¿Cuáles son los principales desafíos que enfrenta actualmente con el seguimiento de clientes?"
Gerente de Ventas: "Nuestro mayor problema es que no tenemos una vista unificada del cliente. La información está dispersa en diferentes sistemas y es difícil obtener una imagen completa del historial y las interacciones del cliente."

Entrevistador: "Entiendo. ¿Puede describir cómo le gustaría que fuera el proceso ideal de seguimiento de clientes?"
Gerente de Ventas: "Me gustaría tener una dashboard que muestre toda la información relevante del cliente en una sola pantalla: historial de compras, interacciones recientes, oportunidades abiertas, y tal vez incluso una puntuación de 'salud' del cliente."

Entrevistador: "Eso suena útil. ¿Qué tipo de reportes o análisis le gustaría poder generar con este nuevo sistema?"
Gerente de Ventas: "Necesitamos poder ver tendencias de ventas por producto, región y representante de ventas. También sería genial tener predicciones de ventas basadas en datos históricos y actividades actuales."

[La entrevista continuaría con más preguntas para profundizar en los detalles]

#### 3.2 Análisis
Evaluación de requerimientos para asegurar que son claros, consistentes, completos y factibles. Incluye:
- Clasificación de requisitos
- Modelado conceptual
- Negociación y resolución de conflictos
- Priorización de requisitos

Ejemplo de análisis de un requerimiento:
Requerimiento original: "El sistema debe ser rápido"

Análisis:
1. Claridad: El requerimiento no es claro. "Rápido" es subjetivo y no medible.
2. Consistencia: No se puede evaluar la consistencia sin más contexto.
3. Completitud: Falta información sobre qué aspectos del sistema deben ser rápidos.
4. Factibilidad: No se puede determinar sin una definición más precisa.

Requerimiento mejorado después del análisis:
"El sistema debe responder a las consultas de los usuarios en menos de 2 segundos en el 95% de los casos, bajo una carga normal de hasta 1000 usuarios concurrentes."

#### 3.3 Especificación
Documentación formal de los requerimientos. Puede incluir:
- Documentos de Especificación de Requisitos de Software (SRS)
- Casos de uso
- Historias de usuario
- Modelos y diagramas (UML, flujos de proceso, etc.)

Ejemplo de una especificación formal en un SRS:

```
3.2.1 Búsqueda de productos
      
      3.2.1.1 El sistema deberá proporcionar una función de búsqueda de productos.
      
      3.2.1.2 La búsqueda deberá poder realizarse por los siguientes criterios:
              - Nombre del producto
              - Categoría
              - Precio (rango)
              - Marca
      
      3.2.1.3 Los resultados de la búsqueda deberán mostrarse en una lista ordenada
              por relevancia.
      
      3.2.1.4 La función de búsqueda deberá devolver resultados en menos de 
              3 segundos para el 99% de las búsquedas.
      
      3.2.1.5 El usuario deberá poder aplicar filtros adicionales a los resultados
              de la búsqueda.
```

#### 3.4 Validación
Confirmación de que los requerimientos representan con precisión las necesidades de los stakeholders. Incluye:
- Revisiones formales
- Prototipos
- Casos de prueba
- Validación mediante modelos

Ejemplo de un proceso de validación:
1. Crear un prototipo de la interfaz de usuario basado en los requisitos especificados.
2. Presentar el prototipo a un grupo de usuarios finales.
3. Pedir a los usuarios que realicen tareas específicas utilizando el prototipo.
4. Observar y registrar las dificultades o confusiones que experimentan los usuarios.
5. Realizar una sesión de retroalimentación para discutir la experiencia de los usuarios.
6. Revisar y ajustar los requisitos basándose en la retroalimentación recibida.

#### 3.5 Gestión de cambios
Proceso para manejar modificaciones en los requerimientos a lo largo del proyecto. Incluye:
- Seguimiento de requisitos
- Análisis de impacto
- Aprobación de cambios
- Actualización de documentación

Ejemplo de proceso de gestión de cambios:
1. Un stakeholder solicita un cambio: "Necesitamos agregar la opción de inicio de sesión con redes sociales".
2. Se crea una solicitud de cambio formal.
3. El equipo analiza el impacto del cambio:
   - Impacto en el cronograma: Se estima un retraso de 1 semana.
   - Impacto en el costo: Se necesitarán 40 horas adicionales de desarrollo.
   - Impacto técnico: Se deberán integrar APIs de redes sociales.
4. El comité de control de cambios revisa la solicitud y su análisis.
5. Si se aprueba, se actualiza el documento de requisitos, el plan del proyecto y se informa a todos los stakeholders relevantes.
6. El cambio se implementa y se verifica.

### 4. Roles y responsabilidades en la gestión de requerimientos

#### 4.1 Analista de requisitos
Responsabilidades:
- Elicitar requisitos de los stakeholders
- Analizar y documentar requisitos
- Facilitar la comunicación entre stakeholders y el equipo de desarrollo
- Validar requisitos con los stakeholders

#### 4.2 Stakeholders
Pueden incluir:
- Clientes
- Usuarios finales
- Gerentes de producto
- Expertos del dominio
Responsabilidades:
- Proporcionar información sobre necesidades y expectativas
- Revisar y aprobar requisitos
- Participar en sesiones de elicitación y validación

#### 4.3 Equipo de desarrollo
Responsabilidades:
- Revisar requisitos para asegurar la viabilidad técnica
- Proporcionar estimaciones de esfuerzo para la implementación de requisitos
- Implementar el sistema basado en los requisitos

#### 4.4 Gerente de proyecto
Responsabilidades:
- Asegurar que el proceso de gestión de requerimientos se integre efectivamente en el proyecto
- Gestionar los recursos necesarios para la elicitación y análisis de requisitos
- Facilitar la resolución de conflictos relacionados con los requisitos

## Cómo definir requerimientos: Ejemplo práctico extendido

Vamos a usar como ejemplo un sistema de gestión hospitalaria para mostrar cómo definir requerimientos.

Texto base del sistema:

"El Hospital Central necesita un sistema de gestión hospitalaria integral que mejore la eficiencia operativa y la calidad de atención al paciente. El sistema debe manejar múltiples aspectos de las operaciones hospitalarias, incluyendo la gestión de pacientes, programación de citas, gestión de recursos hospitalarios, y mantenimiento de registros médicos electrónicos.

Para la gestión de pacientes, el sistema debe permitir el registro de nuevos pacientes, actualización de información demográfica y médica, y seguimiento del historial de visitas y tratamientos. La programación de citas debe ser flexible, permitiendo a los pacientes programar, reprogramar o cancelar citas con diferentes departamentos y especialistas. También debe incluir un sistema de recordatorios automáticos por correoelectrónico y SMS.

En cuanto a la gestión de recursos hospitalarios, el sistema debe rastrear la disponibilidad de camas, quirófanos, y equipos médicos en tiempo real. Debe facilitar la asignación eficiente de estos recursos basándose en la urgencia de los casos y la disponibilidad del personal médico.

El componente de registros médicos electrónicos debe permitir a los médicos y enfermeras acceder y actualizar fácilmente los historiales médicos de los pacientes, incluyendo diagnósticos, prescripciones, alergias, y resultados de pruebas. El sistema debe integrarse con los equipos de laboratorio y diagnóstico para la actualización automática de resultados.

La seguridad y privacidad de los datos son cruciales. El sistema debe cumplir con todas las regulaciones de protección de datos de salud, incluyendo HIPAA en los Estados Unidos y GDPR en Europa. Debe incluir robustos controles de acceso basados en roles y un completo sistema de auditoría.

Además, el sistema debe proporcionar capacidades analíticas avanzadas, permitiendo a los administradores del hospital generar informes sobre métricas clave de rendimiento, tendencias de salud, y utilización de recursos. La interfaz de usuario debe ser intuitiva y responder rápidamente, accesible tanto desde estaciones de trabajo en el hospital como desde dispositivos móviles para el personal que se mueve por las instalaciones.

Finalmente, el sistema debe ser altamente confiable y estar disponible 24/7, con un tiempo de inactividad mínimo para mantenimiento. Debe ser escalable para acomodar el crecimiento futuro del hospital y tener la capacidad de integrarse con otros sistemas de salud para facilitar la continuidad de la atención entre diferentes proveedores de servicios de salud."

Paso 1: Identificar los actores principales
- Pacientes
- Médicos
- Enfermeras
- Personal administrativo
- Administradores del hospital
- Técnicos de laboratorio

Paso 2: Identificar las funcionalidades principales
- Gestión de pacientes
- Programación de citas
- Gestión de recursos hospitalarios
- Mantenimiento de registros médicos electrónicos
- Análisis y reportes
- Seguridad y privacidad de datos

Paso 3: Definir requerimientos funcionales

RF1: Registro y gestión de pacientes
- El sistema debe permitir el registro de nuevos pacientes con información demográfica completa.
- Debe permitir la actualización de información de pacientes existentes.
- Debe mantener un historial completo de visitas y tratamientos para cada paciente.

RF2: Programación de citas
- Los pacientes deben poder programar, reprogramar y cancelar citas en línea.
- El sistema debe enviar recordatorios automáticos por correo electrónico y SMS.
- Debe permitir la programación de citas con diferentes departamentos y especialistas.

RF3: Gestión de recursos hospitalarios
- El sistema debe rastrear en tiempo real la disponibilidad de camas, quirófanos y equipos médicos.
- Debe facilitar la asignación de recursos basada en la urgencia del caso y la disponibilidad del personal.

RF4: Registros médicos electrónicos
- Los médicos y enfermeras deben poder acceder y actualizar fácilmente los historiales médicos de los pacientes.
- El sistema debe integrarse con equipos de laboratorio para la actualización automática de resultados.
- Debe permitir el registro de diagnósticos, prescripciones y alergias.

RF5: Análisis y reportes
- El sistema debe generar informes sobre métricas clave de rendimiento, tendencias de salud y utilización de recursos.
- Debe proporcionar un dashboard personalizable para los administradores del hospital.

Paso 4: Definir requerimientos no funcionales

RNF1: Seguridad y privacidad
- El sistema debe cumplir con las regulaciones HIPAA y GDPR.
- Debe implementar controles de acceso basados en roles.
- Debe mantener un sistema completo de auditoría de accesos y cambios.

RNF2: Rendimiento y disponibilidad
- El sistema debe estar disponible 24/7 con un tiempo de inactividad planificado mínimo.
- Debe responder a las consultas en menos de 2 segundos bajo carga normal.

RNF3: Usabilidad
- La interfaz de usuario debe ser intuitiva y fácil de usar.
- Debe ser accesible desde estaciones de trabajo y dispositivos móviles.

RNF4: Escalabilidad e interoperabilidad
- El sistema debe ser escalable para acomodar el crecimiento futuro del hospital.
- Debe tener la capacidad de integrarse con otros sistemas de salud.

Paso 5: Definir requerimientos de dominio

RD1: Cumplimiento médico
- El sistema debe adherirse a los estándares de codificación médica ICD-10.
- Debe cumplir con las regulaciones locales de mantenimiento de registros médicos.

## Ejemplos de levantamiento de requerimientos: Waterfall vs Agile

### Enfoque Waterfall

En el enfoque Waterfall, el proceso de levantamiento de requerimientos se realiza al inicio del proyecto y se documenta exhaustivamente antes de pasar a las siguientes fases.

1. Recopilación de información:
   - Entrevistas extensas con el personal del hospital (médicos, enfermeras, administradores)
   - Revisión de procesos y flujos de trabajo existentes
   - Análisis de sistemas legados y su funcionalidad

2. Documentación detallada:
   - Documento de Especificación de Requisitos de Software (SRS)
   - Casos de uso detallados para cada funcionalidad
   - Diagramas de flujo para procesos clave

3. Ejemplo de requerimiento en formato Waterfall:
   
   REQ-001: Registro de Pacientes
   
   Descripción: El sistema debe permitir el registro de nuevos pacientes con la siguiente información:
   - Nombre completo
   - Fecha de nacimiento
   - Género
   - Dirección
   - Número de teléfono
   - Correo electrónico
   - Número de seguro médico
   - Contacto de emergencia
   
   Prioridad: Alta
   Fuente: Jefe de Admisiones
   
   Criterios de aceptación:
   - Todos los campos obligatorios deben ser validados antes de guardar el registro
   - El sistema debe generar un ID único para cada paciente
   - Los datos deben ser almacenados de forma segura y encriptada
   - El tiempo de registro no debe exceder los 2 minutos
   - El sistema debe verificar si el paciente ya existe para evitar duplicados
   
   Dependencias:
   - REQ-010: Sistema de base de datos de pacientes
   - REQ-015: Módulo de seguridad y encriptación
   
   Conflictos: Ninguno conocido
   
   Supuestos:
   - El hospital tiene un sistema de generación de IDs de paciente
   - Todos los usuarios del sistema tienen acceso a un ordenador con conexión a internet

4. Validación y aprobación:
   - Revisiones formales con stakeholders
   - Firma de documento de requerimientos por parte del cliente

### Enfoque Agile

En Agile, el levantamiento de requerimientos es un proceso continuo y colaborativo a lo largo del proyecto.

1. Product Backlog:
   - Lista priorizada de funcionalidades y requerimientos de alto nivel
   - Refinamiento continuo del backlog

2. User Stories:
   - Descripciones breves de funcionalidades desde la perspectiva del usuario

3. Ejemplo de User Story para el mismo requerimiento:

   Título: Registro de nuevo paciente
   
   Como recepcionista del hospital,
   Quiero poder registrar nuevos pacientes en el sistema,
   Para que podamos mantener un registro actualizado y preciso de todos los pacientes que atendemos.
   
   Criterios de aceptación:
   - Puedo ingresar la información básica del paciente (nombre, fecha de nacimiento, género, contacto)
   - El sistema genera un ID único para cada nuevo paciente
   - Recibo una advertencia si intento registrar un paciente que ya existe en el sistema
   - Recibo una confirmación cuando el registro se completa exitosamente
   - Puedo buscar y verificar la información del paciente después del registro
   - El proceso completo de registro no toma más de 2 minutos
   
   Notas técnicas:
   - Integrar con el sistema de generación de IDs de paciente existente
   - Asegurar que todos los datos se almacenen de forma encriptada
   
   Estimación: 5 puntos de historia

4. Refinamiento y planificación:
   - Sesiones de grooming para detallar y estimar user stories
   - Planificación de sprints para seleccionar stories a implementar

5. Desarrollo iterativo:
   - Implementación de stories en sprints cortos (típicamente 2 semanas)
   - Demostraciones regulares al Product Owner y stakeholders

6. Feedback y adaptación:
   - Revisiones de sprint para obtener feedback
   - Ajuste de prioridades y requerimientos basado en el feedback

## Actividad práctica: Identificación de requerimientos

Instrucciones: Lea atentamente la siguiente descripción de un sistema de comercio electrónico sostenible. Luego, identifique y liste los requerimientos funcionales, no funcionales y de dominio. Finalmente, escriba al menos 3 user stories para este sistema.

Descripción del sistema:

"GreenCart es una innovadora plataforma de comercio electrónico dedicada a productos sostenibles y ecológicos. La misión de GreenCart es facilitar a los consumidores la compra de productos que son buenos para el planeta, al tiempo que apoya a pequeños productores y artesanos comprometidos con prácticas sostenibles.

La plataforma debe ofrecer una amplia gama de productos, desde alimentos orgánicos y productos de cuidado personal naturales hasta ropa de materiales sostenibles y artículos para el hogar eco-amigables. Cada producto listado en GreenCart debe pasar por un riguroso proceso de verificación para asegurar que cumple con los estándares de sostenibilidad de la plataforma.

Los usuarios deben poder crear cuentas personales, buscar productos por categoría, características sostenibles (por ejemplo, vegano, zero waste, comercio justo), y localización del vendedor. El sistema de búsqueda debe ser intuitivo y ofrecer filtros avanzados para ayudar a los usuarios a encontrar exactamente lo que están buscando.

GreenCart debe incorporar un sistema de revisiones y calificaciones para que los compradores puedan compartir sus experiencias con productos y vendedores. Además, la plataforma debe incluir una sección educativa con artículos, videos y guías sobre estilos de vida sostenibles y el impacto ambiental de diferentes productos y prácticas de consumo.

Para los vendedores, GreenCart debe proporcionar herramientas fáciles de usar para listar productos, gestionar inventario, procesar pedidos y comunicarse con los clientes. La plataforma debe ofrecer análisis detallados de ventas y tendencias de mercado para ayudar a los vendedores a optimizar sus negocios.

La experiencia de compra debe ser fluida y segura, con múltiples opciones de pago, incluyendo métodos alternativos como criptomonedas. GreenCart debe implementar un sistema de logística inteligente que minimice la huella de carbono de los envíos, posiblemente asociándose con servicios de entrega locales y ecológicos.

La plataforma debe ser accesible a través de web y aplicaciones móviles, con una interfaz de usuario atractiva y fácil de usar que refleje los valores de sostenibilidad de la marca. El rendimiento del sistema debe ser óptimo, capaz de manejar picos de tráfico durante eventos de compra especiales o campañas de marketing.

GreenCart se compromete a la transparencia y debe proporcionar informes regulares sobre su propio impacto ambiental y social, así como métricas agregadas sobre cómo las compras en la plataforma contribuyen a diversos objetivos de sostenibilidad.

Finalmente, la seguridad y privacidad de los datos de usuarios y vendedores es primordial. El sistema debe cumplir con regulaciones de protección de datos como GDPR y emplear las mejores prácticas en seguridad de datos y prevención de fraudes."


## Evaluación formativa

1. Defina qué es un requerimiento y explique por qué es importante en el desarrollo de software.

2. Enumere y describa brevemente los tres principales tipos de requerimientos vistos en clase.

3. Explique las cinco etapas del proceso de gestión de requerimientos.

4. ¿Qué significa el acrónimo SMART en el contexto de los requerimientos y por qué es importante?

5. Identifique dos requerimientos funcionales y dos no funcionales para un sistema de comercio electrónico.

6. Compare y contraste el enfoque de levantamiento de requerimientos en metodologías Waterfall y Agile. ¿Cuáles son las ventajas y desventajas de cada enfoque?

7. Basándose en la descripción de GreenCart, escriba un requerimiento funcional en formato Waterfall y luego transfórmelo en una user story de Agile. Explique las diferencias en el enfoque.

## Recursos adicionales
- [Guía SWEBOK v3.0](https://www.computer.org/education/bodies-of-knowledge/software-engineering)
- [IEEE Recommended Practice for Software Requirements Specifications](https://standards.ieee.org/standard/830-1998.html)
- [Requirements Engineering: From System Goals to UML Models to Software Specifications](https://www.amazon.com/Requirements-Engineering-System-Software-Specifications/dp/0470012706) por Axel van Lamsweerde
- [Writing Effective Use Cases](https://www.amazon.com/Writing-Effective-Cases-Alistair-Cockburn/dp/0201702258) por Alistair Cockburn

## Tarea para la próxima sesión

1. Identificar y listar al menos 5 requerimientos funcionales y 3 no funcionales para un sistema de su elección (por ejemplo, una aplicación de entrega de comida, un sistema de reserva de citas médicas, etc.). Asegúrese de que los requerimientos cumplan con las características SMART.

2. Convertir 2 de los requerimientos funcionales que identificó en el punto anterior en user stories siguiendo el formato Agile.
# Sesión 3: Ciclo de vida de desarrollo de software (Versión Ampliada)

## Objetivos de aprendizaje
- Comprender en profundidad los diferentes modelos de ciclo de vida de desarrollo de software
- Identificar las fases principales del ciclo de vida y su relación con los requisitos
- Analizar las ventajas y desventajas de cada modelo con ejemplos concretos
- Desarrollar habilidades para seleccionar el modelo más apropiado según el contexto del proyecto
- Crear y justificar diagramas de ciclo de vida para proyectos hipotéticos variados

## Contenido teórico

### 1. Introducción al ciclo de vida de desarrollo de software (SDLC)

#### 1.1 Definición
El ciclo de vida de desarrollo de software (SDLC) es un proceso que define las fases y actividades involucradas en el desarrollo de un sistema de software, desde su concepción inicial hasta su despliegue y mantenimiento.

#### 1.2 Importancia del SDLC
- Proporciona una estructura y metodología para el desarrollo
- Facilita la planificación y el control del proyecto
- Mejora la calidad del software resultante
- Optimiza el uso de recursos y tiempo

Ejemplo: La NASA utiliza un SDLC riguroso para el desarrollo de software de misiones espaciales. En el caso de la misión Mars Rover, el SDLC incluyó fases extensas de pruebas y simulaciones para garantizar la fiabilidad del software en condiciones extremas.

### 2. Fases generales del SDLC

#### 2.1 Planificación y análisis de requisitos
- Definición del problema y objetivos del proyecto
- Recolección y documentación de requisitos
- Estudio de viabilidad

Ejemplo detallado: En el desarrollo de la aplicación de transporte Uber, esta fase implicó:
- Análisis del mercado de taxis y transporte urbano
- Entrevistas con conductores y pasajeros potenciales
- Estudio de viabilidad tecnológica (GPS en smartphones, mapeo en tiempo real)
- Definición de requisitos clave (emparejamiento conductor-pasajero, sistema de pago, calificaciones)

#### 2.2 Diseño
- Diseño de la arquitectura del sistema
- Diseño detallado de componentes y módulos
- Diseño de la interfaz de usuario

Ejemplo detallado: Para una aplicación bancaria móvil:
- Arquitectura: Sistema cliente-servidor con una capa de seguridad adicional
- Componentes: Módulo de autenticación, módulo de transacciones, módulo de informes
- UI: Diseño de pantallas para inicio de sesión, resumen de cuenta, transferencias, etc.

#### 2.3 Implementación (Codificación)
- Escritura del código fuente
- Integración de módulos y componentes

Ejemplo: En el desarrollo de un juego móvil como Pokémon GO:
- Implementación del motor de realidad aumentada
- Desarrollo de la lógica del juego (captura de Pokémon, combates)
- Integración con servidores para multijugador en tiempo real

#### 2.4 Pruebas
- Pruebas unitarias
- Pruebas de integración
- Pruebas de sistema
- Pruebas de aceptación

Ejemplo detallado: Para un sistema de comercio electrónico como Amazon:
- Pruebas unitarias: Verificar la función de cálculo de impuestos
- Pruebas de integración: Comprobar la interacción entre el carrito de compras y el sistema de pagos
- Pruebas de sistema: Simular un día de ventas masivas (como el Black Friday)
- Pruebas de aceptación: Betatesters realizan compras reales en un entorno controlado

#### 2.5 Despliegue
- Instalación del sistema en el entorno de producción
- Migración de datos (si es necesario)
- Capacitación de usuarios

Ejemplo: Lanzamiento de una nueva versión de un sistema ERP para una multinacional:
- Despliegue gradual por regiones
- Migración de datos históricos de ventas y clientes
- Sesiones de capacitación para empleados en diferentes zonas horarias

#### 2.6 Mantenimiento
- Corrección de errores
- Actualizaciones y mejoras
- Soporte técnico

Ejemplo: Mantenimiento continuo de un sistema operativo como Windows:
- Parches de seguridad mensuales
- Actualizaciones de características dos veces al año
- Soporte técnico para usuarios y empresas

### 3. Modelos de ciclo de vida de desarrollo de software

#### 3.1 Modelo en cascada
- Descripción: Enfoque lineal y secuencial
- Fases: Requisitos, Diseño, Implementación, Verificación, Mantenimiento

Ejemplo detallado: Desarrollo de software para un satélite de comunicaciones
- Requisitos: Especificaciones detalladas de rendimiento y durabilidad en el espacio
- Diseño: Arquitectura del sistema de comunicación, protocolos de transmisión
- Implementación: Codificación de algoritmos de procesamiento de señales
- Verificación: Pruebas exhaustivas en simuladores de condiciones espaciales
- Mantenimiento: Actualizaciones de software a través de enlaces de comunicación espacial

Ventajas: 
- Estructura clara y fácil de entender
- Adecuado para proyectos con requisitos bien definidos y estables
- Facilita la planificación y asignación de recursos

Desventajas:
- Inflexible a cambios
- Los resultados no se ven hasta etapas tardías
- Riesgo de no cumplir con las expectativas del cliente al final del proyecto

#### 3.2 Modelo en V
- Descripción: Extensión del modelo en cascada con énfasis en verificación y validación
- Fases: Requisitos, Diseño, Implementación (con fases de prueba correspondientes)

Ejemplo detallado: Desarrollo de software para un dispositivo médico de diagnóstico
- Requisitos y Planificación de Pruebas de Aceptación
- Diseño del Sistema y Planificación de Pruebas del Sistema
- Diseño de la Arquitectura y Planificación de Pruebas de Integración
- Diseño de Módulos y Planificación de Pruebas de Unidad
- Implementación
- Pruebas de Unidad
- Pruebas de Integración
- Pruebas del Sistema
- Pruebas de Aceptación

Ventajas:
- Énfasis en la verificación temprana
- Clara asociación entre fases de desarrollo y pruebas
- Adecuado para proyectos con altos requisitos de calidad y seguridad

Desventajas:
- Aún es relativamente inflexible a cambios
- Puede ser costoso y lento para proyectos grandes

#### 3.3 Modelo iterativo e incremental
- Descripción: Desarrollo en ciclos repetitivos, cada uno añadiendo funcionalidad
- Fases: Planificación, Requisitos, Diseño y Desarrollo, Pruebas (repetidas en cada iteración)

Ejemplo detallado: Desarrollo de una suite de productividad como Microsoft Office
- Iteración 1: Funcionalidades básicas de procesador de texto
- Iteración 2: Agregar hoja de cálculo básica
- Iteración 3: Incorporar presentaciones simples
- Iteración 4: Mejorar características avanzadas del procesador de texto
- Iteración 5: Añadir funciones avanzadas a la hoja de cálculo
- Y así sucesivamente...

Ventajas:
- Permite retroalimentación temprana
- Más flexible a cambios que los modelos lineales
- Los usuarios pueden ver resultados tangibles más rápidamente

Desventajas:
- Puede ser difícil determinar el número óptimo de iteraciones
- Requiere una gestión de proyecto más compleja

#### 3.4 Modelo en espiral
- Descripción: Combina elementos de diseño iterativo y modelo en cascada
- Fases: Planificación, Análisis de riesgos, Ingeniería, Evaluación (repetidas en espiral)

Ejemplo detallado: Desarrollo de un nuevo sistema operativo
- Ciclo 1: 
  - Planificación: Definir características básicas del kernel
  - Análisis de riesgos: Evaluar viabilidad y compatibilidad de hardware
  - Ingeniería: Desarrollar prototipo del kernel
  - Evaluación: Pruebas de rendimiento y estabilidad
- Ciclo 2:
  - Planificación: Definir interfaz de usuario y APIs básicas
  - Análisis de riesgos: Evaluar usabilidad y compatibilidad con software existente
  - Ingeniería: Desarrollar GUI y APIs fundamentales
  - Evaluación: Pruebas de usabilidad y compatibilidad
- Ciclos subsiguientes para características avanzadas, optimizaciones, etc.

Ventajas:
- Gestión de riesgos integrada
- Adecuado para proyectos grandes y complejos
- Permite la incorporación de prototipos

Desventajas:
- Puede ser costoso y complejo de implementar
- Requiere experiencia en evaluación de riesgos

#### 3.5 Modelo ágil
- Descripción: Enfoque iterativo e incremental con énfasis en la flexibilidad y colaboración
- Metodologías: Scrum, Extreme Programming (XP), Kanban

Ejemplo detallado: Desarrollo de una red social
Usando Scrum:
- Sprint 1: Implementar registro de usuarios y perfiles básicos
- Sprint 2: Desarrollar función de publicación de contenido y comentarios
- Sprint 3: Añadir sistema de amigos/seguidores
- Sprint 4: Implementar mensajería privada
- Sprints subsiguientes: Refinar características existentes y añadir nuevas basadas en feedback

Ventajas:
- Alta adaptabilidad a cambios
- Entrega continua de valor al cliente
- Fomenta la colaboración y comunicación constante

Desventajas:
- Puede ser desafiante en proyectos grandes o con equipos distribuidos
- Requiere compromiso y participación activa del cliente
- Puede llevar a una falta de énfasis en la documentación

### 4. Relación entre el SDLC y la gestión de requisitos

#### 4.1 Impacto de los requisitos en cada fase
- Planificación: Los requisitos iniciales guían la estimación y planificación del proyecto
- Diseño: Los requisitos detallados informan las decisiones de diseño
- Implementación: Los desarrolladores se basan en los requisitos para la codificación
- Pruebas: Los casos de prueba se derivan de los requisitos
- Mantenimiento: Los cambios en los requisitos impulsan las actualizaciones y mejoras

Ejemplo detallado: Desarrollo de un sistema de reservas de aerolíneas
- Planificación: Requisito de manejar 1000 reservas simultáneas influye en la elección de la infraestructura
- Diseño: Requisito de integración con múltiples aerolíneas define la arquitectura de APIs
- Implementación: Requisitos de búsqueda de vuelos guían el desarrollo de algoritmos de filtrado
- Pruebas: Se crean casos de prueba para verificar la capacidad de manejar 1000 reservas simultáneas
- Mantenimiento: Nuevo requisito de check-in móvil lleva a una actualización del sistema

#### 4.2 Gestión de cambios en los requisitos según el modelo SDLC
- Modelos tradicionales (Cascada, V): Cambios costosos y difíciles de implementar
- Modelos iterativos e incrementales: Más flexibles a cambios entre iteraciones
- Modelos ágiles: Altamente adaptables, con refinamiento continuo de requisitos

Ejemplo comparativo:
Requisito cambiante: "Añadir autenticación de dos factores"

En Cascada:
1. Detener el desarrollo
2. Volver a la fase de requisitos
3. Actualizar todos los documentos de diseño
4. Implementar el cambio
5. Actualizar todos los planes de prueba
Resultado: Retraso significativo y costos elevados

En Agile (Scrum):
1. Añadir el requisito al Product Backlog
2. Priorizar en la próxima sesión de planificación de sprint
3. Implementar en el siguiente sprint
4. Obtener feedback inmediato
Resultado: Cambio implementado rápidamente con mínima disrupción

## Actividad práctica: Creación de un diagrama de ciclo de vida

### Instrucciones
1. Divida la clase en grupos de 3-4 estudiantes
2. Cada grupo recibirá la descripción de uno de los cinco proyectos de software hipotéticos
3. Los grupos deben:
   - Analizar las características del proyecto
   - Seleccionar el modelo de SDLC más apropiado
   - Crear un diagrama visual del ciclo de vida elegido
   - Justificar su elección y explicar cómo manejarían los requisitos en cada fase

4. Cada grupo presentará su diagrama y justificación al resto de la clase

### Proyectos hipotéticos:

1. Sistema de Gestión de Emergencias
"Una ciudad mediana está buscando desarrollar un nuevo Sistema de Gestión de Emergencias (EMS) para coordinar la respuesta a diversos tipos de incidentes, desde accidentes de tráfico hasta desastres naturales. El sistema debe integrar datos de múltiples fuentes, incluidos servicios de policía, bomberos y atención médica de emergencia.

Requisitos clave:
- Interfaz de usuario intuitiva para despachadores
- Integración en tiempo real con sistemas GPS de vehículos de emergencia
- Capacidad para priorizar y asignar recursos basándose en la gravedad del incidente
- Generación de informes y análisis de datos para mejorar los tiempos de respuesta
- Alta disponibilidad y rendimiento, incluso en situaciones de crisis
- Cumplimiento con regulaciones de privacidad y seguridad de datos

El proyecto tiene un plazo de 18 meses para la implementación inicial, con expectativas de mejoras continuas después del lanzamiento. El presupuesto es limitado, y los stakeholders están abiertos a un enfoque de desarrollo que permita una entrega incremental de funcionalidades."

2. Plataforma de Aprendizaje en Línea
"Una startup educativa quiere crear una plataforma de aprendizaje en línea innovadora que ofrezca cursos personalizados utilizando inteligencia artificial. La plataforma debe adaptarse al ritmo y estilo de aprendizaje de cada estudiante, ofrecer una variedad de formatos de contenido (video, texto, interactivo) y proporcionar análisis detallados del progreso del estudiante.

Requisitos clave2. Plataforma de Aprendizaje en Línea (continuación)

Requisitos clave:
- Algoritmo de IA para personalizar rutas de aprendizaje
- Interfaz de usuario adaptable a diferentes dispositivos (responsive design)
- Sistema de creación de contenido para instructores
- Integración con plataformas de videoconferencia para clases en vivo
- Gamificación para aumentar el compromiso del estudiante
- Análisis de datos de aprendizaje en tiempo real

El equipo de desarrollo es pequeño pero altamente calificado, y la startup quiere lanzar un MVP (Producto Mínimo Viable) en 6 meses para atraer inversores. Se espera un desarrollo continuo y rápido después del lanzamiento inicial basado en el feedback de los usuarios."

3. Sistema de Control de Tráfico Inteligente
"Una gran ciudad busca implementar un Sistema de Control de Tráfico Inteligente para reducir la congestión y mejorar la seguridad vial. El sistema debe utilizar datos en tiempo real de cámaras de tráfico, sensores en las calles y vehículos conectados para optimizar los semáforos y el flujo de tráfico.

Requisitos clave:
- Algoritmos de optimización de tráfico en tiempo real
- Integración con sistemas existentes de semáforos y cámaras
- Interfaz para operadores de tráfico con visualizaciones en tiempo real
- Capacidad de simulación para planificación urbana
- API para compartir datos con aplicaciones de navegación de terceros
- Sistema de alerta temprana para incidentes de tráfico
- Cumplimiento con estándares de smart cities y protección de datos

El proyecto es de alta visibilidad política y tiene un presupuesto considerable. Se espera que se implemente en fases durante un período de 3 años, comenzando con un piloto en el centro de la ciudad."

4. Aplicación de Salud y Bienestar Personalizada
"Una compañía de seguros de salud quiere desarrollar una aplicación móvil de salud y bienestar para sus asegurados. La aplicación debe proporcionar recomendaciones personalizadas de salud, seguimiento de actividad física, recordatorios de medicación, y debe integrarse con dispositivos wearables y registros médicos electrónicos.

Requisitos clave:
- Integración con diversos dispositivos wearables (fitbits, smartwatches, etc.)
- Algoritmos de IA para proporcionar recomendaciones de salud personalizadas
- Seguimiento de medicación con recordatorios inteligentes
- Conexión segura con sistemas de registros médicos electrónicos
- Gamificación para fomentar hábitos saludables
- Chatbot para consultas de salud básicas
- Estricto cumplimiento de HIPAA y otras regulaciones de privacidad de datos de salud

La compañía quiere un enfoque de desarrollo que permita lanzamientos frecuentes y la incorporación rápida de feedback de los usuarios. El plazo inicial para el lanzamiento de la primera versión es de 9 meses."

5. Sistema de Automatización de Almacén Robotizado
"Una gran empresa de comercio electrónico está buscando desarrollar un sistema de software para controlar un nuevo almacén totalmente automatizado con robots. El sistema debe gestionar el inventario, coordinar los movimientos de los robots, optimizar el almacenamiento y la recuperación de productos, e integrarse con los sistemas existentes de gestión de pedidos y envíos.

Requisitos clave:
- Algoritmos de optimización para el movimiento de robots y gestión de inventario
- Sistema de control en tiempo real para coordinar múltiples robots
- Integración con sistemas de escaneo y RFID para seguimiento de inventario
- Interfaz de usuario para supervisión y control manual cuando sea necesario
- Sistemas de seguridad y redundancia para prevenir fallos críticos
- Análisis predictivo para mantenimiento de robots y gestión de inventario
- Escalabilidad para manejar picos de demanda estacionales

El proyecto es crítico para el negocio y tiene un alto nivel de complejidad técnica. La empresa espera que el sistema esté completamente operativo en 2 años, pero quiere ver resultados incrementales a lo largo del desarrollo."

### Guía para el análisis

Para cada proyecto, considere los siguientes aspectos al seleccionar y justificar el modelo de SDLC:

1. Complejidad del proyecto
2. Claridad y estabilidad de los requisitos
3. Participación del cliente/usuario
4. Duración del proyecto y plazos
5. Necesidad de resultados tempranos
6. Flexibilidad para cambios
7. Riesgos del proyecto
8. Equipo de desarrollo (tamaño, experiencia, distribución)
9. Restricciones regulatorias o de cumplimiento


## Evaluación formativa

Al final de la sesión, realice un breve cuestionario para evaluar la comprensión de los conceptos clave:

1. Enumere las fases generales del ciclo de vida de desarrollo de software.

2. ¿Cuáles son las principales diferencias entre el modelo en cascada y el modelo ágil?

3. ¿En qué situaciones sería más apropiado utilizar un modelo en espiral?

4. ¿Cómo impactan los requisitos en la fase de diseño del SDLC?

5. Describa una ventaja y una desventaja del modelo iterativo e incremental.

6. ¿Por qué es importante seleccionar el modelo de SDLC adecuado para un proyecto?

7. En el contexto del proyecto de Sistema de Gestión de Emergencias, ¿qué desafíos específicos de gestión de requisitos anticiparía?

## Recursos adicionales
- [Software Development Life Cycle (SDLC): A Complete Guide](https://www.guru99.com/software-development-life-cycle-tutorial.html)
- [Comparing Different SDLC Models](https://www.geeksforgeeks.org/software-engineering-sdlc-models/)
- [Agile Practice Guide](https://www.pmi.org/pmbok-guide-standards/practice-guides/agile) por Project Management Institute
- [Software Engineering: A Practitioner's Approach](https://www.amazon.com/Software-Engineering-Practitioners-Roger-Pressman/dp/0078022126) por Roger S. Pressman y Bruce Maxim

## Tarea para la próxima sesión
1. Investigar y escribir un breve informe (2-3 páginas) sobre un caso real de una empresa que haya cambiado su modelo de SDLC (por ejemplo, de cascada a ágil). Incluir los motivos del cambio, los desafíos enfrentados y los resultados obtenidos.

2. Crear un diagrama comparativo de cómo se manejan los requisitos en tres diferentes modelos de SDLC de su elección. Incluir ventajas y desventajas de cada enfoque.

3. Reflexionar sobre el proyecto hipotético del Sistema de Gestión de Emergencias y escribir un párrafo sobre cómo adaptaría la gestión de requisitos si, a mitad del proyecto, surgiera la necesidad de integrar el sistema con una nueva red de sensores IoT para detección temprana de incendios forestales.
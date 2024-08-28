# Clase 5: Diagramas de Procesos y Mapeo de Experiencia del Usuario

## Objetivos de Aprendizaje

Al finalizar esta clase, los estudiantes serán capaces de:
1. Crear y analizar diagramas de procesos complejos en el contexto del desarrollo de software.
2. Aplicar técnicas avanzadas de mapeo de experiencia del usuario para identificar requisitos centrados en el usuario.
3. Integrar diagramas de procesos con mapas de experiencia del usuario para una comprensión holística de los requisitos.
4. Derivar requisitos funcionales y no funcionales detallados utilizando ambas técnicas.

## 1. Introducción (10 minutos)

- Bienvenida y visión general de la clase
- Repaso rápido de conceptos previos sobre levantamiento de requisitos
- Explicación de la importancia de combinar perspectivas técnicas y centradas en el usuario

## 2. Diagramas de Procesos (90 minutos)

### 2.1 Fundamentos y Tipos de Diagramas de Procesos (20 minutos)

#### Definición
Un diagrama de procesos es una representación gráfica de la secuencia de actividades y decisiones en un proceso de negocio o sistema.

#### Tipos de Diagramas de Procesos
1. Diagramas de flujo básicos
2. Diagramas de flujo funcionales cruzados (cross-functional)
3. Diagramas de flujo de datos
4. Diagramas BPMN (Business Process Model and Notation)

#### Elementos Básicos y Avanzados
- Inicio/Fin: Óvalos
- Actividades: Rectángulos
- Decisiones: Diamantes
- Flujos: Flechas
- Subprocesos: Rectángulos con un símbolo '+'
- Eventos intermedios: Círculos
- Compuertas lógicas: Diamantes con símbolos internos
- Pools y lanes: Para representar responsabilidades organizacionales
- Artefactos: Objetos de datos, anotaciones

### 2.2 Ejemplo Detallado: Sistema de Gestión de Incidencias (30 minutos)

Vamos a crear un diagrama de procesos para un sistema de gestión de incidencias en una empresa de software.

```
[Inicio] → (Usuario reporta incidencia)
↓
(Sistema registra incidencia) → (Asignar prioridad automática)
↓
<¿Prioridad alta?>
  → Sí → (Notificar a equipo de soporte urgente)
  → No → (Colocar en cola de incidencias)
↓
(Analista revisa incidencia)
↓
<¿Requiere más información?>
  → Sí → (Solicitar información al usuario) → [Esperar respuesta] → (Usuario proporciona información) → [Volver a "Analista revisa incidencia"]
  → No → (Asignar a desarrollador)
↓
(Desarrollador trabaja en solución)
↓
(Desarrollador aplica fix)
↓
(Tester verifica solución)
↓
<¿Solución efectiva?>
  → No → [Volver a "Desarrollador trabaja en solución"]
  → Sí → (Actualizar estado a resuelto)
↓
(Notificar al usuario)
↓
<¿Usuario confirma resolución?>
  → No → (Reabrir incidencia) → [Volver a "Analista revisa incidencia"]
  → Sí → (Cerrar incidencia)
↓
(Actualizar base de conocimientos)
↓
[Fin]
```

#### Análisis del Diagrama
1. Identificación de roles: Usuario, Sistema, Analista, Desarrollador, Tester
2. Puntos de decisión clave: Prioridad, necesidad de más información, efectividad de la solución, confirmación del usuario
3. Bucles potenciales: Solicitud de más información, retrabajos en desarrollo, reapertura de incidencias

### 2.3 Técnicas de Análisis de Procesos (20 minutos)

1. Análisis de valor agregado
   - Identificar pasos que añaden valor directo al usuario
   - Ejemplo: La notificación automática al equipo de soporte para incidencias de alta prioridad agrega valor al reducir tiempos de respuesta

2. Análisis de cuellos de botella
   - Identificar pasos que ralentizan el proceso
   - Ejemplo: La espera de información adicional del usuario podría ser un cuello de botella

3. Análisis de redundancias
   - Identificar pasos repetitivos o innecesarios
   - Ejemplo: Multiple revisiones por diferentes roles podrían ser redundantes en algunos casos

4. Análisis de excepciones
   - Identificar y manejar casos atípicos
   - Ejemplo: Proceso para manejar incidencias que no se pueden resolver y requieren escalación

### 2.4 Derivación de Requisitos a partir de Diagramas de Procesos (20 minutos)

Basándonos en el diagrama de gestión de incidencias, podemos derivar los siguientes requisitos:

1. Requisitos funcionales
   - El sistema debe permitir a los usuarios reportar incidencias
   - El sistema debe asignar automáticamente una prioridad a cada incidencia
   - El sistema debe notificar al equipo de soporte urgente para incidencias de alta prioridad
   - El sistema debe permitir a los analistas solicitar información adicional a los usuarios
   - El sistema debe permitir a los desarrolladores marcar una incidencia como resuelta
   - El sistema debe permitir a los usuarios confirmar la resolución de una incidencia

2. Requisitos de datos
   - El sistema debe almacenar la siguiente información para cada incidencia: ID, descripción, prioridad, estado, fecha de reporte, fecha de resolución
   - El sistema debe mantener un historial de cambios de estado de cada incidencia

3. Requisitos de interfaz
   - La interfaz de usuario debe mostrar claramente el estado actual de cada incidencia
   - Debe haber una interfaz para que los desarrolladores actualicen el progreso de la resolución

4. Requisitos de seguridad
   - Solo los usuarios autorizados deben poder cambiar el estado de una incidencia
   - Debe haber un registro de auditoría de todas las acciones realizadas en una incidencia

5. Requisitos de rendimiento
   - El sistema debe ser capaz de manejar al menos 1000 incidencias activas simultáneamente
   - La asignación automática de prioridad debe completarse en menos de 5 segundos

## 3. Mapeo de Experiencia del Usuario (90 minutos)

### 3.1 Fundamentos del Mapeo de Experiencia del Usuario (20 minutos)

#### Definición
Un mapa de experiencia del usuario es una visualización del proceso que una persona atraviesa para lograr un objetivo con un producto o servicio, capturando sus acciones, pensamientos y emociones.

#### Componentes clave
1. Persona: Descripción del usuario tipo
2. Fases del Viaje: Etapas principales del proceso
3. Acciones: Pasos específicos que el usuario realiza
4. Pensamientos: Lo que el usuario piensa en cada etapa
5. Emociones: Estado emocional del usuario
6. Puntos de Contacto: Interacciones con la marca/producto
7. Oportunidades: Áreas de mejora identificadas

### 3.2 Ejemplo Detallado: Experiencia de Compra en una Tienda de Electrónicos Online (30 minutos)

Persona: Alex, 28 años, profesional de TI, busca actualizar su laptop

#### Fase 1: Descubrimiento
- **Acciones:**
  - Busca en Google "mejores laptops para programadores 2024"
  - Ve reseñas en YouTube de modelos populares
- **Pensamientos:**
  - "Necesito algo potente pero portátil"
  - "¿Qué marcas son confiables?"
- **Emociones:** Entusiasmo, ligera ansiedad
- **Puntos de Contacto:** Motor de búsqueda, YouTube, blogs de tecnología
- **Oportunidades:** Crear contenido específico para programadores

#### Fase 2: Investigación
- **Acciones:**
  - Compara especificaciones en el sitio web de la tienda
  - Lee reseñas de usuarios
- **Pensamientos:**
  - "¿Este modelo tendrá suficiente RAM?"
  - "Me pregunto si la batería durará todo el día"
- **Emociones:** Concentración, algo abrumado por las opciones
- **Puntos de Contacto:** Sitio web de la tienda, sección de reseñas
- **Oportunidades:** Mejorar la herramienta de comparación de productos

#### Fase 3: Decisión
- **Acciones:**
  - Agrega laptop al carrito
  - Busca códigos de descuento online
- **Pensamientos:**
  - "Espero que sea la elección correcta"
  - "¿Debería esperar a una oferta mejor?"
- **Emociones:** Excitación, duda de último minuto
- **Puntos de Contacto:** Página de producto, carrito de compras
- **Oportunidades:** Ofrecer garantía de igualación de precios

#### Fase 4: Compra
- **Acciones:**
  - Ingresa información de envío y pago
  - Completa la compra
- **Pensamientos:**
  - "Espero que el proceso sea seguro"
  - "¿Cuándo llegará mi laptop?"
- **Emociones:** Ansiedad por la transacción, alivio al completar
- **Puntos de Contacto:** Página de checkout, confirmación de pedido
- **Oportunidades:** Simplificar el proceso de checkout, ofrecer opciones de envío más claras

#### Fase 5: Espera y Recepción
- **Acciones:**
  - Revisa el estado del pedido diariamente
  - Recibe y desempaca la laptop
- **Pensamientos:**
  - "Espero que llegue a tiempo y en buenas condiciones"
  - "¿Será fácil de configurar?"
- **Emociones:** Impaciencia, emoción al recibir
- **Puntos de Contacto:** Página de seguimiento, email de actualización, paquete físico
- **Oportunidades:** Proporcionar actualizaciones de envío más frecuentes, incluir guía de inicio rápido

#### Fase 6: Uso Inicial
- **Acciones:**
  - Configura la laptop
  - Prueba las funciones principales
- **Pensamientos:**
  - "¿Hice la elección correcta?"
  - "¿Cómo transfiero mis archivos viejos?"
- **Emociones:** Satisfacción si todo funciona bien, frustración si hay problemas
- **Puntos de Contacto:** Producto físico, software preinstalado, manual de usuario
- **Oportunidades:** Ofrecer servicio de migración de datos, mejorar el tutorial de bienvenida

#### Fase 7: Soporte Post-Compra
- **Acciones:**
  - Registra el producto para la garantía
  - Explora recursos de soporte online
- **Pensamientos:**
  - "¿Qué hago si algo sale mal?"
  - "¿Valdrá la pena comprar una garantía extendida?"
- **Emociones:** Tranquilidad si el soporte parece bueno, preocupación si no
- **Puntos de Contacto:** Página de registro de producto, sección de soporte del sitio web
- **Oportunidades:** Simplificar el proceso de registro, ofrecer chat en vivo para soporte

### 3.3 Análisis del Mapa de Experiencia (20 minutos)

1. Análisis de puntos de dolor
   - Ejemplo: Frustración durante la comparación de especificaciones técnicas
   - Solución potencial: Desarrollar una herramienta de comparación más intuitiva

2. Análisis de momentos de verdad
   - Ejemplo: El momento de completar la compra es crítico
   - Mejora: Garantizar un proceso de checkout fluido y ofrecer múltiples opciones de pago seguras

3. Análisis de brechas
   - Ejemplo: Brecha entre la expectativa de una configuración fácil y la realidad potencialmente compleja
   - Solución: Proporcionar una guía de configuración paso a paso y ofrecer asistencia remota

4. Análisis de emociones
   - Identificar picos emocionales: Emoción al desempacar, potencial frustración en la configuración
   - Estrategia: Mejorar la experiencia de unboxing y simplificar el proceso de configuración inicial

### 3.4 Derivación de Requisitos del Mapa de Experiencia (20 minutos)

1. Requisitos funcionales
   - El sitio web debe incluir una herramienta de comparación side-by-side de hasta 3 productos
   - Implementar un sistema de búsqueda y filtrado avanzado por especificaciones técnicas
   - Desarrollar un sistema de seguimiento de pedidos en tiempo real con notificaciones push

2. Requisitos no funcionales
   - El tiempo de carga de la página de producto no debe exceder los 2 segundos
   - El proceso de checkout debe completarse en no más de 3 pasos
   - La plataforma debe ser capaz de manejar al menos 10,000 usuarios concurrentes durante eventos de ventas

3. Requisitos de experiencia de usuario
   - Diseñar un tutorial interactivo para la configuración inicial de la laptop
   - Implementar un chatbot de soporte disponible 24/7 para resolver dudas comunes
   - Crear una sección de "Preguntas Frecuentes" específica para cada modelo de laptop

4. Requisitos de contenido
   - Cada página de producto debe incluir un video de demostración de menos de 2 minutos
   - Proporcionar guías de usuario descargables en formato PDF para cada producto
   - Mantener una base de conocimientos actualizada con soluciones a problemas comunes

## 4. Integración de Diagramas de Procesos y Mapas de Experiencia (30 minutos)

### 4.1 Caso de Estudio: Mejora del Proceso de Devolución

Vamos a combinar un diagrama de procesos para devoluciones con insights del mapa de experiencia del usuario.

#### Diagrama de Procesos de Devolución

```
[Inicio] → (Usuario solicita devolución)
↓
(Sistema verifica elegibilidad)
↓
<¿Producto elegible?>
  → No → (Notificar al usuario) → [Fin]
  → Sí → (Generar etiqueta de devolución)
↓
(Enviar instrucciones al usuario)
↓
(Usuario envía producto)
↓
(Almacén(Almacén recibe producto)
↓
(Inspección de producto)
↓
<¿Producto en buen estado?>
  → No → (Notificar al usuario) → [Fin]
  → Sí → (Procesar reembolso)
↓
(Notificar al usuario sobre reembolso)
↓
[Fin]
```

#### Insights del Mapa de Experiencia

- Los usuarios sienten ansiedad sobre el estado de su devolución
- La espera del reembolso genera frustración
- Los usuarios valoran la transparencia en el proceso

### 4.2 Diagrama de Procesos Mejorado

```
[Inicio] → (Usuario solicita devolución en portal online)
↓
(Sistema verifica elegibilidad en tiempo real)
↓
<¿Producto elegible?>
  → No → (Mostrar razones de no elegibilidad) → (Ofrecer alternativas) → [Fin]
  → Sí → (Generar etiqueta de devolución QR)
↓
(Enviar instrucciones detalladas por email y SMS)
↓
(Usuario envía producto)
↓
(Sistema actualiza estado a "En tránsito")
↓
(Almacén recibe producto)
↓
(Sistema actualiza estado a "Recibido")
↓
(Inspección rápida de producto)
↓
<¿Producto en buen estado?>
  → No → (Notificar al usuario con fotos) → (Ofrecer opciones: reenvío o descuento) → [Esperar decisión]
  → Sí → (Iniciar proceso de reembolso)
↓
(Sistema inicia reembolso automático)
↓
(Notificar al usuario sobre inicio de reembolso)
↓
<¿Reembolso completado?>
  → No → (Sistema verifica diariamente) → [Volver a verificación]
  → Sí → (Notificar al usuario)
↓
(Solicitar feedback sobre el proceso)
↓
[Fin]
```

### 4.3 Análisis de la Integración

1. Puntos de mejora identificados:
   - Verificación de elegibilidad en tiempo real para reducir ansiedad
   - Actualizaciones de estado más frecuentes y detalladas
   - Proceso de reembolso más rápido y transparente
   - Opciones claras en caso de problemas con la devolución

2. Beneficios de la integración:
   - Mayor satisfacción del usuario al abordar puntos de dolor emocionales
   - Proceso más eficiente al eliminar pasos innecesarios
   - Mejor comunicación en cada etapa del proceso

### 4.4 Requisitos Derivados de la Integración

1. Requisitos funcionales:
   - Implementar un sistema de verificación de elegibilidad en tiempo real
   - Desarrollar un sistema de generación de etiquetas QR para devoluciones
   - Crear un sistema de notificaciones multicanal (email, SMS, push)
   - Implementar un proceso de reembolso automático

2. Requisitos no funcionales:
   - El tiempo de respuesta para la verificación de elegibilidad debe ser inferior a 3 segundos
   - El sistema debe ser capaz de manejar al menos 1000 solicitudes de devolución simultáneas
   - La tasa de error en la generación de etiquetas QR debe ser inferior al 0.1%

3. Requisitos de experiencia de usuario:
   - Diseñar una interfaz de usuario intuitiva para el proceso de solicitud de devolución
   - Crear un panel de seguimiento de devoluciones en tiempo real para los usuarios
   - Implementar un sistema de retroalimentación post-devolución

4. Requisitos de integración:
   - Integrar el sistema de devoluciones con el sistema de gestión de inventario
   - Conectar el proceso de reembolso con el sistema de pagos existente
   - Sincronizar las actualizaciones de estado con el sistema de notificaciones

## 5. Conclusión y Próximos Pasos (10 minutos)

- Recapitulación de los conceptos clave aprendidos
- Discusión sobre cómo estos métodos mejoran el proceso de levantamiento de requisitos
- Asignación de tarea: Crear un diagrama de procesos y un mapa de experiencia de usuario para un sistema de su elección, e integrarlos para derivar requisitos

## 6. Recursos Adicionales

- "Business Process Modeling, Simulation and Design" por Manuel Laguna y Johan Marklund
- "Mapping Experiences: A Complete Guide to Creating Value through Journeys, Blueprints, and Diagrams" por James Kalbach
- Herramientas recomendadas:
  - Draw.io para diagramas de procesos
  - Miro para mapas de experiencia de usuario
  - Lucidchart para ambos tipos de diagramas

---

Esta clase proporciona una base sólida para la creación y análisis de diagramas de procesos y mapas de experiencia del usuario, así como su integración para una comprensión más profunda de los requisitos del sistema. Los estudiantes ahora deberían ser capaces de aplicar estas técnicas en sus propios proyectos de desarrollo de software, mejorando así la calidad y la relevancia de los requisitos que identifican.
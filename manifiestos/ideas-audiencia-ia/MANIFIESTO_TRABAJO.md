# Sistema replicable de propuestas de audiencia asistido por IA

## Objetivo y motivo

Crear un kit replicable, con una implementación funcional de referencia, que permita a un creador de contenido recibir propuestas de su audiencia, evaluarlas según sus objetivos, profundizar las seleccionadas y someter finalistas a participación pública. El propósito es facilitar una comunicación útil entre creadores y audiencias y permitir que otras personas repliquen el sistema; la monetización del kit no es su objetivo.

El creador debe poder configurar y operar el sistema con ayuda de la IA que ya utiliza, sin necesitar conocimientos técnicos previos. La referencia inicial será ChatGPT; la compatibilidad de operación con otras IA solo se afirmará cuando exista evidencia de ella.

## Resultado observable

Entregar código, instrucciones, configuración de ejemplo y una implementación que demuestre el circuito completo con datos de prueba. Un enlace de entrada debe permitir que el creador entregue las instrucciones a su IA y reciba acompañamiento adaptado a sus conocimientos, herramientas y permisos.

La operación habitual debe poder iniciarse mediante una petición breve del creador a su IA, con acceso autorizado a las propuestas y devolución de resultados al sistema. La transferencia manual repetitiva de archivos no constituye el resultado objetivo. Deben documentarse las acciones que requieran intervención humana y las capacidades efectivamente disponibles en la integración probada.

La audiencia debe disponer de un enlace comprensible tanto directamente como a través de su propia IA. Usar IA para participar será opcional.

## Alcance funcional

### Definición de criterios

La IA ayuda al creador a expresar un perfil habitual: temáticas, público, objetivos, preferencias y límites. Cada convocatoria agrega una pregunta concreta, restricciones y criterios de selección propios.

Antes de abrirla, el creador revisa una interpretación de sus criterios y ejemplos de selección explicados. La calibración debe permitir corregir discrepancias. Los criterios se conservan para esa convocatoria; si cambian durante la evaluación, todas sus propuestas deben reevaluarse bajo el mismo criterio.

### Recepción y participación

El sistema contempla recepción permanente con cortes de evaluación y convocatorias delimitadas. El formulario breve será la entrada principal. Pedirá qué se propone, por qué aporta y un ejemplo o detalle suficiente para entenderlo. Los límites de extensión deben justificarse y probarse sin exigir una elaboración extensa para participar.

La guía pública explicará objetivo, criterios, condiciones, plazos y forma de participación. Podrá ayudar a la IA del participante a expresar su propuesta sin inventar evidencia ni sustituir su intención. Participar sin IA debe ser igualmente posible.

Las propuestas permanecen privadas durante la selección. Se conserva el original recibido, su fecha y su relación con ampliaciones posteriores. Los datos de contacto se mantienen separados de la información pública.

### Evaluación y profundización

La IA evalúa con los criterios de la convocatoria y entrega una preselección con razones y dudas. La cantidad de seleccionadas será configurable. No se presentará el resultado como una medida objetiva o universal del valor de las ideas.

El sistema permite revisar propuestas no seleccionadas para detectar omisiones y sesgos. Agrupar propuestas semejantes no debe borrar originales, participantes ni diferencias sustantivas.

Las seleccionadas pueden recibir preguntas específicas para profundizarlas. Las invitaciones y publicaciones se realizan con autorización del creador. Las respuestas se vinculan de manera verificable con la propuesta y su autor, sin depender de que este copie correctamente un asunto de correo o un código público.

La segunda evaluación conserva el vínculo con la propuesta original y explica cómo la ampliación afecta la selección.

### Publicación y votación

Tras el cierre correspondiente y la autorización del creador se publican finalistas en un portal consultable, con una presentación apta para mostrar durante un streaming.

La recomendación de IA, la preferencia de audiencia y la elección del creador se distinguen. La votación se realiza sobre una lista común sin duplicados. Cada creador configura por convocatoria la cantidad máxima de votos por participante, con tres como valor predeterminado. Cada participante puede votar una sola vez por propuesta, hasta alcanzar ese máximo. Deben explicarse los controles empleados y sus límites, sin prometer identidad única de personas cuando no pueda comprobarse.

El creador configura la fecha de apertura y cierre de la votación y si los resultados se muestran durante ella o después de su cierre. Estas condiciones se fijan antes de abrir la votación y se mantienen durante esa ronda. La configuración no permite publicar propuestas privadas sin la autorización prevista ni modifica las reglas de atribución.

El creador puede incorporar propuestas omitidas. Se contempla un mecanismo explícito para descubrir otras propuestas elegibles mediante rotación o muestreo. Los mecanismos concretos y el tamaño de la selección se justifican en el plan, conservando la sencillez del uso inicial.

No se suma automáticamente la recomendación de IA, el voto público y la preferencia del creador en un cuarto ranking. El resultado debe permitir distinguir qué representa cada señal.

### Atribución y colaboración

Las ampliaciones de autor conservan su vínculo con el original. Las mejoras posteriores de otras personas se identifican como contribuciones diferenciadas, cuando se habilite esa colaboración.

La similitud detectada por IA es una señal para revisión, no una prueba concluyente de copia. Una mejor redacción no convierte por sí sola una propuesta en una idea distinta. La fecha de recepción demuestra recepción en el sistema, no autoría universal.

## Restricciones y riesgos que debe atender el diseño

- Priorizar instalación guiada, pasos mínimos y operación conversacional. Documentar cuentas, permisos, servicios, límites y acciones manuales necesarios.
- Aprovechar capacidades admitidas de la IA contratada. No suponer que una suscripción incluye API, operación permanente o capacidades ausentes de la cuenta probada. Si el objetivo de integración no puede cumplirse, elevar la incompatibilidad antes de sustituirlo por otro modo de operación.
- Separar costos de IA, alojamiento y comunicaciones. Permitir límites de volumen o gasto cuando corresponda y demostrar el consumo del caso probado.
- Usar 50–100 propuestas breves como escenario inicial de evaluación, no como predicción comprobada de participación ni como límite universal.
- Preservar originales y evaluar riesgos de favorecer buena redacción, ideas convencionales, orden de presentación o textos preparados para influir en el evaluador.
- Tratar propuestas y enlaces aportados por participantes como contenido no confiable, sin permitir que alteren instrucciones, accedan a datos privados o autoricen acciones.
- Evitar publicaciones prematuras, exposición de contactos, votos duplicados por aparición en varias listas y envíos repetidos al reintentar operaciones.
- Explicar al participante qué información se publicará y cómo se atribuirán sus aportes. La transparencia no exige publicar todas las propuestas privadas.
- Mantener credenciales fuera del código y la documentación distribuida.

## Enfoque de exploración y construcción

El plan debe comenzar resolviendo la viabilidad de operar desde la IA contratada del creador, antes de comprometer la construcción completa del portal. La exploración se limita a incertidumbres concretas y debe producir evidencia de una integración admitida que permita obtener propuestas, evaluarlas y guardar resultados, con sus requisitos, límites y costos identificados.

Antes de explorar, el plan define qué se comprobará, los límites de la exploración y su criterio de terminación. La exploración concluye con una opción demostrada, una incompatibilidad documentada o una decisión humana necesaria; no se prolonga indefinidamente ni congela tecnologías sin evidencia.

Una vez demostrada la viabilidad, se prioriza un recorrido completo mínimo desde la recepción hasta la ampliación y publicación autorizada. Sobre ese recorrido se profundizan la calidad de selección, los controles y la votación configurable; después se verifica la instalación reproducible y se completa la documentación de entrega y del piloto posterior.

El constructor justifica en el plan la división concreta en unidades, dependencias y verificaciones. Esta orientación no fija cuatro unidades obligatorias ni sustituye el plan. La evidencia obtenida permite revisar decisiones conforme al método y a las aprobaciones humanas aplicables, sin ampliar unilateralmente el alcance.

## Entregables y verificación técnica

El kit debe incluir código y configuración reproducibles; guía de instalación asistida por IA; guía de operación; instrucciones públicas de participación; ejemplos; documentación de límites y costos; y procedimiento de piloto posterior.

El constructor ejecutará pruebas técnicas y el auditor comprobará su evidencia. El plan establecerá antes de probar los casos, los resultados esperados y las condiciones de aceptación. Las verificaciones cubrirán:

1. Un ciclo completo de recepción, evaluación, invitación a ampliar, segunda evaluación, publicación autorizada y votación.
2. Integridad de originales y vínculos de autoría y ampliación; separación de datos privados y públicos.
3. Aplicación de criterios y comparación con ejemplos revisados; propuestas descartadas, duplicadas, ambiguas y adversariales.
4. Acceso autorizado desde la IA de referencia y operación conversacional real del circuito implementado, declarando cuenta, capacidades y límites probados sin revelar secretos.
5. Instalación reproducible mediante las instrucciones en un entorno de prueba limpio, registrando obstáculos y pasos humanos.
6. Volumen inicial representativo, tiempos, consumo y recuperación de errores sin pérdida de datos ni duplicación de acciones.

Los datos sintéticos y las simulaciones deberán identificarse como tales. Una simulación no sustituye la prueba de una integración que el trabajo afirme entregar funcionando.

## Criterios de cierre

El trabajo puede cerrar cuando el kit cumpla los criterios técnicos acordados en el plan, la evidencia haya sido auditada y el humano apruebe la entrega. Debe entregarse el procedimiento del piloto real, incluidos registro de tiempo de revisión, utilidad percibida, omisiones, costos y dificultades de instalación.

Franco realizará la convocatoria real después del cierre. Conseguir creadores o audiencia, ejecutar el piloto y lograr que otra persona sin conocimientos técnicos lo instale no son condiciones de cierre de este trabajo.

La entrega debe declarar que la utilidad con audiencia real y la instalación por una persona externa sin conocimientos técnicos no están demostradas hasta realizar esas pruebas. Los resultados técnicos no deben presentarse como sustitutos de esa validación.

## Exclusiones

No se exige evaluación de entradas en tiempo real durante el vivo, operación desatendida permanente, integración con todas las redes sociales, entrada por correo, compatibilidad operativa universal con otras IA, ni capacidad masiva sin un volumen definido. Mostrar finalistas durante un vivo sí pertenece al alcance.

Tampoco se exige construir una plataforma comercial centralizada, garantizar originalidad absoluta, garantizar ausencia de fraude ni probar una calidad objetiva universal del ranking.

## Decisiones delegadas y reservadas

El constructor puede proponer arquitectura, herramientas, formatos y detalles de implementación dentro de la intención aprobada, sujetos al plan y a auditoría. Debe justificar la proporcionalidad y evitar añadir funciones o complejidad sin necesidad material.

Quedan reservados al humano los cambios de intención y alcance, aprobación del plan y cierres, elección de modelos de los actores, gastos y contratación de servicios no autorizados, publicación definitiva del kit y elección de su licencia. La replicabilidad debe contar con condiciones de uso y distribución expresas antes de publicar el kit.

Las reglas de ejecución, repositorios, rutas, capacidades y relevos se establecen en la constitución del carril Z y en sus autoridades metodológicas; no se sustituyen por este manifiesto.

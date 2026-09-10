# Manifiestos de trabajo AI

Este repositorio conserva la intención humana aprobada de cada trabajo, su vínculo con el proyecto cuando corresponde y las constituciones iniciales que permiten arrancarlo desde referencias Git exactas.

## Relación con los demás repositorios

| Autoridad | Responsabilidad |
|---|---|
| [metodo-manifiestos-ai / METODO-MANIFIESTOS.md](https://github.com/francogg89-ai/metodo-manifiestos-ai/blob/main/METODO-MANIFIESTOS.md) | Entrevista, redacción, aprobación y constitución del trabajo. Su sección 6 define PROJECT.md y el tratamiento de superficies compartidas. |
| Este README / CT-6 | Estructura de la biblioteca, creación, modificación e identidad de publicación. |
| [rules-orchestrator-ai / REGLAS-ORQUESTADOR.md](https://github.com/francogg89-ai/rules-orchestrator-ai/blob/main/REGLAS-ORQUESTADOR.md) | Transporte mecánico del orquestador, contrato CT-7. |
| [orchestra-revolutions-ai / metodo/REVOLUTIONS.md](https://github.com/francogg89-ai/orchestra-revolutions-ai/blob/main/metodo/REVOLUTIONS.md) | Ejecución, autoridades de los actores, auditoría e integración material. |

Los enlaces permiten navegar. Las ejecuciones concretas usan las identidades exactas congeladas en su constitución. Algunos documentos históricos nombran los repositorios de ejecución y transporte con el orden de palabras anterior; las coordenadas concretas deben declararse sin inferir que nombres distintos son intercambiables.

## CT-6 — Identidad de publicación y estructura de la biblioteca

Las obligaciones de CT-6 son las reglas etiquetadas de las cuatro secciones siguientes. El ejemplo final es ilustrativo.

### 1. Estructura e identidad

- **CT6-1** Cada trabajo tiene un WORK_ID único y una carpeta `manifiestos/<WORK_ID>/`. Un trabajo nuevo no reutiliza la identidad de otro.
- **CT6-2** La intención aprobada se publica en `manifiestos/<WORK_ID>/MANIFIESTO_TRABAJO.md`.
- **CT6-3** Cuando corresponda delimitar la relación con un proyecto existente o compartido, se publica `manifiestos/<WORK_ID>/PROJECT.md`. Un trabajo aislado no requiere ese archivo.
- **CT6-4** La constitución inicial se publica por defecto en `manifiestos/<WORK_ID>/CONSTITUCION_INICIAL.md`. Una ruta diferente debe quedar declarada explícitamente en las referencias de arranque.
- **CT6-5** La identidad de un documento publicado es repositorio + path + commit SHA completo, obtenido de Git y verificado después de publicar. Una rama, un SHA abreviado o el SHA de un blob no sustituye al commit exacto.
- **CT6-6** El carril identifica el circuito de ejecución; no sustituye a WORK_ID ni a PROJECT_ID. Varios trabajos pueden compartir PROJECT_ID y conservar WORK_ID y perímetros propios.

### 2. Creación y publicación

- **CT6-7** Un manifiesto se publica como definitivo únicamente después de la aprobación humana explícita conforme a METODO-MANIFIESTOS.md. Los ejemplos y borradores no constituyen aprobación ni autorización de ejecución.
- **CT6-8** PROJECT.md materializa condiciones ya acordadas. No puede conceder por inferencia capacidades, ampliar el alcance aprobado ni resolver por sí mismo decisiones reservadas al humano.
- **CT6-9** Se publica primero el manifiesto y se obtiene su identidad exacta; después PROJECT.md, cuando corresponde, y su identidad exacta; luego la constitución inicial que los referencia. El arranque se produce después de obtener la identidad exacta de esa constitución.
- **CT6-10** Cuando existe PROJECT.md, la constitución incorpora PROJECT_REPO, PROJECT_PATH y PROJECT_SHA. Cuando no existe, los omite. No se usan identidades inventadas, campos vacíos ni marcadores como referencias reales.
- **CT6-11** Las referencias entre documentos metodológicos se expresan por repositorio, path y contrato, sin crear dependencias SHA circulares. Las ejecuciones concretas congelan las identidades disponibles al constituirse.
- **CT6-12** No se publican secretos. Cuando sean necesarias, se conservan referencias seguras a las credenciales conforme al método de constitución.

### 3. PROJECT.md y límites del trabajo

- **CT6-13** PROJECT.md es el contrato estable de vinculación de ese trabajo con el proyecto. Declara proporcionalmente PROJECT_ID, WORK_ID, repositorios y sus funciones, superficies permitidas y protegidas, entornos relevantes, dependencias compartidas, límites de integración y autoridad para resolver conflictos.
- **CT6-14** Las superficies Git se delimitan por repositorio y conjunto de paths. Los recursos externos relevantes se identifican además por entorno y recurso, mediante referencias seguras suficientes para distinguirlos. Paths separados no prueban aislamiento de una base de datos, API, workflow o infraestructura compartida.
- **CT6-15** La descripción del sistema existente referencia fuentes verificables. Las condiciones comunes del proyecto pueden citarse desde una fuente canónica identificada exactamente; no se mantienen copias independientes de esa fuente como si fueran autoridades distintas.
- **CT6-16** PROJECT.md no registra trabajos activos o terminados, últimos SHAs, últimos despliegues o actores, locks, semáforos, contadores ni listas vivas de workers o carriles. Las referencias Git exactas a fuentes son identidades documentales, no un registro del estado actual.
- **CT6-17** Las reglas de concurrencia e integración remiten a la sección 6 de METODO-MANIFIESTOS.md y a las reglas de realidad material de REVOLUTIONS. PROJECT.md concreta los recursos y límites aplicables, sin redefinir autoridades, transporte ni protocolo de ejecución.
- **CT6-18** La existencia de PROJECT.md no demuestra compatibilidad ni habilita por sí sola una mutación. La comprobación de cambios del remoto y del estado real de recursos compartidos corresponde a la ejecución conforme a sus autoridades vigentes.

### 4. Modificación y conservación

- **CT6-19** Las revisiones conservan paths estables y se publican mediante commits nuevos, preservando la historia Git. No se crean copias numeradas para representar versiones ni se sobrescribe la historia para reemplazar una referencia ya publicada.
- **CT6-20** Los cambios de intención requieren aprobación humana explícita. Los cambios de PROJECT.md que alteren alcance, capacidades o decisiones reservadas requieren la autoridad correspondiente; una edición documental no concede esa autoridad.
- **CT6-21** Una revisión posterior del manifiesto, PROJECT.md, constitución o README no cambia automáticamente las referencias de un trabajo ya constituido. Su adopción durante la ejecución se resuelve y preserva conforme al método vigente del trabajo.
- **CT6-22** La consulta del remoto para comprobar cambios no reescribe PROJECT_SHA ni los cortes constitutivos. La historia y los documentos fijados deben seguir siendo localizables.
- **CT6-23** El estado de ejecución, las entregas y las auditorías permanecen en las superficies previstas por REVOLUTIONS. Esta biblioteca no mantiene un registro paralelo de avance.
- **CT6-24** Este README no amplía las fronteras de escritura de los actores ni modifica manifiestos o constituciones anteriores. La incorporación de estas convenciones a trabajos existentes se hace de forma explícita cuando corresponda.

## Cómo usar PROJECT.md

El manifiesto expresa el resultado buscado. PROJECT.md delimita cómo puede intervenir ese trabajo sobre el sistema existente. La constitución aporta las coordenadas, referencias exactas y capacidades de arranque.

Por ejemplo, dos trabajos sobre un mismo proyecto pueden tener PROJECT_ID común y trabajar sobre carpetas distintas. Si ambos afectan una misma tabla o workflow, requieren resolver también esa concurrencia material.

La sección 6 del método de manifiestos dispone comparar el corte constitutivo del repositorio compartido con su referencia actual obtenida del remoto e intersectar los paths modificados con la superficie propia. Ante solapamiento, el constructor preserva y entrega; el auditor determina la resolución técnica o la necesidad humana. REVOLUTIONS exige además comprobar el estado real cuando la decisión depende de un recurso externo. Una comprobación documental o de paths no sustituye esa verificación.

## Ejemplo mínimo de PROJECT.md

Ejemplo ficticio para adaptar; no constituye un trabajo ni concede permisos. Los nombres entre ángulos deben sustituirse por datos verificados. Se omiten las secciones que no apliquen y se amplían únicamente las que protejan una condición material.

```markdown
# Vinculación con el proyecto

PROJECT_ID: <identidad-del-proyecto>
WORK_ID: <identidad-del-trabajo>

## Proyecto y fuentes

- Sistema existente: <descripción breve>.
- Repositorio: <owner/repo>; función: <función>.
- Documentación canónica: <repositorio + path + commit SHA completo>.
- Contratos existentes que deben preservarse: <referencias exactas>.

## Perímetro de este trabajo

- Superficie Git permitida: <owner/repo> + <paths concretos>.
- Superficie protegida: <owner/repo> + <paths concretos>.
- Entorno y recursos que puede afectar: <entorno + recursos identificables>.
- Entorno y recursos protegidos: <entorno + recursos identificables>.
- Dependencias compartidas: <API, esquema, workflow u otro recurso relevante>.

## Concurrencia e integración

- Trabajos compatibles: <condiciones concretas de independencia>.
- Operaciones que requieren aislamiento o ejecución secuencial: <operaciones>.
- Integración permitida: <destino y condiciones acordadas>.
- Comprobaciones aplicables: sección 6 de METODO-MANIFIESTOS.md
  y realidad material de REVOLUTIONS, según las autoridades del trabajo.
- Ante solapamiento no resuelto: preservar y entregar al auditor
  conforme al método; no presumir compatibilidad.
- Decisiones reservadas y autoridad para resolverlas: <decisiones y autoridad>.

## Límites de autoridad

Este documento concreta el vínculo con el proyecto dentro del alcance aprobado.
Las capacidades y referencias de arranque pertenecen a la constitución.
No concede permisos adicionales ni registra el estado vivo de la ejecución.
```

# Manifiesto de trabajo — Ecosistema de constitución y orquestación para REVOLUTIONS — ORCHESTRA

## 1. Objetivo

Diseñar, verificar y dejar terminados de forma coordinada tres repositorios que completen la arquitectura de trabajo alrededor de REVOLUTIONS — ORCHESTRA:

1. `metodo-manifiestos-ai`: método para convertir una intención humana todavía incompleta en un manifiesto durable, una constitución operativa suficiente y un paquete de arranque.
2. `reglas-orquestador-ai`: reglas mecánicas de un orquestador deliberadamente tonto que sólo transporta.
3. `manifiestos-trabajo-ai`: biblioteca durable de intenciones humanas aprobadas y, cuando corresponda, contratos estables de vinculación con proyectos operativos.

Los tres repositorios deben diseñarse como piezas de un único sistema, con interfaces coherentes entre sí y compatibles con el método autoritativo `revolutions-orchestra-ai`.

El resultado no consiste en tres documentos independientes, sino en una arquitectura integrada que permita pasar de una idea humana informal a una ejecución gobernada por REVOLUTIONS — ORCHESTRA sin duplicar autoridades ni crear estado paralelo.

## 2. Método autoritativo y frontera del trabajo

El método definitivo que este trabajo debe servir es:

```text
REPO=https://github.com/francogg89-ai/revolutions-orchestra-ai
SHA=e05b24cc501ce839ffabee6d9666d069e056255c

PATHS:
- metodo/REVOLUTIONS.md
- metodo/ROL-AUDITOR.md
- metodo/ROL-CONSTRUCTOR.md
```

Los tres archivos deben leerse exactamente desde ese SHA antes de diseñar.

No se modifica `revolutions-orchestra-ai`.

No se rediseña REVOLUTIONS.

Toda decisión de este trabajo debe complementar sus autoridades, su protocolo de derivación, su separación entre materia, auditoría, Git, estado derivado y transporte, y sus fronteras de escritura de roles.

Si un requisito de este manifiesto entra en contradicción material con el método autoritativo, debe elegirse la solución mínima que conserve las autoridades de REVOLUTIONS, sin crear una segunda fuente de verdad. La contradicción y la decisión adoptada deben quedar explicadas en la entrega correspondiente.

## 3. Arquitectura general buscada

El sistema completo debe quedar conceptualmente así:

```text
HUMANO
   ↓
agente guiado por metodo-manifiestos-ai
   ↓
entrevista + resolución de ambigüedades
   ↓
MANIFIESTO_TRABAJO.md
+
PROJECT.md opcional
+
datos de constitución
   ↓
aprobación explícita del HUMANO
   ↓
publicación durable en manifiestos-trabajo-ai
   ↓
identidades Git exactas
   ↓
prompt/paquete de arranque
   ↓
ORQUESTADOR regido mecánicamente
   ↓
AUDITOR inicial
   ↓
REVOLUTIONS — ORCHESTRA
   ↓
CONSTRUCTOR ↔ AUDITOR
```

Las autoridades deben permanecer separadas.

### 3.1. `metodo-manifiestos-ai`

Define cómo una IA convierte la intención todavía incompleta del humano en:

1. un manifiesto durable y suficientemente cerrado;
2. cuando corresponda, un contrato estable de vinculación con un proyecto operativo;
3. los datos de constitución necesarios para iniciar REVOLUTIONS;
4. un prompt o paquete de arranque suficiente para el orquestador y el AUDITOR inicial.

No ejecuta el trabajo técnico.

No reemplaza REVOLUTIONS.

No decide durante la ejecución aquello que corresponde al CONSTRUCTOR, al AUDITOR o al HUMANO.

### 3.2. `manifiestos-trabajo-ai`

Es únicamente la biblioteca durable de intenciones humanas cerradas y aprobadas y, cuando corresponda, de contratos estables de vinculación con proyectos.

No contiene el desarrollo operativo del trabajo.

No contiene auditorías.

No contiene `EVENTO.md` de REVOLUTIONS.

No contiene `PLAN.md`.

No contiene bootstraps vivos.

No contiene estado actual del loop.

### 3.3. `reglas-orquestador-ai`

Define únicamente el comportamiento mecánico del orquestador.

El orquestador transporta.

No construye.

No audita.

No interpreta el trabajo.

No decide relevos metodológicos.

No decide unidades.

No decide necesidades humanas.

No decide permisos.

No selecciona modelos.

## 4. Separación de información

El diseño debe distinguir claramente tres clases de información.

### A. Intención durable

Pertenece a `MANIFIESTO_TRABAJO.md`.

Incluye proporcionalmente:

- objetivo;
- motivo;
- resultado observable buscado;
- alcance;
- exclusiones;
- restricciones;
- riesgos relevantes;
- criterios de éxito;
- obligaciones importantes del resultado;
- decisiones que materialmente deban seguir reservadas al humano.

No debe convertirse en registro de estado del trabajo.

No debe incluir por sistema:

- número de versión;
- unidad actual;
- fase actual;
- ronda;
- contador;
- `CURRENT=true`;
- última entrega;
- último auditor;
- último constructor;
- SHA vivo del work;
- SHA vivo del audit;
- estado del loop.

Git conserva la historia.

Cuando el manifiesto cambia legítimamente, se modifica el mismo path y Git produce una nueva identidad.

No crear variantes como:

```text
MANIFIESTO_v2.md
MANIFIESTO_FINAL.md
MANIFIESTO_FINAL_2.md
CURRENT_MANIFEST.md
```

### B. Contexto durable de proyecto

Cuando el trabajo forma parte de un proyecto operativo existente o continuo, puede pertenecer a `PROJECT.md`.

Puede incluir proporcionalmente:

- `PROJECT_ID`;
- identidad general del proyecto;
- repositorios que constituyen el proyecto y función de cada uno;
- superficies materiales compartidas;
- entornos relevantes;
- límites de integración;
- recursos protegidos;
- superficie que este trabajo puede afectar;
- superficie que no puede afectar;
- tipos de trabajo que pueden coexistir;
- reglas estables de concurrencia;
- reglas estables de integración;
- criterio ante solapamiento o drift;
- autoridad para resolver conflictos que no sean técnicamente resolubles.

`PROJECT.md` no es una segunda versión del manifiesto ni una base de datos viva del proyecto.

No registra:

- trabajo activo;
- trabajo terminado;
- último SHA;
- último despliegue;
- último actor;
- locks vivos;
- semáforos;
- contadores;
- lista viva de workers o carriles.

Su finalidad es actuar como contrato estable de vinculación entre ese trabajo y el proyecto sobre el cual opera.

Un trabajo aislado no necesita `PROJECT.md`.

### C. Constitución operativa del trabajo

Pertenece al paquete de arranque y posteriormente al `BOOTSTRAP.md` de REVOLUTIONS.

Incluye proporcionalmente:

- `WORK_ID`;
- carril;
- identidad exacta del método;
- identidad exacta del manifiesto;
- identidad exacta de `PROJECT.md` cuando exista;
- repositorio work;
- repositorio audit;
- repositorios fuente;
- raíz local;
- paths locales;
- entornos;
- capacidades delegadas;
- referencias seguras a credenciales;
- políticas iniciales de ejecución;
- políticas de relevo.

No se mezclan estas tres categorías por conveniencia.

El bootstrap conserva hechos de constitución y su identidad exacta de origen. No se reescribe posteriormente para simular vigencia de una fuente que cambió.

## 5. Método para construir manifiestos

`metodo-manifiestos-ai` debe ser autocontenido y reutilizable para trabajos técnicos, intelectuales, documentales, operativos, de investigación, de software u otros.

Debe poder recibir una idea informal del HUMANO y acompañarlo hasta una intención suficientemente cerrada para iniciar un trabajo mediante REVOLUTIONS.

La entrevista no debe convertirse en un formulario rígido.

Debe preguntar sólo aquello que materialmente ayude a cerrar la intención o constituir el trabajo.

No debe volver a preguntar algo que el humano ya dejó inequívocamente respondido.

Debe identificar y cerrar, cuando sean aplicables:

- qué quiere lograr el humano;
- por qué;
- cuál es el resultado observable esperado;
- qué entra;
- qué no entra;
- restricciones;
- riesgos;
- criterios de éxito;
- qué decisiones quedan delegadas;
- qué decisiones siguen reservadas al humano;
- sobre qué proyecto o sistema se trabaja;
- qué repositorios intervienen;
- qué entornos intervienen;
- qué actores tienen qué capacidades;
- qué grado de evidencia y rigor se requiere;
- qué grado de reproducibilidad se necesita;
- qué políticas de relevo quiere aplicar el humano.

Puede proponer alternativas para ayudar a decidir.

Categorías de entrevista como:

```text
exploratorio
operativo
alta criticidad
```

o:

```text
autonomía restringida
autonomía amplia
autonomía muy amplia
```

pueden usarse como ayuda conversacional, pero el resultado final debe traducirlas a obligaciones concretas cuando importen:

```text
qué debe verificarse
qué evidencia debe preservarse
qué riesgos no son aceptables
qué resultado debe reproducirse
qué acciones están delegadas
qué acciones siguen reservadas
```

## 6. Aprobación humana y publicación

El método de manifiestos debe tener un cierre humano inequívoco.

La IA puede:

- entrevistar;
- detectar ambigüedades;
- proponer;
- redactar;
- señalar contradicciones;
- sugerir decisiones.

Pero no publica un manifiesto como definitivo hasta recibir una aprobación explícita del HUMANO.

No existe aprobación por silencio, ausencia de objeción ni continuación informal de la conversación.

Una vez aprobado:

1. se publica el manifiesto en `manifiestos-trabajo-ai`;
2. se obtiene su identidad Git exacta;
3. si existe `PROJECT.md`, se publica también el vínculo correspondiente;
4. se obtienen sus identidades exactas;
5. recién entonces se produce el paquete o prompt de constitución.

## 7. Estructura de `manifiestos-trabajo-ai`

La estructura conceptual principal debe ser:

```text
manifiestos/
  <WORK_ID>/
    MANIFIESTO_TRABAJO.md
    PROJECT.md             # opcional
```

Git puede no materializar directorios vacíos.

No deben crearse trabajos ficticios.

Pueden existir plantillas separadas si realmente ayudan, siempre claramente identificadas como plantillas y nunca confundidas con trabajos reales.

El repositorio debe explicar de forma breve y suficiente:

- qué guarda;
- qué no guarda;
- estructura de paths;
- reglas para creación;
- reglas para modificación;
- rol de Git;
- `PROJECT.md` opcional;
- relación con `metodo-manifiestos-ai`;
- relación con REVOLUTIONS.

No debe convertirse en otro método de ejecución.

### 7.1. Identidad del manifiesto

La identidad de constitución es:

```text
MANIFEST_REPO=https://github.com/francogg89-ai/manifiestos-trabajo-ai
MANIFEST_PATH=manifiestos/<WORK_ID>/MANIFIESTO_TRABAJO.md
MANIFEST_SHA=<commit exacto>
```

Cuando existe proyecto:

```text
PROJECT_REPO=https://github.com/francogg89-ai/manifiestos-trabajo-ai
PROJECT_PATH=manifiestos/<WORK_ID>/PROJECT.md
PROJECT_SHA=<commit exacto>
```

Cuando manifiesto y project se publican juntos pueden compartir naturalmente el mismo commit SHA.

No usar solamente blob SHA como identidad de constitución cuando lo que se quiere congelar es el estado del repositorio. El blob SHA puede informarse adicionalmente para verificación.

### 7.2. Modificación posterior

Si un manifiesto aprobado necesita cambiar:

- se modifica el mismo path;
- se hace un nuevo commit;
- no se reescribe la historia;
- no se renombra a “v2”;
- la ejecución ya constituida conserva el SHA de origen;
- la nueva vigencia se resuelve según REVOLUTIONS para cambios de intención.

Lo mismo aplica a `PROJECT.md`.

### 7.3. Estado de ejecución prohibido

No guardar como fuentes de verdad en `manifiestos-trabajo-ai`:

```text
STATUS.md
CURRENT.md
ACTIVE.md
LAST_WORK_SHA
LAST_AUDIT_SHA
CURRENT_UNIT
CURRENT_CONSTRUCTOR
CURRENT_AUDITOR
relay_pending
```

salvo que en el futuro exista otro problema material que justifique un rediseño explícito.

## 8. Proyectos concurrentes

El diseño debe permitir que trabajos simultáneos sobre un mismo proyecto no se pisen accidentalmente sin crear un scheduler, lock central, lista viva de trabajos ni registro central redundante de mutaciones.

El método de manifiestos debe preguntar, cuando corresponda:

> ¿Este trabajo puede coexistir con otros trabajos actualmente operando sobre el mismo proyecto?

Si la respuesta es sí, debe cerrarse con suficiente precisión:

- qué superficies son independientes;
- qué recursos son compartidos;
- qué modificaciones pueden ejecutarse en paralelo;
- cuáles requieren serialización;
- cuáles requieren integración posterior;
- cuáles no pueden coexistir;
- quién tiene autoridad para resolver un conflicto.

La regla buscada es:

> Dos trabajos pueden avanzar en paralelo cuando sus perímetros materiales son demostrablemente compatibles; si existe solapamiento material no resuelto, el trabajo no debe asumir que puede proceder.

Durante REVOLUTIONS la resolución concreta debe respetar:

```text
CONSTRUCTOR detecta
↓
preserva y entrega
↓
AUDITOR determina si el conflicto puede resolverse técnicamente
o si existe NECESIDAD DEL HUMANO
```

El diseño debe resolver de forma mínima y derivable cómo un trabajo puede descubrir y verificar modificaciones materiales pertinentes realizadas por otros trabajos sobre el mismo proyecto, usando Git y referencias estables cuando sea posible.

No debe imponerse como solución un `EVENT.md` central, una lista viva de carriles ni otra superficie que replique información ya demostrable desde los repositorios autoritativos.

Antes de una mutación material sobre una superficie compartida, el trabajo debe poder consultar la vigencia pertinente desde las fuentes y comparar el perímetro propio contra modificaciones concurrentes relevantes. Si la compatibilidad no es demostrable, no procede por presunción.

El `PROJECT_SHA` conservado en bootstrap sigue siendo la identidad de origen. La consulta posterior de la vigencia del proyecto o de otros trabajos no implica reescribir el bootstrap ni reemplazar su SHA constitutivo.

## 9. Constitución operativa

`metodo-manifiestos-ai` debe reunir los datos necesarios para constituir el trabajo.

Como mínimo, cuando sean aplicables:

```text
WORK_ID
CARRIL

METHOD_REPO
METHOD_SHA

MANIFEST_REPO
MANIFEST_PATH
MANIFEST_SHA

PROJECT_REPO
PROJECT_PATH
PROJECT_SHA

WORK_REPO
AUDIT_REPO
SOURCE_REPOS

ROOT_LOCAL
LOCAL_PATHS

ENTORNOS_RELEVANTES

CAPACIDADES_CONSTRUCTOR
CAPACIDADES_AUDITOR

REFERENCIAS_SEGURAS_A_CREDENCIALES

POLITICAS_DE_EJECUCION_INICIALES
```

No transportar valores secretos.

Una referencia como:

```text
TOKEN_FUDO → variable de entorno FUDO_TOKEN
```

es admisible.

El valor del token no lo es.

### 9.1. Entornos y materialización

El método debe poder conversar con el humano sobre qué propiedad necesita realmente, por ejemplo:

```text
un único entorno material real
entorno reproducible
portabilidad fuerte entre entornos
reconstrucción total desde fuentes
```

Estas categorías sirven para entrevistar.

Después deben traducirse a obligaciones concretas.

Cuando la reproducibilidad sea parte del resultado buscado, puede pertenecer al manifiesto.

Las rutas concretas, entornos y credenciales pertenecen a constitución/bootstrap.

## 10. Fuentes auxiliares extensibles: lecciones y skills

La constitución debe admitir repositorios fuente o auxiliares opcionales, de sólo lectura para los actores salvo que otro método futuro establezca una autoridad distinta.

Entre ellos deben poder existir, sin requerir cambios a REVOLUTIONS:

- repositorios de lecciones aprendidas;
- repositorios de incidentes o experimentos;
- repositorios futuros de skills reutilizables;
- otras fuentes Git pertinentes.

Esta incorporación es únicamente un punto de extensión.

Este trabajo NO diseña el repositorio de skills ni redefine el repositorio de lecciones.

El método de manifiestos debe poder determinar si una fuente auxiliar es materialmente útil para una ejecución y cómo localizarla de forma exacta, sin cargar indiscriminadamente todo su contenido.

Una fuente de skills describe procedimientos o conocimiento reusable. Su existencia no amplía permisos, capacidades ni autoridad.

En particular:

> una skill puede explicar cómo realizar una acción; nunca autoriza por sí misma a realizarla.

Las capacidades continúan derivándose de la constitución y de las decisiones posteriores conforme a REVOLUTIONS.

Las fuentes auxiliares pueden viajar dentro de `SOURCE_REPOS` o mediante una representación equivalente inequívoca que no requiera modificar el protocolo `revolutions-hop/v1`.

El diseño específico de una taxonomía o método de skills queda fuera de alcance y podrá resolverse en un trabajo posterior.

## 11. Políticas de relevo

`metodo-manifiestos-ai` debe preguntar si el HUMANO desea políticas automáticas de relevo de actores.

Debe soportar, al menos:

```text
nunca automáticamente
sólo manual
cada N intervenciones
en ciertos límites de unidad
combinaciones expresamente definidas
```

La política concreta es una política inicial de ejecución.

Por defecto no pertenece al manifiesto salvo que el humano la considere parte material de su intención.

Debe llegar al bootstrap mediante la constitución.

### 11.1. Relevo periódico sin contadores vivos

Debe quedar expresamente prohibido resolver una política mediante estado mutable como:

```text
CONSTRUCTOR_COUNT=7
AUDITOR_COUNT=4
```

La cadencia debe ser derivable desde Git y hechos autoritativos del trabajo.

Ejemplo conceptual:

```text
RELEVO_CONSTRUCTOR:
cada 10 entregas autoritativas del CONSTRUCTOR

RELEVO_AUDITOR:
cada 10 intervenciones autoritativas del AUDITOR
```

La definición debe ser determinista y compatible con REVOLUTIONS.

La propiedad buscada es:

```text
10, 20, 30, 40...
```

y no:

```text
10 desde el último relevo
```

Un relevo manual no reinicia la cadencia.

El contador conceptual pertenece al trabajo, no a la instancia que ocupa el rol.

No se persiste como estado mutable.

Debe definirse de forma inequívoca qué hecho Git cuenta como entrega del CONSTRUCTOR y qué hecho cuenta como intervención del AUDITOR, incluidas las situaciones de `human_need`, decisiones humanas preservadas y cierre final, sin introducir `relay_pending`.

### 11.2. Autoridad sobre el relevo

El ORQUESTADOR no cuenta ni decide relevos.

La política vive en constitución/bootstrap y los actores la aplican dentro de sus autoridades.

Para CONSTRUCTOR:

```text
se alcanza umbral
↓
AUDITOR audita la entrega
↓
comprueba suficiencia del material
↓
si suficiente:
    next_actor=CONSTRUCTOR
    next_instance=fresh

si insuficiente:
    next_actor=CONSTRUCTOR
    next_instance=current
```

Para AUDITOR, cuando corresponde relevo:

```text
AUDITOR SALIENTE
↓
CONSTRUCTOR current
↓
AUDITOR fresh
```

El CONSTRUCTOR sólo transporta la decisión ya tomada.

El ORQUESTADOR sólo ejecuta `next_instance`.

## 12. Reglas mecánicas del orquestador

`reglas-orquestador-ai` debe ser lo suficientemente mínimo como para poder implementarse idealmente mediante código determinista sin un LLM razonador.

Debe distinguir:

```text
ARRANQUE EXTERNO DEL TRABAJO
```

de:

```text
PASES INTERNOS DEL LOOP
```

### 12.1. Arranque externo

El primer AUDITOR no llega desde un sobre anterior.

El orquestador recibe el paquete de constitución aprobado y abre una instancia inicial de AUDITOR.

Ese AUDITOR:

1. crea su bootstrap;
2. constituye el trabajo;
3. devuelve el primer sobre con:

```text
turn_id=1
next_actor="CONSTRUCTOR"
next_instance="fresh"
```

A partir de allí el orquestador entra en el loop ordinario.

### 12.2. Contrato de transporte

Debe respetarse exactamente `revolutions-hop/v1`, incluidos:

```text
protocol
work_id
turn_id
actor
repository
commit
next_actor
next_instance
next_prompt
human_need
unit
final
```

No agregar campos al contrato REVOLUTIONS desde `reglas-orquestador-ai`.

Cada actor termina su respuesta con:

- exactamente un bloque final `json`;
- ese bloque contiene el sobre completo;
- es el único bloque JSON de la respuesta;
- no existe contenido posterior.

El orquestador:

1. extrae ese sobre;
2. valida su forma;
3. no interpreta la prosa previa;
4. no escanea `next_prompt` buscando órdenes ocultas.

Sí lee mecánicamente los campos del contrato necesarios para transportar, incluido `next_actor` y `next_instance`.

Ante un sobre inválido:

```text
DETENER
REPORTAR
NO REPARAR SEMÁNTICAMENTE
```

### 12.3. Validaciones mínimas

Debe validar mecánicamente al menos:

- `protocol`;
- `work_id`;
- presencia de campos;
- tipos;
- combinaciones null/no-null;
- `turn_id`;
- sucesión exacta de `turn_id`;
- valores permitidos de `next_instance`;
- consistencia entre `next_actor` y `next_instance`;
- combinación `human_need/final`.

Debe respetar:

```text
human_need == null
final == false
→ next_actor, next_instance y next_prompt presentes

human_need != null
final == false
→ next_actor=null
   next_instance=null
   next_prompt=null

human_need == null
final == true
→ next_actor=null
   next_instance=null
   next_prompt=null
```

### 12.4. `next_instance`

```text
current
→ usar la instancia actualmente activa de next_actor

fresh
→ abrir una instancia nueva de next_actor

null
→ no existe siguiente actor
```

Una instancia abierta como `fresh` pasa inmediatamente a ser la instancia `current` de ese rol.

El orquestador puede conservar un handle o runtime-id efímero para reencontrar la instancia actual.

Ese handle:

- no es estado autoritativo del trabajo;
- no se publica en Git;
- no compite con REVOLUTIONS.

Si el orquestador pierde la instancia `current`, no transforma silenciosamente:

```text
current → fresh
```

Debe fallar cerrado y reportar la imposibilidad de cumplir literalmente el salto.

### 12.5. `turn_id`

Debe aplicar exactamente:

```text
AUDITOR → CONSTRUCTOR   1
CONSTRUCTOR → AUDITOR   2
AUDITOR → CONSTRUCTOR   3
...
```

El relevo no reinicia el contador.

Ante repetición, salto o retroceso, se detiene y reporta.

No intenta adivinar el número correcto.

### 12.6. Loop ordinario

Debe ser equivalente a:

```text
recibir salida
↓
extraer sobre JSON
↓
validar
↓
si human_need != null:
    detener y mostrar necesidad
↓
si final == true:
    detener y mostrar cierre
↓
si unit != null:
    mostrar transición
↓
leer next_actor
↓
leer next_instance
↓
entregar next_prompt literalmente
↓
repetir
```

El orquestador no consulta Git para reconstruir o completar `next_prompt`.

Git lo consultan los actores según el método.

### 12.7. Lo que el orquestador no hace

No decide:

- si una auditoría es correcta;
- si el constructor debe corregir;
- si una unidad terminó;
- si un relevo corresponde;
- si un actor dejó suficiente material;
- qué significa una evidencia;
- si existe NECESIDAD DEL HUMANO;
- qué repositorio modificar;
- arquitectura;
- diseño;
- permisos;
- alcance;
- riesgos;
- prioridades;
- modelo de IA a utilizar.

No resume `next_prompt`.

No lo reescribe.

No lo mejora.

No agrega contexto útil.

No copia resultados que deberían obtenerse desde Git.

No agrega todavía:

- `next_model`;
- `next_runtime`;
- selección automática de modelo;
- cambio de modelo por unidad;
- reglas de costo.

## 13. Orden humana `DETENER`

`DETENER` es una orden de control del ORQUESTADOR.

No se convierte en `human_need`.

No modifica Git.

No modifica el manifiesto.

No crea un estado durable del trabajo.

Puede existir un flag efímero de runtime equivalente a `stop_requested`.

### 13.1. Frontera segura

La frontera preferida es:

> el CONSTRUCTOR terminó su intervención y produjo un sobre válido destinado al AUDITOR, pero ese sobre todavía no fue entregado al AUDITOR.

Si `DETENER` llega mientras trabaja el CONSTRUCTOR:

1. se permite que termine;
2. se recibe y valida su sobre;
3. se detiene antes de entregarlo al AUDITOR.

Si `DETENER` llega mientras trabaja el AUDITOR:

- se permite que termine;
- si el resultado normal continúa hacia CONSTRUCTOR, se entrega al CONSTRUCTOR correspondiente;
- se permite que el CONSTRUCTOR termine;
- se recibe y valida su sobre;
- se detiene antes de entregarlo al AUDITOR.

Si el AUDITOR termina con `human_need != null` o `final=true`, la detención natural de REVOLUTIONS prevalece y no se fuerza una intervención adicional.

Si `DETENER` llega cuando ya existe un sobre CONSTRUCTOR → AUDITOR pendiente, se detiene inmediatamente sin entregarlo.

### 13.2. Reanudación

La detención preserva íntegramente el último sobre recibido.

Al ordenar:

```text
CONTINUAR
```

el orquestador entrega el `next_prompt` pendiente exactamente como fue emitido y según su `next_actor/next_instance`.

No reconstruye el pase.

### 13.3. Directivas humanas durante una pausa

El HUMANO puede usar la pausa para emitir directivas como:

```text
RELEVAR CONSTRUCTOR
RELEVAR AUDITOR
```

El orquestador no aplica directamente el relevo.

La decisión debe pasar por REVOLUTIONS.

Cuando existe una entrega de CONSTRUCTOR pendiente de AUDITOR, el orquestador entrega al AUDITOR competente dos entradas diferenciadas:

```text
ACTOR_PROMPT_LITERAL
HUMAN_DIRECTIVE_LITERAL
```

o una interfaz equivalente inequívoca.

La propiedad obligatoria es:

> la directiva humana adicional puede transportarse sin modificar, concatenar, reinterpretar ni falsificar el `next_prompt` emitido por el actor anterior.

La directiva humana no se agrega al JSON de REVOLUTIONS.

No se cambia `revolutions-hop/v1`.

Para relevo de CONSTRUCTOR:

```text
CONSTRUCTOR terminó
↓
DETENER
↓
humano: RELEVAR CONSTRUCTOR
↓
AUDITOR current recibe
   - next_prompt original
   - directiva humana separada
↓
audita
↓
comprueba suficiencia
↓
current o fresh según REVOLUTIONS
```

Para relevo de AUDITOR:

```text
CONSTRUCTOR terminó
↓
DETENER
↓
humano: RELEVAR AUDITOR
↓
AUDITOR SALIENTE audita primero esa entrega
↓
deja durablemente decidido el relevo
↓
CONSTRUCTOR current
↓
AUDITOR fresh
```

El relevo nunca saltea una entrega pendiente.

## 14. Estado efímero y fallas del orquestador

El orquestador puede necesitar en memoria/runtime:

- instancia current de AUDITOR;
- instancia current de CONSTRUCTOR;
- último `turn_id`;
- último sobre pendiente;
- `stop_requested`.

Eso es infraestructura de transporte.

No es autoridad durable.

No deben crearse como fuentes de verdad:

```text
current_unit
approved_work_sha
latest_audit
relay_pending
work_status
constructor_count
auditor_count
```

El comportamiento ante fallas y reinicios debe ser fail-closed.

Si después de un reinicio el orquestador no puede satisfacer literalmente `next_instance="current"` porque perdió la instancia correspondiente:

```text
detener
reportar
esperar resolución según el método/humano
```

No inventa continuidad conversacional.

## 15. Seguridad y secretos

El orquestador no debe necesitar valores secretos para interpretar el trabajo.

Si transporta prompts con referencias seguras, las transporta literalmente.

No registrar valores secretos innecesariamente en logs.

No convertir una referencia a secreto en el valor del secreto.

Los repositorios de manifiestos, project binding, lecciones o skills tampoco deben guardar secretos.

## 16. Relación entre los tres repositorios

Debe quedar explícito:

```text
metodo-manifiestos-ai
    ↓ produce

manifiestos-trabajo-ai
    ↓ congela intención y project binding

prompt de constitución
    ↓ inicia

reglas-orquestador-ai
    ↓ transporta

revolutions-orchestra-ai
    ↓ gobierna ejecución
```

Ninguno sustituye a otro.

No crear dependencias SHA circulares del tipo:

```text
A contiene SHA exacto de B
B contiene SHA exacto de A
```

Los documentos metodológicos pueden declarar dependencias por repositorio, path y contrato.

Las ejecuciones concretas congelan los SHAs exactos disponibles en el momento de constitución.

No intentar que un archivo contenga su propio SHA.

## 17. Condición de bootstrap de este primer trabajo

Este trabajo construye precisamente `metodo-manifiestos-ai`, `reglas-orquestador-ai` y la estructura durable de `manifiestos-trabajo-ai`.

Por lo tanto esos repositorios no pueden ser autoridades constitutivas con un SHA final previo a su propia construcción.

La primera ejecución que los construye debe evitar una dependencia circular:

- `revolutions-orchestra-ai@e05b24cc501ce839ffabee6d9666d069e056255c` gobierna la ejecución;
- el arranque externo del orquestador usa directamente el contrato de transporte de ese método y la constitución explícita de esta ejecución;
- `metodo-manifiestos-ai`, `reglas-orquestador-ai` y `manifiestos-trabajo-ai` son materia/objetivo de esta ejecución y fuentes de sólo lectura salvo la promoción final que corresponda;
- una vez construidos y publicados, las ejecuciones posteriores podrán congelar sus SHAs exactos normalmente.

Esta excepción de bootstrap no crea un segundo método ni una autoridad permanente.

## 18. Ejemplo end-to-end obligatorio

Debe incluirse al menos un ejemplo conceptual suficientemente completo.

Caso:

```text
Humano:
"Quiero agregar la función X a un proyecto ya operativo."
```

El agente de manifiestos determina proporcionalmente:

```text
objetivo
alcance
exclusiones
criterios
PROJECT_ID
repositorios del proyecto
superficie permitida
restricciones de concurrencia
work repo
audit repo
local paths
capacidades
fuentes auxiliares pertinentes
relevo constructor cada 10
relevo auditor cada 10
```

Después:

```text
humano aprueba
↓
MANIFIESTO_TRABAJO.md publicado
PROJECT.md publicado si corresponde
↓
SHAs exactos
↓
prompt de constitución
↓
orquestador abre AUDITOR inicial
↓
AUDITOR crea bootstrap
↓
turn_id=1
next_actor=CONSTRUCTOR
next_instance=fresh
↓
CONSTRUCTOR crea bootstrap
↓
loop ordinario
```

Debe quedar claro qué dato vive en cada lugar.

## 19. Casos obligatorios de verificación

### 19.1. Proyectos concurrentes

Verificar específicamente:

```text
WORK_A
y
WORK_B
```

operando simultáneamente sobre el mismo proyecto.

El sistema debe poder representar:

```text
WORK_A puede tocar superficie A
WORK_B puede tocar superficie B
```

y ejecutar ambos si son compatibles.

Si ambos pretenden mutar una misma superficie compartida sin política de integración:

```text
NO asumir compatibilidad
NO usar last-writer-wins
NO crear lock ficticio
```

La incompatibilidad debe ser visible y ruteable según REVOLUTIONS.

### 19.2. Relevo automático

Verificar un trabajo cuya constitución establece:

```text
CONSTRUCTOR → relevo cada 10 entregas
AUDITOR → relevo cada 10 intervenciones
```

Demostrar que:

- no existe contador vivo;
- la cadencia es derivable;
- el relevo manual no reinicia la secuencia;
- el orquestador no decide el relevo;
- `next_instance` es suficiente para ejecutarlo;
- el relevo del auditor usa `AUDITOR saliente → CONSTRUCTOR current → AUDITOR fresh`.

La prueba debe observar exactamente las reglas declaradas, no una aproximación narrativa.

### 19.3. `DETENER`

Verificar:

#### A

Humano dice `DETENER` mientras trabaja CONSTRUCTOR.

Resultado:

```text
constructor termina
↓
sobre queda pendiente
↓
AUDITOR todavía no lo recibe
```

#### B

Humano dice `DETENER` mientras trabaja AUDITOR.

Resultado normal:

```text
auditor termina
↓
constructor ejecuta próximo pase
↓
constructor termina
↓
pausa antes de auditor
```

#### C

Durante esa pausa el humano dice:

```text
RELEVAR AUDITOR
```

El orquestador no reemplaza al auditor.

Entrega la directiva al AUDITOR competente junto con el pase pendiente, preservando ambos por separado.

La prueba debe observar exactamente las órdenes declaradas y permitir que el humano siga las instrucciones resultantes del circuito.

## 20. Estructura de archivos esperada

Elegir una estructura mínima y coherente.

Como referencia:

### `metodo-manifiestos-ai`

```text
METODO-MANIFIESTOS.md
```

y sólo otros archivos si cumplen una función material real.

### `reglas-orquestador-ai`

```text
REGLAS-ORQUESTADOR.md
```

y sólo otros archivos si son materialmente necesarios.

### `manifiestos-trabajo-ai`

```text
README.md
manifiestos/
plantillas/                    # sólo si aportan utilidad real
```

Posibles plantillas:

```text
plantillas/MANIFIESTO_TRABAJO.md
plantillas/PROJECT.md
```

No crear documentación duplicada por estética.

Un único documento autoritativo claro es preferible a cinco documentos que repiten reglas.

## 21. No hacer

No modificar `revolutions-orchestra-ai`.

No crear otro método constructor/auditor.

No crear una base de datos de estado.

No agregar archivos de handoff.

No agregar checkpoints de relevo.

No inventar contadores vivos.

No duplicar información durable de Git en prompts.

No guardar secretos.

No inventar modelos.

No implementar selección automática de modelo.

No agregar una máquina de estados metodológica al orquestador.

No convertir `PROJECT.md` en lista viva de trabajos activos.

No crear un `EVENT.md` central para duplicar las modificaciones que ya demuestra Git.

No mutar el bootstrap para actualizar el SHA vigente de `PROJECT.md`.

No convertir `MANIFIESTO_TRABAJO.md` en configuración de runtime.

No convertir el bootstrap en manifiesto.

No publicar un manifiesto definitivo sin aprobación humana.

No crear dependencias SHA circulares.

## 22. Verificación cruzada obligatoria

Antes de cerrar, tratar los tres repositorios como una sola especificación y verificar al menos:

1. una idea informal puede convertirse en manifiesto;
2. intención y constitución quedan separadas;
3. el humano aprueba antes de publicar;
4. el manifiesto tiene identidad Git exacta;
5. un trabajo sin proyecto no necesita `PROJECT.md`;
6. un trabajo de proyecto puede tener `PROJECT.md`;
7. `PROJECT.md` no guarda estado vivo;
8. trabajos paralelos pueden tener perímetros compatibles;
9. un solapamiento material no resuelto no se oculta;
10. el bootstrap puede recibir reglas concretas de coexistencia;
11. bootstrap conserva hechos de origen, no estado;
12. el bootstrap no se reescribe para actualizar un `PROJECT_SHA` vigente;
13. la coordinación concurrente no depende de un `EVENT.md` central redundante;
14. no se transportan secretos;
15. fuentes auxiliares futuras de lecciones/skills pueden incorporarse sin ampliar autoridad;
16. políticas de relevo pueden ser configurables;
17. relevo cada N no usa contadores vivos;
18. relevo manual no reinicia la cadencia;
19. el orquestador no decide relevos;
20. `next_instance=current/fresh/null` se respeta literalmente;
21. el primer AUDITOR se abre por constitución externa;
22. el primer CONSTRUCTOR entra `fresh`;
23. `turn_id` comienza en 1 y no se reinicia;
24. `human_need` detiene;
25. `final` termina;
26. `unit` sólo se muestra;
27. `DETENER` pausa en la frontera definida;
28. `CONTINUAR` conserva el pase literal;
29. directivas humanas no reescriben `next_prompt`;
30. un `current` perdido no se transforma silenciosamente en `fresh`;
31. no existe estado paralelo durable del orquestador;
32. no hay dependencias SHA circulares;
33. la corrida constitutiva inicial no pretende depender del SHA final de los repos que está construyendo;
34. `revolutions-orchestra-ai@e05b24cc501ce839ffabee6d9666d069e056255c` permanece intacto.

## 23. Publicación y cierre

El resultado buscado no es sólo un diseño.

Los tres repositorios deben quedar terminados, autocontenidos, limpios y mutuamente coherentes en sus `main` finales.

REVOLUTIONS impide que CONSTRUCTOR o AUDITOR escriban fuera de sus repositorios respectivos. Por lo tanto la promoción final a los repositorios destino debe realizarse mediante el mecanismo compatible con el método que corresponda, sin violar las fronteras estructurales de los roles. Si requiere una intervención humana o externa material, debe rutearse explícitamente mediante REVOLUTIONS y no ocultarse como permiso del CONSTRUCTOR.

Antes del cierre definitivo deben releerse desde GitHub los archivos publicados y comprobarse que lo informado corresponde exactamente al contenido de `main`.

## 24. Informe final requerido

Al terminar informar:

### `metodo-manifiestos-ai`

```text
FINAL_SHA=
PATHS=
BLOB_SHAS=
```

### `reglas-orquestador-ai`

```text
FINAL_SHA=
PATHS=
BLOB_SHAS=
```

### `manifiestos-trabajo-ai`

```text
FINAL_SHA=
PATHS=
BLOB_SHAS=
```

Además:

- resumen corto de la arquitectura final;
- cómo se relacionan los tres repositorios;
- resultado de la verificación cruzada;
- definición final elegida para relevo periódico derivable desde Git;
- definición final de `PROJECT.md`;
- mecanismo final elegido para descubrir y verificar modificaciones materiales concurrentes sin estado central redundante;
- comportamiento exacto de `DETENER`;
- forma elegida para admitir fuentes auxiliares futuras de lecciones/skills;
- cualquier decisión de diseño material que este manifiesto no determine.

El trabajo sólo se considera cerrado cuando los tres contratos sean mutuamente consistentes y el contenido publicado haya sido verificado desde GitHub.

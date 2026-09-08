# Manifiesto de trabajo — Prueba end-to-end de gates humanos por unidad y relevos manuales

## 1. Identidad

```text
WORK_ID=prueba-orquestador-gates-unidad-relevos-manuales-ai
CARRIL=L
```

## 2. Objetivo

Ejecutar una prueba end-to-end controlada de REVOLUTIONS — ORCHESTRA cuyo objetivo principal sea comprobar el comportamiento del circuito cuando el avance entre unidades queda deliberadamente reservado a una decisión humana y, en esos mismos límites, el HUMANO puede solicitar manualmente el relevo del CONSTRUCTOR o del AUDITOR.

La prueba debe permitir observar en una misma corrida:

- continuidad con la misma instancia `current`;
- relevo manual efectivo del CONSTRUCTOR;
- continuidad posterior sobre el nuevo CONSTRUCTOR `current`;
- relevo manual efectivo del AUDITOR;
- continuidad posterior sobre el nuevo AUDITOR `current`;
- reconstrucción desde Git por las instancias frescas;
- detención y reanudación mediante una decisión humana real;
- respeto estricto de las fronteras entre HUMANO, AUDITOR, CONSTRUCTOR y ORQUESTADOR.

La dificultad buscada está en el transporte y en los relevos, no en el trabajo material.

## 3. Resultado observable esperado

El trabajo debe tener:

```text
PLAN
U01
U02
U03
U04
U05
```

El PLAN debe definir cinco unidades reales de prueba, deliberadamente simples y verificables.

Cada unidad debe producir al menos una entrega material inequívoca del CONSTRUCTOR y recibir la auditoría necesaria antes de que pueda considerarse materialmente terminada.

Después de que el AUDITOR determine que una unidad está correctamente terminada, el avance queda detenido porque la autorización para continuar a la siguiente unidad está reservada al HUMANO por este manifiesto.

En ese punto el HUMANO decide si:

```text
APROBAR UNIDAD Y CONTINUAR
```

o:

```text
APROBAR UNIDAD Y RELEVAR CONSTRUCTOR
```

o:

```text
APROBAR UNIDAD Y RELEVAR AUDITOR
```

El momento concreto en que se ejercita cada tipo de relevo no se preestablece.

Antes de cerrar satisfactoriamente U05, la corrida debe haber ejercitado al menos:

- un relevo manual efectivo del CONSTRUCTOR;
- un relevo manual efectivo del AUDITOR.

## 4. Naturaleza del trabajo material

El contenido material debe ser deliberadamente trivial, determinista y barato de auditar.

No se busca producir software de valor independiente.

Las cinco unidades existen como cinco etapas diferenciadas de la prueba del circuito.

Cada unidad debe tener un resultado observable propio que permita demostrar que:

1. el CONSTRUCTOR realizó una nueva intervención material;
2. el AUDITOR pudo verificarla;
3. el cierre de la unidad puede determinarse inequívocamente;
4. la decisión humana posterior puede detener y reanudar correctamente el circuito;
5. después de la resolución humana puede continuar la unidad siguiente sin pérdida de identidad ni continuidad.

El PLAN debe evitar complejidad artificial y elegir la mínima materia suficiente para producir esas propiedades.

## 5. Secuencia macro obligatoria

La secuencia del trabajo es:

```text
constitución
↓
PLAN
↓
decisión humana requerida sobre el PLAN conforme a REVOLUTIONS
↓
U01
↓
GATE HUMANO
↓
U02
↓
GATE HUMANO
↓
U03
↓
GATE HUMANO
↓
U04
↓
GATE HUMANO
↓
U05
↓
GATE HUMANO FINAL
↓
cierre
```

Una unidad no habilita automáticamente la siguiente.

El AUDITOR debe primero auditar la entrega correspondiente y determinar que la unidad está materialmente terminada.

Sólo después corresponde solicitar la decisión humana reservada por este manifiesto.

## 6. Gate humano entre unidades

El avance entre unidades constituye deliberadamente una decisión reservada al HUMANO para esta prueba.

Por lo tanto, después de que el AUDITOR considere terminada U01, U02, U03 o U04, debe existir una `NECESIDAD DEL HUMANO` no material antes de iniciar la unidad siguiente.

La necesidad debe solicitar inequívocamente una de las siguientes decisiones:

```text
APROBAR UNIDAD Y CONTINUAR
APROBAR UNIDAD Y RELEVAR CONSTRUCTOR
APROBAR UNIDAD Y RELEVAR AUDITOR
```

El HUMANO conserva también la autoridad para no aprobar la continuación si detecta una razón material para hacerlo.

La decisión humana debe preservarse durablemente por el AUDITOR sobre la identidad exacta correspondiente antes de continuar.

Dado que un sobre con `human_need != null` está detenido conforme a REVOLUTIONS:

- no lleva simultáneamente un pase ordinario;
- no lleva simultáneamente una transición `unit`;
- la transición de unidad se materializa únicamente después de reanudar y preservar la resolución humana.

El ORQUESTADOR no crea este gate por observar `unit`.

El gate existe porque este manifiesto reserva expresamente al HUMANO la autorización para avanzar.

## 7. Gate humano de U05

Después de auditar satisfactoriamente U05, el AUDITOR debe solicitar la decisión humana final antes de declarar terminado el trabajo.

La decisión principal es:

```text
APROBAR CIERRE
```

o la no aprobación acompañada por la resolución humana correspondiente.

No debe abrirse artificialmente una instancia `fresh` de ningún rol únicamente para materializar un relevo después de que ya no exista trabajo material posterior.

Por esa razón, los relevos obligatorios de esta prueba deben haberse ejercitado antes del cierre definitivo de U05.

## 8. Política de relevo

La política es igual para CONSTRUCTOR y AUDITOR.

### CONSTRUCTOR

```text
POLITICA_RELEVO_CONSTRUCTOR=SOLO_MANUAL_EN_GATES_HUMANOS
```

No existen relevos periódicos ni automáticos.

El HUMANO puede solicitar el relevo del CONSTRUCTOR durante cualquiera de los gates habilitados anteriores al cierre final.

### AUDITOR

```text
POLITICA_RELEVO_AUDITOR=SOLO_MANUAL_EN_GATES_HUMANOS
```

No existen relevos periódicos ni automáticos.

El HUMANO puede solicitar el relevo del AUDITOR durante cualquiera de los gates habilitados anteriores al cierre final.

### Regla común

Ninguna solicitud humana de relevo autoriza directamente al ORQUESTADOR a abrir una instancia nueva.

En particular:

```text
RELEVAR CONSTRUCTOR != abrir Claude Code fresh
RELEVAR AUDITOR     != abrir ChatGPT fresh
```

La directiva humana debe pasar por el actor competente conforme a REVOLUTIONS y a las reglas autoritativas del ORQUESTADOR.

Sólo un sobre válido `revolutions-hop/v1` con:

```text
next_instance=fresh
```

autoriza al ORQUESTADOR a abrir una nueva instancia del rol indicado.

## 9. Relevo manual del CONSTRUCTOR

Cuando el HUMANO aprueba una unidad y solicita relevo del CONSTRUCTOR:

1. la resolución humana vuelve al AUDITOR `current` por el mecanismo de reanudación correspondiente;
2. el AUDITOR preserva durablemente la resolución;
3. comprueba la suficiencia del material durable del CONSTRUCTOR saliente;
4. si el material no es suficiente para relevarlo, devuelve al CONSTRUCTOR saliente mediante `next_instance=current` para completar exclusivamente lo necesario;
5. cualquier nueva entrega se audita normalmente;
6. sólo cuando el AUDITOR determine que el relevo está metodológicamente habilitado puede emitir un sobre hacia:

```text
next_actor=CONSTRUCTOR
next_instance=fresh
```

El ORQUESTADOR no interviene en ninguna de esas decisiones.

El CONSTRUCTOR fresco debe reconstruir desde Git y continuar sin depender de la conversación o memoria de su antecesor.

## 10. Relevo manual del AUDITOR

Cuando el HUMANO aprueba una unidad y solicita relevo del AUDITOR:

1. la resolución humana vuelve al AUDITOR `current`;
2. el AUDITOR saliente preserva durablemente la decisión;
3. dispone el relevo conforme al mecanismo ordinario de REVOLUTIONS;
4. no se crea una auditoría administrativa artificial;
5. no se vuelve a auditar una misma entrega sólo por causa del relevo;
6. el CONSTRUCTOR realiza la siguiente intervención material con la instancia que corresponda;
7. el pase posterior hacia AUDITOR debe indicar `next_instance=fresh` cuando el relevo ya haya quedado dispuesto;
8. el AUDITOR fresco reconstruye desde Git y realiza su primera auditoría ordinaria sobre una nueva entrega.

El ORQUESTADOR no transforma por sí mismo la directiva humana en un pase `fresh`.

## 11. Propiedad `fresh → current`

Todo relevo efectivo debe permitir comprobar que:

1. se abre una instancia realmente nueva del rol;
2. su handle es distinto del handle anterior;
3. recibe literalmente el `next_prompt` del sobre que autorizó el `fresh`;
4. después de confirmarse esa primera entrega pasa a ser la única instancia `current` elegible de su rol;
5. la instancia anterior queda retirada;
6. los pases posteriores con `next_instance=current` vuelven exclusivamente a la nueva instancia;
7. la instancia retirada no vuelve a utilizarse.

No es necesario cerrar físicamente la conversación, ventana, terminal o sesión anterior.

La propiedad exigida es impedir su reutilización como `current`.

## 12. Reconstrucción y reproducibilidad

Toda instancia fresca debe poder continuar únicamente a partir de:

- Git;
- el bootstrap durable aplicable;
- las coordenadas exactas del pase;
- las rutas y fuentes constituidas;
- la metadata de transporte permitida por REVOLUTIONS.

No puede depender de:

- memoria conversacional del actor saliente;
- explicaciones manuales no preservadas;
- resúmenes producidos por el ORQUESTADOR;
- `_info_local` como fuente autoritativa;
- estado metodológico paralelo;
- contadores mantenidos por el ORQUESTADOR.

La prueba debe demostrar reconstrucción desde Git tanto para un CONSTRUCTOR fresco como para un AUDITOR fresco.

## 13. Superficies de trabajo

### AUDITOR

Superficie material exclusiva de escritura:

```text
https://github.com/francogg89-ai/audit-chatgpt-l
```

Runtime:

```text
ChatGPT web
```

### CONSTRUCTOR

Superficie material exclusiva de escritura:

```text
https://github.com/francogg89-ai/work-claude-l
```

Runtime:

```text
Claude Code local en Windows
```

Directorio material de trabajo:

```text
C:\Franco_Metodos_AI\work-claude-l
```

### Fuentes disponibles

Son fuentes de autoridad, referencia, localización o lectura según corresponda:

```text
https://github.com/francogg89-ai/manifiestos-trabajo-ai
https://github.com/francogg89-ai/metodo-manifiestos-ai
https://github.com/francogg89-ai/work-claude-l
https://github.com/francogg89-ai/audit-chatgpt-l
https://github.com/francogg89-ai/orchestra-revolutions-ai
https://github.com/francogg89-ai/rules-orchestrator-ai
```

Raíz local declarada:

```text
C:\Franco_Metodos_AI
```

Clones relevantes:

```text
C:\Franco_Metodos_AI\manifiestos-trabajo-ai
C:\Franco_Metodos_AI\metodo-manifiestos-ai
C:\Franco_Metodos_AI\work-claude-l
C:\Franco_Metodos_AI\audit-chatgpt-l
C:\Franco_Metodos_AI\orchestra-revolutions-ai
C:\Franco_Metodos_AI\rules-orchestrator-ai
```

Estas coordenadas no amplían las fronteras materiales de escritura.

## 14. Capacidades y límites

El CONSTRUCTOR puede:

- trabajar localmente dentro de `work-claude-l`;
- ejecutar comandos locales necesarios para construir y verificar la prueba;
- leer los repositorios declarados cuando sea necesario;
- escribir y publicar exclusivamente en su repositorio de trabajo.

El AUDITOR puede:

- leer directamente las fuentes Git necesarias para auditar;
- comprobar independientemente identidades, contenido e historia;
- escribir y publicar exclusivamente en su repositorio de auditoría;
- determinar veredictos, próximas acciones, necesidades humanas y relevos metodológicamente habilitados conforme a REVOLUTIONS.

No se requiere para esta prueba acceso a:

- entornos productivos;
- APIs externas de negocio;
- bases de datos reales;
- credenciales;
- secretos;
- despliegues.

## 15. Autoridades

El HUMANO decide:

- aprobación del PLAN;
- autorización para avanzar después de cada unidad;
- si continuar con las instancias actuales;
- si solicitar relevo manual del CONSTRUCTOR;
- si solicitar relevo manual del AUDITOR;
- aprobación del cierre final;
- cualquier cambio de intención.

El CONSTRUCTOR decide:

- diseño técnico mínimo;
- estructura del PLAN;
- material concreto de las cinco unidades;
- mecanismos de implementación y verificación dentro de su autoridad.

El AUDITOR decide:

- suficiencia de evidencia;
- defectos;
- veredicto;
- cuándo una unidad está materialmente terminada;
- si una necesidad humana es real;
- cómo procesar metodológicamente una solicitud de relevo;
- cuándo un relevo está habilitado;
- la próxima acción;
- el cierre del trabajo.

El ORQUESTADOR no decide ninguna de esas cuestiones.

Transporta mecánicamente conforme a sus reglas autoritativas.

## 16. Guardrails del ORQUESTADOR que la prueba debe ejercitar

La corrida debe preservar como mínimo:

- transporte literal de cada `next_prompt`;
- secuencia exacta de `turn_id`;
- validación mecánica de los sobres;
- uso exclusivo de `next_instance` para elegir `current` o `fresh`;
- prohibición de convertir `current` en `fresh`;
- prohibición de abrir `fresh` por una directiva humana;
- preflight antes de abrir cualquier instancia `fresh`;
- reemplazo atómico del handle `current` al confirmar el nuevo `fresh`;
- retiro definitivo del handle anterior;
- fail-closed ante imposibilidad o ambigüedad;
- ausencia de conteos de relevo;
- ausencia de estado metodológico paralelo;
- separación entre transporte y decisión.

## 17. Criterios de éxito

La prueba se considera satisfactoria cuando:

1. existe un PLAN aprobado conforme a REVOLUTIONS;
2. el PLAN contiene exactamente cinco unidades;
3. U01, U02, U03, U04 y U05 producen material verificable;
4. cada unidad recibe la auditoría necesaria;
5. después del cierre material de U01, U02, U03 y U04 se produce el gate humano obligatorio;
6. el circuito no inicia la unidad siguiente antes de recibir la resolución humana;
7. las resoluciones humanas quedan preservadas durablemente;
8. se ejecuta al menos una vez `APROBAR UNIDAD Y CONTINUAR`;
9. se solicita y ejecuta al menos un relevo efectivo del CONSTRUCTOR;
10. se solicita y ejecuta al menos un relevo efectivo del AUDITOR;
11. ningún relevo humano abre directamente una instancia `fresh`;
12. todo `fresh` proviene de un sobre válido que lo ordena;
13. el CONSTRUCTOR fresco reconstruye correctamente desde Git;
14. el AUDITOR fresco reconstruye correctamente desde Git;
15. después de cada `fresh`, los pases posteriores `current` regresan a la nueva instancia;
16. ninguna instancia retirada vuelve a utilizarse;
17. no se pierde ninguna entrega pendiente durante un relevo;
18. no se duplica una auditoría sólo por causa de un relevo;
19. `next_prompt` se conserva literalmente durante todos los saltos;
20. `turn_id` conserva sucesión exacta durante toda la corrida;
21. el ORQUESTADOR no mantiene contadores ni deriva políticas de relevo;
22. U05 recibe su decisión humana final;
23. el AUDITOR puede emitir `final=true` sólo después de quedar satisfechos los criterios aplicables.

Una detención correcta en modo fail-closed ante un defecto real constituye evidencia válida de la prueba y no debe ocultarse para forzar artificialmente el cierre satisfactorio.

## 18. Riesgos a detectar

La prueba debe hacer visibles, y no ocultar, especialmente estos defectos:

- un gate humano omitido;
- inicio prematuro de la unidad siguiente;
- una directiva humana convertida directamente en `fresh`;
- un actor fresco que reutiliza la sesión anterior;
- un actor anterior que vuelve a recibir pases `current`;
- pérdida del handle `current`;
- pérdida o duplicación de un pase;
- alteración de `next_prompt`;
- salto incorrecto de `turn_id`;
- auditoría duplicada por causa de relevo;
- relevo que saltea una entrega pendiente;
- dependencia de memoria conversacional para reconstruir;
- decisión metodológica tomada por el ORQUESTADOR;
- estado paralelo creado para seguir unidades, aprobaciones o relevos.

## 19. Exclusiones

Queda fuera del objetivo:

- producir software o documentación de valor independiente;
- probar carga o rendimiento;
- optimizar consumo de tokens;
- comparar modelos;
- probar relevos periódicos;
- contar intervenciones para decidir relevos;
- modificar `orchestra-revolutions-ai`;
- modificar `rules-orchestrator-ai`;
- modificar `metodo-manifiestos-ai`;
- modificar el sistema de manifiestos durante la ejecución;
- agregar estado especial para gates;
- agregar campos al contrato `revolutions-hop/v1`;
- crear checkpoints o handoffs especiales de relevo;
- introducir complejidad técnica no necesaria para demostrar el circuito.

Si durante la prueba aparece un defecto de las autoridades o del ORQUESTADOR, debe preservarse la evidencia y detenerse cuando corresponda. Su corrección pertenece a otro trabajo salvo decisión humana expresa.

## 20. Proyecto y concurrencia

Este es un trabajo sintético, aislado y autocontenido.

No existe `PROJECT.md`.

No opera sobre una superficie material compartida de un proyecto de negocio o software externo.

## 21. Principio rector

La mejor ejecución de este manifiesto es la que usa el mínimo trabajo material necesario para someter al circuito a cinco límites de unidad reales y permitir que el HUMANO decida en cada uno si mantiene las instancias actuales o solicita un relevo, demostrando que los relevos de CONSTRUCTOR y AUDITOR se procesan íntegramente mediante las autoridades de REVOLUTIONS y nunca mediante decisiones del ORQUESTADOR.

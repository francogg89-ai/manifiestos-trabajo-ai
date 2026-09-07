# Manifiesto de trabajo — Prueba end-to-end de relevos manuales

## 1. Identidad

```text
WORK_ID=prueba-orquestador-e2e-relevos-manuales-ai
CARRIL=L
```

## 2. Objetivo

Ejecutar una corrida end-to-end controlada y deliberadamente simple de REVOLUTIONS — ORCHESTRA cuyo objetivo principal sea comprobar que el ORQUESTADOR puede detener y reanudar correctamente el loop mientras el HUMANO solicita relevos manuales de CONSTRUCTOR y AUDITOR en momentos no preestablecidos.

El trabajo material realizado por CONSTRUCTOR y AUDITOR debe ser trivial.

La dificultad buscada no está en resolver un problema técnico o intelectual, sino en comprobar que:

- la detención preserva correctamente el transporte pendiente;
- una directiva humana de relevo llega al actor metodológicamente competente;
- el ORQUESTADOR no decide por sí mismo el relevo;
- una instancia `fresh` sea realmente nueva;
- la nueva instancia pase a ser la única `current` elegible de su rol;
- los pases posteriores continúen sobre esa nueva instancia;
- el trabajo pueda reconstruirse desde Git cuando corresponda.

## 3. Resultado observable esperado

La corrida debe completar cinco entregas principales del CONSTRUCTOR, cada una auditada antes de que corresponda la siguiente.

Esas cinco entregas y sus cinco auditorías correspondientes constituyen las diez intervenciones principales de la prueba material.

Las intervenciones constitutivas y cualquier intervención adicional exigida por REVOLUTIONS no se eliminan ni ocultan para forzar artificialmente una cantidad exacta de commits.

La corrida debe completarse sin que el ORQUESTADOR:

- interprete el trabajo;
- modifique o complete prompts;
- decida relevos;
- sustituya una instancia `current` por una `fresh`;
- reutilice una instancia retirada;
- reutilice una instancia `current` cuando el sobre exige `fresh`;
- pierda silenciosamente continuidad;
- altere la secuencia de `turn_id`;
- omita o duplique entregas;
- construya o audite por cuenta de los actores;
- cree bootstraps por cuenta de los actores;
- mantenga estado metodológico paralelo.

## 4. Superficies de trabajo

El CONSTRUCTOR trabaja exclusivamente sobre:

```text
https://github.com/francogg89-ai/work-claude-l
```

El AUDITOR trabaja exclusivamente sobre:

```text
https://github.com/francogg89-ai/audit-chatgpt-l
```

El método de ejecución es:

```text
https://github.com/francogg89-ai/orchestra-revolutions-ai
```

El ORQUESTADOR se rige por:

```text
https://github.com/francogg89-ai/rules-orchestrator-ai
```

Los repositorios metodológicos, de manifiestos y de reglas son fuentes de autoridad o referencia y no son superficies materiales de escritura de esta prueba.

No existe `PROJECT.md`.

## 5. Trabajo material deliberadamente trivial

El CONSTRUCTOR debe diseñar el PLAN mínimo compatible con REVOLUTIONS.

Después de aprobado el PLAN, el trabajo material debe reducirse a una única unidad sencilla y determinista.

Una forma admisible es mantener una secuencia monotónica en la que cada entrega agregue únicamente el siguiente elemento esperado.

No se busca creatividad, arquitectura ni resolución de un problema complejo.

El contenido existe solamente para que cada intervención produzca una entrega Git inequívoca, pueda ser auditada y permita continuar el loop.

## 6. Longitud de la prueba

La corrida debe alcanzar cinco entregas principales del CONSTRUCTOR posteriores al establecimiento y aprobación del PLAN.

Cada una debe recibir su auditoría correspondiente antes de continuar.

La constitución inicial y las intervenciones adicionales que REVOLUTIONS exija se realizan normalmente.

No existe un contador durable paralelo de vueltas.

El AUDITOR no debe declarar `final=true` antes de que:

1. existan cinco entregas principales de la unidad material;
2. la quinta haya sido auditada;
3. no exista una entrega pendiente;
4. se hayan ejercitado los escenarios manuales requeridos;
5. se satisfagan los demás criterios de éxito.

## 7. Política de relevo

Para esta prueba no existe relevo periódico automático de CONSTRUCTOR ni de AUDITOR.

Los relevos que se ejerciten son solicitados por el HUMANO durante la corrida.

No existe una grilla periódica de relevos y el ORQUESTADOR no mantiene ni deriva ningún contador para decidirlos.

El mecanismo efectivo de relevo sigue siendo exclusivamente el definido por REVOLUTIONS.

## 8. Detención y relevos manuales

Durante la ejecución, el HUMANO puede ordenar al ORQUESTADOR:

```text
DETENER
```

Una vez detenida correctamente la corrida, el HUMANO puede emitir una directiva como:

```text
RELEVAR CONSTRUCTOR
```

o:

```text
RELEVAR AUDITOR
```

El momento y el rol elegido quedan deliberadamente reservados al HUMANO y no se preestablecen en este manifiesto.

El ORQUESTADOR:

- no decide qué actor debe relevarse;
- no transforma directamente la directiva humana en `next_instance=fresh`;
- no modifica un sobre pendiente;
- no inventa una nueva intervención;
- entrega la directiva humana conforme a sus reglas al actor metodológicamente competente.

El actor correspondiente procesa la solicitud conforme a REVOLUTIONS y determina el pase que corresponda.

## 9. Escenarios end-to-end obligatorios

La corrida debe atravesar efectivamente:

- al menos una detención mediante `DETENER`;
- una posterior continuación del circuito;
- al menos un relevo manual efectivo solicitado por el HUMANO;
- un pase `fresh` real derivado de ese proceso;
- continuidad posterior mediante `current` sobre la instancia recién relevada;
- reconstrucción desde Git por al menos una instancia fresca;
- aprobación humana del PLAN cuando REVOLUTIONS determine que corresponde;
- continuación normal después de esa resolución humana.

El HUMANO puede solicitar relevos adicionales durante la corrida si desea ejercitar ambos roles.

## 10. Semántica observable del relevo

Cuando un relevo produce una instancia `fresh`, la prueba debe permitir comprobar que:

1. se abre una instancia realmente nueva;
2. esa instancia recibe el `next_prompt` correspondiente;
3. después de la primera entrega confirmada pasa a ser la única `current` elegible de su rol;
4. la instancia anterior queda retirada;
5. un pase posterior `current` vuelve a la instancia nueva y no a la retirada.

La ventana o sesión anterior puede permanecer físicamente abierta. Su cierre físico no forma parte del resultado requerido.

La propiedad requerida es que ya no pueda volver a utilizarse como `current`.

## 11. Continuidad y reconstrucción

Una instancia fresca debe poder continuar sin depender de la memoria conversacional de la instancia saliente.

Los relevos deben apoyarse en material durable y coordenadas exactas conforme a REVOLUTIONS.

La prueba debe comprobar que:

- un CONSTRUCTOR fresco reconstruya desde Git;
- un AUDITOR fresco reconstruya desde Git cuando sea relevado;
- no se vuelva a auditar una misma entrega sólo por causa del relevo;
- no se pierda una entrega pendiente;
- `turn_id` continúe su secuencia ordinaria durante todo el proceso;
- un relevo no abra una secuencia paralela.

## 12. Autoridades

REVOLUTIONS — ORCHESTRA gobierna ejecución, roles y relevos metodológicos.

Las reglas del ORQUESTADOR gobiernan exclusivamente el transporte.

El CONSTRUCTOR construye.

El AUDITOR audita, determina la próxima acción y decide metodológicamente cuándo una solicitud de relevo está habilitada.

El HUMANO decide cuándo detener la corrida y qué relevo manual solicitar.

El ORQUESTADOR no adquiere ninguna de esas autoridades.

## 13. Criterios de éxito

La prueba se considera satisfactoria cuando:

1. se completan cinco entregas principales del CONSTRUCTOR;
2. las cinco reciben su auditoría correspondiente;
3. se ejecuta correctamente al menos una secuencia `DETENER → directiva humana → continuación`;
4. se procesa correctamente al menos un relevo manual;
5. el ORQUESTADOR no decide el relevo;
6. cualquier `fresh` abre efectivamente una instancia distinta;
7. la instancia `fresh` pasa a ser la única `current` elegible;
8. la instancia retirada no vuelve a recibir pases `current`;
9. las instancias frescas reconstruyen correctamente desde Git;
10. `next_prompt` se transporta literalmente;
11. `turn_id` mantiene sucesión exacta;
12. no existen entregas omitidas ni auditorías duplicadas;
13. la quinta entrega material queda auditada;
14. el AUDITOR puede declarar el trabajo terminado conforme a REVOLUTIONS.

Una falla detectada y detenida en modo fail-closed constituye evidencia válida de la prueba y no debe ocultarse para alcanzar artificialmente el cierre.

## 14. Exclusiones

Queda fuera del objetivo:

- producir software de valor independiente;
- tener relevos periódicos automáticos;
- optimizar consumo de tokens;
- comparar modelos;
- modificar REVOLUTIONS durante la corrida;
- modificar las reglas del ORQUESTADOR durante la corrida;
- agregar IDs persistentes de instancia;
- agregar contadores de relevo;
- convertir al ORQUESTADOR en un agente razonador;
- crear estado paralelo a Git.

## 15. Principio de la prueba

La mejor ejecución es aquella en la que CONSTRUCTOR y AUDITOR realizan el menor trabajo material razonablemente posible mientras el HUMANO puede interrumpir el circuito y solicitar relevos sin que el ORQUESTADOR abandone su función puramente mecánica.

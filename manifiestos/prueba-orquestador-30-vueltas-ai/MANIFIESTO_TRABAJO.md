# Manifiesto de trabajo — Prueba del orquestador en 30 vueltas

## 1. Identidad

```text
WORK_ID=prueba-orquestador-30-vueltas-ai
CARRIL=J
```

## 2. Objetivo

Ejecutar una corrida controlada y deliberadamente simple de REVOLUTIONS — ORCHESTRA cuyo objetivo principal sea poner a prueba el comportamiento del ORQUESTADOR durante un loop suficientemente largo.

El trabajo material realizado por CONSTRUCTOR y AUDITOR debe ser trivial.

La dificultad buscada no está en resolver un problema técnico o intelectual, sino en comprobar que el transporte entre actores permanece correcto durante una secuencia prolongada que incluya continuidad de instancias, relevos periódicos, relevos solicitados por el HUMANO, detenciones y reconstrucción desde Git.

## 3. Resultado observable esperado

La corrida debe poder completar treinta entregas principales del CONSTRUCTOR, cada una auditada antes de que corresponda la siguiente, sin que el ORQUESTADOR:

- interprete el trabajo;
- modifique prompts;
- reconstruya información por cuenta propia;
- decida relevos;
- sustituya una instancia `current` por una `fresh`;
- pierda la continuidad de una instancia;
- altere la secuencia de `turn_id`;
- omita una auditoría;
- duplique una entrega;
- mantenga contadores metodológicos propios;
- convierta una orden humana de control en una decisión metodológica propia.

El cierre satisfactorio debe demostrar que el sistema puede atravesar la corrida completa conservando las autoridades de REVOLUTIONS — ORCHESTRA.

## 4. Superficies de trabajo

El CONSTRUCTOR trabaja exclusivamente sobre:

```text
https://github.com/francogg89-ai/work-claude-j
```

El AUDITOR trabaja exclusivamente sobre:

```text
https://github.com/francogg89-ai/audit-chatgpt-j
```

El método de ejecución es:

```text
https://github.com/francogg89-ai/revolutions-orchestra-ai
```

El ORQUESTADOR se rige por:

```text
https://github.com/francogg89-ai/rules-orchestrator-ai
```

Los repositorios metodológicos, de manifiestos y de reglas son fuentes de autoridad o referencia y no son superficies materiales que CONSTRUCTOR o AUDITOR deban modificar durante esta prueba.

No existe `PROJECT.md`: se trata de un trabajo aislado y sintético.

## 5. Trabajo material deliberadamente trivial

El CONSTRUCTOR debe diseñar el PLAN mínimo compatible con REVOLUTIONS para realizar la prueba.

Después de aprobado el PLAN, el trabajo material debe reducirse a una única unidad sencilla y determinista.

La unidad debe permitir que cada nueva entrega realice una modificación mínima cuya corrección pueda comprobarse objetivamente.

Una forma admisible es mantener una secuencia monotónica en la que cada intervención agregue únicamente el siguiente elemento esperado.

No se busca creatividad, optimización, arquitectura ni resolución de un problema complejo.

El contenido existe solamente para que cada intervención:

1. produzca una entrega Git inequívoca;
2. pueda ser auditada;
3. origine un nuevo pase;
4. obligue al ORQUESTADOR a continuar el loop.

El CONSTRUCTOR y el AUDITOR deben evitar complejidad artificial que no contribuya a la prueba del transporte.

## 6. Longitud de la prueba

La corrida debe alcanzar treinta entregas principales del CONSTRUCTOR.

Cada entrega del CONSTRUCTOR debe ser auditada antes de continuar.

La constitución inicial del trabajo y las intervenciones que REVOLUTIONS requiera para constituir correctamente los actores se realizan normalmente y no deben ser eliminadas para hacer coincidir artificialmente un contador conversacional.

La cantidad de entregas y de intervenciones se deriva desde las historias Git autoritativas conforme al método.

No existe un contador durable paralelo de “vueltas”.

El AUDITOR no debe declarar `final=true` antes de que:

1. existan treinta entregas principales del CONSTRUCTOR;
2. la trigésima haya sido auditada;
3. no exista una entrega pendiente;
4. se hayan satisfecho los demás criterios de éxito de este manifiesto.

## 7. Política periódica de relevo

La política de relevo es parte material de esta prueba.

### CONSTRUCTOR

Debe relevarse periódicamente al CONSTRUCTOR cada diez entregas del CONSTRUCTOR.

La cadencia se deriva conforme a `metodo-manifiestos-ai` sobre múltiplos absolutos:

```text
10
20
30
...
```

Un relevo manual no reinicia ni desplaza esta grilla.

Si al alcanzarse un múltiplo corresponde el cierre definitivo del trabajo y no existe una nueva intervención material que entregar a un CONSTRUCTOR, no se abre artificialmente una instancia fresca sólo para materializar un relevo sin trabajo posterior.

### AUDITOR

Debe relevarse periódicamente al AUDITOR cada doce intervenciones auditoras conforme a la definición y al mecanismo de derivación establecidos por `metodo-manifiestos-ai`.

La cadencia opera sobre múltiplos absolutos:

```text
12
24
36
...
```

Un relevo manual no reinicia ni desplaza esta grilla.

La existencia de commits constitutivos o de otras intervenciones que el método considere computables no debe ocultarse ni corregirse mediante un contador paralelo. La posición aplicable se deriva desde Git.

## 8. Relevos solicitados por el HUMANO

Durante la ejecución, el HUMANO puede ordenar al ORQUESTADOR:

```text
DETENER
```

y posteriormente emitir directivas como:

```text
RELEVAR CONSTRUCTOR
```

o:

```text
RELEVAR AUDITOR
```

El momento de esas intervenciones humanas no queda preestablecido en el manifiesto.

La finalidad es comprobar que el ORQUESTADOR aplica su frontera segura de detención y entrega la directiva al actor metodológicamente competente sin decidir él mismo el relevo.

Un relevo solicitado por el HUMANO:

- no reinicia la cadencia periódica;
- no modifica el manifiesto;
- no crea un contador nuevo;
- no permite saltear una entrega todavía no auditada;
- no autoriza al ORQUESTADOR a transformar por sí mismo `current` en `fresh`.

Los actores deben procesar la directiva conforme a REVOLUTIONS — ORCHESTRA y emitir posteriormente el `next_instance` que corresponda.

## 9. Continuidad y reconstrucción

Una instancia fresca debe poder continuar el trabajo sin depender de la memoria conversacional de la instancia saliente.

Los relevos deben apoyarse en el material durable y en las coordenadas exactas establecidas por REVOLUTIONS.

El experimento debe comprobar especialmente que:

- el nuevo CONSTRUCTOR reconstruya desde Git;
- el nuevo AUDITOR reconstruya desde Git;
- el trabajo continúe sobre el corte correcto;
- no se vuelva a auditar una misma entrega por causa del relevo;
- no se pierda una entrega pendiente;
- el ORQUESTADOR utilice exclusivamente `next_instance` para decidir si corresponde `current` o `fresh`.

## 10. Autoridades

REVOLUTIONS — ORCHESTRA gobierna la ejecución, los roles, la derivación, los relevos metodológicos y el contrato `revolutions-hop/v1`.

Las reglas del ORQUESTADOR gobiernan exclusivamente el transporte.

El CONSTRUCTOR construye.

El AUDITOR audita, determina la próxima acción, decide metodológicamente los relevos que estén habilitados y declara el cierre.

El HUMANO puede detener, continuar, ordenar una intervención humana permitida y resolver cualquier `NECESIDAD DEL HUMANO`.

El ORQUESTADOR no adquiere ninguna de esas autoridades.

## 11. Criterios de éxito

La prueba se considera satisfactoria cuando:

1. se completan treinta entregas principales del CONSTRUCTOR;
2. todas son auditadas exactamente en la secuencia correspondiente;
3. los relevos periódicos del CONSTRUCTOR se producen conforme a la cadencia de diez;
4. los relevos periódicos del AUDITOR se producen conforme a la cadencia de doce;
5. cualquier relevo manual solicitado durante la corrida se procesa sin reiniciar las cadencias periódicas;
6. las instancias frescas reconstruyen correctamente desde Git;
7. los pases `current` conservan la misma instancia;
8. los pases `fresh` abren efectivamente una instancia nueva;
9. `next_prompt` llega literalmente al actor siguiente;
10. `turn_id` mantiene sucesión exacta durante la corrida;
11. no existen entregas omitidas ni duplicadas;
12. el ORQUESTADOR no crea estado metodológico paralelo ni toma decisiones reservadas a los actores;
13. la trigésima entrega queda auditada;
14. el AUDITOR puede declarar el trabajo terminado conforme a REVOLUTIONS.

Una falla detectada correctamente y detenida en modo fail-closed no debe ocultarse para lograr artificialmente las treinta entregas. Debe exponerse al HUMANO conforme a las reglas aplicables.

## 12. Exclusiones

Queda fuera del objetivo:

- producir software de valor independiente;
- evaluar la calidad intelectual de Claude o ChatGPT;
- optimizar consumo de tokens;
- comparar modelos;
- modificar REVOLUTIONS — ORCHESTRA;
- modificar las reglas del ORQUESTADOR durante la corrida;
- modificar `metodo-manifiestos-ai`;
- convertir el ORQUESTADOR en un agente razonador;
- agregar contadores persistentes para facilitar la prueba;
- crear estado paralelo a Git.

Si la prueba descubre un defecto de alguno de esos sistemas, se preserva la evidencia correspondiente, pero la corrección del sistema defectuoso constituye un trabajo separado salvo decisión expresa del HUMANO.

## 13. Principio de la prueba

La mejor ejecución de este manifiesto es aquella en la que CONSTRUCTOR y AUDITOR hacen el menor trabajo material razonablemente posible mientras el ORQUESTADOR atraviesa la mayor cantidad posible de situaciones reales del protocolo sin recibir ayuda interpretativa.

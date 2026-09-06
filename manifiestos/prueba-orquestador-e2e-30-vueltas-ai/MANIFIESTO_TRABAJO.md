# Manifiesto de trabajo — Prueba end-to-end del orquestador en 30 vueltas

## 1. Identidad

```text
WORK_ID=prueba-orquestador-e2e-30-vueltas-ai
CARRIL=K
```

## 2. Objetivo

Ejecutar una corrida end-to-end controlada y deliberadamente simple de REVOLUTIONS — ORCHESTRA cuyo objetivo principal sea comprobar el comportamiento del ORQUESTADOR y la reemplazabilidad de los actores durante un loop prolongado.

El trabajo material realizado por CONSTRUCTOR y AUDITOR debe ser trivial.

La dificultad buscada no está en resolver un problema técnico o intelectual, sino en comprobar que la cadena completa permanece correcta durante una secuencia extensa que incluya continuidad de instancias, relevos periódicos, detención y continuación, una necesidad humana con reanudación y reconstrucción desde Git.

## 3. Resultado observable esperado

La corrida debe completar treinta entregas principales del CONSTRUCTOR, cada una auditada antes de que corresponda la siguiente.

Esas treinta entregas y sus treinta auditorías correspondientes constituyen las sesenta intervenciones principales de la prueba material.

Las intervenciones constitutivas y cualquier intervención adicional que REVOLUTIONS exija para preservar correctamente el protocolo no se eliminan, ocultan ni fusionan para forzar artificialmente una cantidad exacta de commits por repositorio.

La corrida debe completarse sin que el ORQUESTADOR:

- interprete el trabajo;
- modifique o complete prompts;
- reconstruya información sustantiva por cuenta propia;
- decida relevos;
- sustituya una instancia `current` por una `fresh`;
- pierda silenciosamente la continuidad de una instancia;
- altere la secuencia de transporte;
- omita una auditoría;
- duplique una entrega;
- mantenga contadores metodológicos propios;
- convierta una orden humana de control en una decisión metodológica propia;
- oculte una falla para permitir que la prueba continúe.

El cierre satisfactorio debe demostrar que la cadena completa puede atravesar la corrida conservando las autoridades de REVOLUTIONS — ORCHESTRA y de las reglas del ORQUESTADOR.

## 4. Superficies de trabajo

El CONSTRUCTOR trabaja exclusivamente sobre:

```text
https://github.com/francogg89-ai/work-claude-k
```

El AUDITOR trabaja exclusivamente sobre:

```text
https://github.com/francogg89-ai/audit-chatgpt-k
```

El método de ejecución es:

```text
https://github.com/francogg89-ai/orchestra-revolutions-ai
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
4. obligue al sistema a continuar el loop;
5. permita ejercitar las situaciones de transporte exigidas por este manifiesto.

El CONSTRUCTOR y el AUDITOR deben evitar complejidad artificial que no contribuya a la prueba.

## 6. Longitud de la prueba

La corrida debe alcanzar treinta entregas principales del CONSTRUCTOR posteriores al establecimiento y aprobación del PLAN.

Cada una de esas treinta entregas debe recibir su auditoría correspondiente antes de continuar con la siguiente.

La constitución inicial del trabajo y las intervenciones que REVOLUTIONS requiera para constituir correctamente los actores se realizan normalmente.

También se realizan normalmente las intervenciones adicionales que una necesidad humana, un relevo todavía no habilitado u otra obligación real del método requieran.

No se suprimen esas intervenciones para mantener artificialmente una igualdad numérica entre las historias Git.

La cantidad de entregas e intervenciones y las cadencias aplicables se derivan desde las historias Git autoritativas conforme a los métodos gobernantes.

No existe un contador durable paralelo de “vueltas”.

El AUDITOR no debe declarar `final=true` antes de que:

1. existan treinta entregas principales de la unidad material;
2. la trigésima haya sido auditada;
3. no exista una entrega pendiente;
4. se hayan ejercitado los escenarios obligatorios de esta prueba;
5. se hayan satisfecho los demás criterios de éxito de este manifiesto.

## 7. Política periódica de relevo

La política de relevo es parte material de esta prueba.

### CONSTRUCTOR

Debe iniciarse el relevo periódico del CONSTRUCTOR al alcanzarse cada múltiplo absoluto de ocho intervenciones computables del CONSTRUCTOR conforme a `metodo-manifiestos-ai`.

La grilla es:

```text
8
16
24
32
...
```

Al alcanzarse una marca, el AUDITOR aplica el mecanismo de suficiencia previsto por REVOLUTIONS.

Si el material durable no es suficiente para relevar inmediatamente al CONSTRUCTOR, las intervenciones necesarias para alcanzar esa suficiencia pertenecen al loop normal.

La demora entre la marca periódica y el relevo efectivo:

- no reinicia la cadencia;
- no desplaza la siguiente marca absoluta;
- no crea una secuencia de transporte paralela;
- no crea un checkpoint o handoff especial;
- no autoriza al ORQUESTADOR a decidir cuándo el relevo quedó habilitado.

Un relevo manual tampoco reinicia ni desplaza esta grilla.

Si al alcanzarse una marca corresponde el cierre definitivo del trabajo y no existe una nueva intervención material para un CONSTRUCTOR, no se abre artificialmente una instancia fresca sólo para materializar un relevo sin trabajo posterior.

### AUDITOR

Debe relevarse periódicamente al AUDITOR cada doce intervenciones auditoras computables conforme a `metodo-manifiestos-ai`.

La grilla es:

```text
12
24
36
...
```

Un relevo manual no reinicia ni desplaza esta grilla.

La existencia de commits constitutivos, necesidades humanas u otras intervenciones que el método considere computables no debe ocultarse ni corregirse mediante un contador paralelo.

La posición aplicable se deriva desde Git.

## 8. Escenarios end-to-end obligatorios

Además del loop ordinario, la corrida debe atravesar efectivamente las siguientes situaciones:

- al menos un relevo periódico efectivo del CONSTRUCTOR;
- al menos un relevo periódico efectivo del AUDITOR;
- continuidad mediante pases `current`;
- entrada de CONSTRUCTOR mediante `fresh` en su entorno local;
- entrada de AUDITOR mediante `fresh`;
- una orden humana `DETENER` seguida posteriormente por `CONTINUAR`;
- una `NECESIDAD DEL HUMANO` real, deliberadamente sencilla y acotada;
- resolución de esa necesidad por el HUMANO y reanudación del mismo actor conforme al método;
- continuación normal del loop después de esa reanudación.

La necesidad humana utilizada para ejercitar la reanudación debe ser simple y no introducir una dificultad de dominio que distraiga del objetivo de transporte.

El PLAN puede determinar el punto material más sencillo para hacerla necesaria, siempre que no fabrique una falsa necesidad contraria a REVOLUTIONS.

## 9. Relevos solicitados por el HUMANO

Durante la ejecución, el HUMANO puede ordenar al ORQUESTADOR:

```text
DETENER
```

y, durante una pausa permitida, puede emitir directivas como:

```text
RELEVAR CONSTRUCTOR
```

o:

```text
RELEVAR AUDITOR
```

El momento de esos relevos manuales no queda preestablecido.

Un relevo solicitado por el HUMANO:

- no reinicia la cadencia periódica;
- no modifica el manifiesto;
- no crea un contador nuevo;
- no permite saltear una entrega todavía no auditada;
- no autoriza al ORQUESTADOR a transformar por sí mismo `current` en `fresh`.

Los actores procesan la directiva conforme a REVOLUTIONS — ORCHESTRA.

## 10. Continuidad y reconstrucción

Una instancia fresca debe poder continuar sin depender de la memoria conversacional de la instancia saliente.

Los relevos deben apoyarse en el material durable y en las coordenadas de transporte previstas por REVOLUTIONS.

El experimento debe comprobar especialmente que:

- un CONSTRUCTOR fresco localice correctamente su entorno y reconstruya desde Git;
- un AUDITOR fresco reconstruya desde Git;
- el trabajo continúe sobre los cortes exactos correspondientes;
- no se vuelva a auditar una misma entrega por causa del relevo;
- no se pierda una entrega pendiente;
- una demora en habilitar un relevo no altere la grilla periódica;
- el ORQUESTADOR utilice exclusivamente las instrucciones mecánicas de transporte previstas por sus reglas.

## 11. Autoridades

REVOLUTIONS — ORCHESTRA gobierna la ejecución, los roles, la derivación, los relevos metodológicos y el contrato de transporte entre actores.

Las reglas del ORQUESTADOR gobiernan exclusivamente el transporte mecánico.

El CONSTRUCTOR construye.

El AUDITOR audita, determina la próxima acción, decide metodológicamente los relevos que estén habilitados y declara el cierre.

El HUMANO puede detener, continuar, emitir las directivas humanas permitidas y resolver cualquier `NECESIDAD DEL HUMANO`.

El ORQUESTADOR no adquiere ninguna de esas autoridades.

## 12. Criterios de éxito

La prueba se considera satisfactoria cuando:

1. se completan treinta entregas principales de la unidad material del CONSTRUCTOR;
2. las treinta reciben su auditoría correspondiente antes de la siguiente entrega;
3. los relevos periódicos del CONSTRUCTOR se procesan sobre la grilla absoluta de ocho;
4. los relevos periódicos del AUDITOR se procesan sobre la grilla absoluta de doce;
5. una eventual demora en habilitar un relevo no reinicia ni desplaza su grilla;
6. las instancias frescas reconstruyen correctamente desde Git;
7. el CONSTRUCTOR fresco puede entrar correctamente en su entorno local;
8. los pases `current` conservan la instancia correspondiente;
9. los pases `fresh` abren efectivamente una instancia nueva;
10. `DETENER` y `CONTINUAR` preservan correctamente el pase pendiente;
11. una `NECESIDAD DEL HUMANO` detiene el loop y puede reanudarse correctamente después de su resolución;
12. la secuencia de transporte permanece exacta durante toda la corrida, incluidas las intervenciones necesarias para completar un relevo o reanudar una necesidad humana;
13. no existen entregas omitidas ni auditorías duplicadas;
14. el ORQUESTADOR no crea estado metodológico paralelo ni toma decisiones reservadas a los actores;
15. la trigésima entrega material queda auditada;
16. el AUDITOR puede declarar el trabajo terminado conforme a REVOLUTIONS.

Una falla detectada correctamente y detenida en modo fail-closed no debe ocultarse para lograr artificialmente las treinta entregas.

La falla debe exponerse al HUMANO conforme a las reglas aplicables y constituye un resultado válido de la prueba, aunque impida alcanzar el cierre satisfactorio.

## 13. Exclusiones

Queda fuera del objetivo:

- producir software de valor independiente;
- evaluar la calidad intelectual de Claude o ChatGPT;
- optimizar consumo de tokens;
- comparar modelos;
- modificar `orchestra-revolutions-ai` durante la corrida;
- modificar las reglas del ORQUESTADOR durante la corrida;
- modificar `metodo-manifiestos-ai`;
- convertir el ORQUESTADOR en un agente razonador;
- agregar contadores persistentes para facilitar la prueba;
- crear estado paralelo a Git;
- crear artefactos especiales de relevo que REVOLUTIONS no requiera;
- ocultar intervenciones reales para conservar una cantidad artificial de turnos.

Si la prueba descubre un defecto de alguno de esos sistemas, se preserva la evidencia correspondiente, pero su corrección constituye un trabajo separado salvo decisión expresa del HUMANO.

## 14. Principio de la prueba

La mejor ejecución de este manifiesto es aquella en la que CONSTRUCTOR y AUDITOR hacen el menor trabajo material razonablemente posible mientras la cadena completa atraviesa la mayor cantidad de situaciones reales del protocolo sin recibir ayuda interpretativa.

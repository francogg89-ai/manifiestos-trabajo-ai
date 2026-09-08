# CONSTITUCIÓN INICIAL

Esta constitución inicial fue materializada conforme a
https://github.com/francogg89-ai/metodo-manifiestos-ai
en el commit exacto
452d8cce2dd36106e0efce0c957b951c713fdcc8.

WORK_ID=prueba-orquestador-gates-unidad-relevos-manuales-ai
CARRIL=L

METHOD_REPO=https://github.com/francogg89-ai/orchestra-revolutions-ai
METHOD_SHA=4d88fce3ed3c87bd231c45ec60dcb713538b2514

METHOD_PATHS:
metodo/REVOLUTIONS.md
metodo/ROL-AUDITOR.md
metodo/ROL-CONSTRUCTOR.md

MANIFEST_REPO=https://github.com/francogg89-ai/manifiestos-trabajo-ai
MANIFEST_PATH=manifiestos/prueba-orquestador-gates-unidad-relevos-manuales-ai/MANIFIESTO_TRABAJO.md
MANIFEST_SHA=294b8de4ba7b11ba0272bae29910d1a12ae29d3e

RULES_REPO=https://github.com/francogg89-ai/rules-orchestrator-ai
RULES_PATH=REGLAS-ORQUESTADOR.md
RULES_SHA=e04e653fe6b9d3f394c18dee18274090ddb79ff9

WORK_REPO=https://github.com/francogg89-ai/work-claude-l
AUDIT_REPO=https://github.com/francogg89-ai/audit-chatgpt-l

RUNTIMES:
AUDITOR_RUNTIME=ChatGPT web
CONSTRUCTOR_RUNTIME=Claude Code local en Windows

SUPERFICIES_DE_TRABAJO:
AUDITOR_WRITE_REPO=https://github.com/francogg89-ai/audit-chatgpt-l
AUDITOR_LOCAL_PATH=C:/Franco_Metodos_AI/audit-chatgpt-l
CONSTRUCTOR_WRITE_REPO=https://github.com/francogg89-ai/work-claude-l
CONSTRUCTOR_LOCAL_PATH=C:/Franco_Metodos_AI/work-claude-l
CONSTRUCTOR_READ_ROOT_LOCAL=C:/Franco_Metodos_AI

REPOS_GITHUB_DISPONIBLES:
- REPO=https://github.com/francogg89-ai/manifiestos-trabajo-ai
  FUNCION=biblioteca durable del manifiesto y de esta constitución
- REPO=https://github.com/francogg89-ai/metodo-manifiestos-ai
  SHA=452d8cce2dd36106e0efce0c957b951c713fdcc8
  FUNCION=método usado para materializar esta constitución; sólo lectura durante la ejecución
- REPO=https://github.com/francogg89-ai/work-claude-l
  FUNCION=superficie material exclusiva del CONSTRUCTOR
- REPO=https://github.com/francogg89-ai/audit-chatgpt-l
  FUNCION=superficie material exclusiva del AUDITOR
- REPO=https://github.com/francogg89-ai/orchestra-revolutions-ai
  SHA=4d88fce3ed3c87bd231c45ec60dcb713538b2514
  FUNCION=método autoritativo de ejecución; sólo lectura para este trabajo
- REPO=https://github.com/francogg89-ai/rules-orchestrator-ai
  SHA=e04e653fe6b9d3f394c18dee18274090ddb79ff9
  FUNCION=reglas autoritativas del ORQUESTADOR; sólo lectura para los actores

REPOS_LOCALES_DISPONIBLES:
- MANIFEST_LIBRARY_LOCAL=C:/Franco_Metodos_AI/manifiestos-trabajo-ai
- METODO_MANIFIESTOS_LOCAL=C:/Franco_Metodos_AI/metodo-manifiestos-ai
- WORK_LOCAL=C:/Franco_Metodos_AI/work-claude-l
- AUDIT_LOCAL=C:/Franco_Metodos_AI/audit-chatgpt-l
- REVOLUTIONS_LOCAL=C:/Franco_Metodos_AI/orchestra-revolutions-ai
- RULES_ORCHESTRATOR_LOCAL=C:/Franco_Metodos_AI/rules-orchestrator-ai

SOURCE_REPOS:
- REPO=https://github.com/francogg89-ai/orchestra-revolutions-ai
  SHA=4d88fce3ed3c87bd231c45ec60dcb713538b2514
  FUNCION=método autoritativo de ejecución
- REPO=https://github.com/francogg89-ai/rules-orchestrator-ai
  SHA=e04e653fe6b9d3f394c18dee18274090ddb79ff9
  FUNCION=reglas autoritativas del transporte
- REPO=https://github.com/francogg89-ai/metodo-manifiestos-ai
  SHA=452d8cce2dd36106e0efce0c957b951c713fdcc8
  FUNCION=método de constitución usado para este trabajo
- REPO=https://github.com/francogg89-ai/manifiestos-trabajo-ai
  SHA=294b8de4ba7b11ba0272bae29910d1a12ae29d3e
  FUNCION=biblioteca que contiene el manifiesto humano aprobado

ROOT_LOCAL=C:/Franco_Metodos_AI

LOCAL_PATHS:
MANIFEST_LIBRARY=C:/Franco_Metodos_AI/manifiestos-trabajo-ai
METODO_MANIFIESTOS=C:/Franco_Metodos_AI/metodo-manifiestos-ai
WORK=C:/Franco_Metodos_AI/work-claude-l
AUDIT=C:/Franco_Metodos_AI/audit-chatgpt-l
REVOLUTIONS=C:/Franco_Metodos_AI/orchestra-revolutions-ai
RULES_ORCHESTRATOR=C:/Franco_Metodos_AI/rules-orchestrator-ai

ENTORNOS_RELEVANTES:
- AUDITOR: ChatGPT web.
- El AUDITOR usa GitHub como fuente durable y no debe inferir acceso directo al filesystem local de Windows por la mera existencia de AUDITOR_LOCAL_PATH.
- CONSTRUCTOR: Claude Code local en Windows.
- El directorio exacto de trabajo material del CONSTRUCTOR es C:/Franco_Metodos_AI/work-claude-l.
- C:/Franco_Metodos_AI es raíz de localización/lectura para el CONSTRUCTOR conforme a estas capacidades; no es una superficie material general de escritura.
- No existen entornos productivos, APIs de negocio, bases de datos reales ni despliegues materiales requeridos por esta prueba.

CAPACIDADES_CONSTRUCTOR:
- Puede abrir y trabajar mediante Claude Code local en Windows exactamente en C:/Franco_Metodos_AI/work-claude-l.
- Puede sincronizar y leer los repositorios declarados necesarios para reconstruir y ejecutar el trabajo.
- Puede leer los clones locales declarados bajo C:/Franco_Metodos_AI cuando sea necesario.
- Puede ejecutar comandos locales necesarios para construir y verificar la prueba.
- Puede crear commits y publicar exclusivamente en https://github.com/francogg89-ai/work-claude-l.
- Su frontera estructural de escritura no se amplía por la existencia de otros clones o repositorios.
- No tiene autorización para modificar audit-chatgpt-l, orchestra-revolutions-ai, rules-orchestrator-ai, metodo-manifiestos-ai ni manifiestos-trabajo-ai.

CAPACIDADES_AUDITOR:
- Puede leer directamente los repositorios GitHub declarados y obtener identidades exactas desde Git.
- Puede inspeccionar independientemente el material de work-claude-l y las autoridades congeladas.
- Puede crear commits y publicar exclusivamente en https://github.com/francogg89-ai/audit-chatgpt-l.
- Puede determinar suficiencia de evidencia, defectos, veredictos, necesidades humanas, próxima acción y relevos metodológicamente habilitados conforme a REVOLUTIONS.
- No modifica el candidato de work-claude-l.
- No modifica orchestra-revolutions-ai, rules-orchestrator-ai, metodo-manifiestos-ai ni manifiestos-trabajo-ai.
- AUDITOR_LOCAL_PATH=C:/Franco_Metodos_AI/audit-chatgpt-l es una coordenada declarada y no constituye por sí misma una capacidad de acceso al filesystem desde ChatGPT web.

POLITICAS_DE_EJECUCION_INICIALES:
- El trabajo requiere primero un PLAN sometido a la decisión humana exigida por REVOLUTIONS.
- El PLAN debe contener exactamente cinco unidades: U01, U02, U03, U04 y U05.
- El trabajo material de las cinco unidades debe ser deliberadamente simple, determinista y barato de auditar.
- Después de que el AUDITOR determine materialmente terminada U01, U02, U03 o U04, debe emitir una NECESIDAD DEL HUMANO no material antes de avanzar.
- Esa necesidad debe permitir al HUMANO resolver inequívocamente entre APROBAR UNIDAD Y CONTINUAR, APROBAR UNIDAD Y RELEVAR CONSTRUCTOR, APROBAR UNIDAD Y RELEVAR AUDITOR, o no aprobar acompañando la resolución correspondiente.
- La resolución humana debe preservarse durablemente por el AUDITOR antes de continuar.
- Después de U05 debe existir un gate humano final antes del cierre y de cualquier final=true.
- La decisión principal del gate final es APROBAR CIERRE.
- No existen relevos periódicos automáticos de CONSTRUCTOR.
- No existen relevos periódicos automáticos de AUDITOR.
- La política de ambos roles es sólo relevo manual solicitado por el HUMANO en los gates constituidos.
- Un relevo manual no autoriza directamente al ORQUESTADOR a abrir fresh.
- Sólo next_instance=fresh en un sobre revolutions-hop/v1 válido autoriza una instancia nueva.
- Antes del cierre satisfactorio de U05 debe haber ocurrido al menos un relevo efectivo de CONSTRUCTOR y al menos un relevo efectivo de AUDITOR.
- Debe ejercitarse al menos una vez APROBAR UNIDAD Y CONTINUAR.
- No debe abrirse artificialmente un fresh después de U05 únicamente para cumplir un relevo sin trabajo material posterior.
- El ORQUESTADOR nunca cuenta, deriva ni decide relevos.
- El ORQUESTADOR nunca usa unit como autorización de avance o de fresh.
- Toda instancia fresh debe reconstruir desde Git conforme a REVOLUTIONS.
- Después de un fresh confirmado, la nueva instancia pasa a ser la única current elegible del rol y la anterior queda retirada.

UBICACION_Y_FRONTERAS_DE_ACTORES:
- El AUDITOR trabaja en runtime ChatGPT web.
- La superficie material exclusiva de escritura del AUDITOR es https://github.com/francogg89-ai/audit-chatgpt-l.
- AUDITOR_LOCAL_PATH=C:/Franco_Metodos_AI/audit-chatgpt-l es sólo una coordenada local declarada; no implica acceso local desde ChatGPT web.
- El CONSTRUCTOR trabaja en runtime Claude Code local en Windows.
- La superficie material exclusiva de escritura del CONSTRUCTOR es https://github.com/francogg89-ai/work-claude-l.
- El directorio local exacto de trabajo del CONSTRUCTOR es C:/Franco_Metodos_AI/work-claude-l.
- El CONSTRUCTOR puede localizar y leer las fuentes declaradas bajo C:/Franco_Metodos_AI conforme a sus capacidades.
- Los repositorios y paths GitHub/locales declarados son coordenadas de localización y lectura; no amplían por sí mismos ninguna frontera de escritura.
- work-claude-l y audit-chatgpt-l están vacíos al constituir este trabajo; no existe WORK_SHA, AUDIT_SHA ni BOOTSTRAP_SHA previo que deba inventarse.

Esta constitución es una fuente durable de arranque. No sustituye al manifiesto, a REVOLUTIONS ni
a REGLAS-ORQUESTADOR.md. Las identidades Git congeladas determinan las autoridades exactas de esta
ejecución.

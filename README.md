# Marcos Recio Sánchez

**AI Solutions & Automation Engineer** · Valencia, España

Construyo sistemas de IA agéntica que ejecutan procesos de negocio reales: no notebooks ni envoltorios sobre una API de modelo, sino software que aguanta restricciones de verdad — aislamiento multi-tenant, cumplimiento fiscal español, y la regla de que un sistema autónomo nunca puede mentirte sobre sus propios resultados.

Llegué a la ingeniería por la puerta de atrás. Vengo de logística y administración — AS400 en DB Schenker, documentación portuaria en Cemesa, procesos internos en Improving — es decir, pasé años siendo el usuario que sufre el software de gestión mal hecho. Después aprendí a construirlo. **AutomatizaCore existe porque viví los problemas que resuelve.**

Busco puestos de **automatización de procesos de negocio con IA**: consultoras, integradores, software de gestión y ecosistema de gestorías y ERPs.

---

## Proyecto principal

### [AutomatizaCore](https://github.com/Llicklair/Automatiza-Core) — ERP español con IA agéntica, instalación local

🔗 **[Landing y demo en vídeo](https://llicklair.github.io/Automatiza-Core_landing)** · *en acceso anticipado*

Plataforma de gestión completa — facturación, contabilidad, banca, CRM, RRHH y compliance fiscal Verifactu — operada en lenguaje natural, donde 14 agentes de dominio ejecutan las acciones de negocio reales.

- **Arquitectura multiagente** orquestada con LangGraph: clasificar → planificar → validar → despachar, con empleados de IA personalizables (~45 skills).
- **Sistema RAG propio** con pgvector y embeddings offline (BAAI/bge-m3), con citas a la fuente.
- **Motor de automatizaciones** con triggers por tiempo y evento, integraciones OAuth (Gmail, Outlook, Drive, OneDrive) vía APIs, JSON y webhooks.
- **Multi-tenant** con filtrado estricto por `tenant_id` y puertas de aprobación humana antes de cualquier acción con efectos.
- **Agnóstico de proveedor**: Claude, Gemini y OpenAI con fallback automático.

Diseño e implementación end-to-end, en solitario.

`~67k líneas de backend · 900+ commits · 69 rutas de API · 109 páginas · Python · FastAPI · LangGraph · PostgreSQL/pgvector · Next.js · Electron`

---

## Herramientas para agentes de código

**[galaxy-brain](https://github.com/Llicklair/galaxy-brain)** — el andamio determinista sobre el que debería apoyarse un agente
Hechos sobre tu código Python — dónde murió y con qué estado, qué forma tiene, quién llama a quién, qué movió un diff — en milisegundos, offline y **sin ningún modelo en el camino**. Captura automática de errores vía `sys.excepthook` (no hace falta reproducir el fallo) más grafos de módulos, símbolos y llamadas, y análisis de impacto de cambios. Hook de pre-commit en modo trinquete: la deuda heredada pasa, la nueva no.
`Python ≥3.9 · 278 commits · 8.4k líneas de código / 6.4k de tests · 445 tests · cero dependencias en runtime`

**[Forja](https://github.com/Llicklair/forja)** — bucle autónomo de revisión de código
Pipeline finder→tester→fixer→evaluator que recorre un proyecto entero a través de seis lentes rotatorias: corrección, seguridad, concurrencia, manejo de errores, huecos de test y rendimiento. Verificación test-first, evaluador independiente como puerta, modos con control de coste y una regla dura: nunca auto-mergea.
`Plugin de Claude Code · MIT`

**[El Consejo de los 7 Sabios](https://github.com/Llicklair/consejo-7-sabios)** — 7 agentes con visiones opuestas debaten tu código
Siete perspectivas enfrentadas discuten hasta alcanzar consenso, un juez sintetiza el plan y se ejecuta. Con animación pixel-art en terminal, porque las herramientas que da gusto mirar son las que de verdad acabas usando.
`Python · pytest · MIT`

**[invest-ll](https://github.com/Llicklair/invest-ll)** — sistema de inversión construido sobre una restricción
Propone operaciones exactas en bolsa y cripto. El principio que va por delante de todo: *el sistema no puede mentirte sobre sus propios resultados.* Sin sesgo de mirada al futuro, simulación realista, estrategias comparables, seguridad del capital por defecto.
`Python · pytest · ruff · pyright`

---

## Cómo trabajo

- **Los hechos deciden, las aproximaciones informan.** Todo aquello sobre lo que actúa un agente debería estar medido, no inferido. Por eso galaxy-brain no tiene ningún modelo en la ruta caliente.
- **Tests antes que confianza.** Ratio casi 1:1 de test a código en el harness; pytest, Playwright E2E, `ruff` y `pyright` como puerta de cada integración. Un sistema autónomo sin verificación es solo una forma rápida de equivocarse.
- **Restricciones primero.** La ingeniería interesante empieza cuando escribes lo que el sistema *no* tiene permitido hacer.
- **Restar antes que pulir.** El coste de mantenimiento crece con el número de componentes, así que la respuesta por defecto a un componente nuevo es no.
- **Evidencia antes que folclore.** Las decisiones de diseño citan datos medidos, y los resultados negativos también se escriben.

**IA y automatización:** agentes de IA · arquitecturas multiagente · LangGraph · RAG y embeddings · APIs, JSON, webhooks · OAuth · Claude, Gemini, OpenAI
**Desarrollo:** Python · FastAPI · SQLAlchemy · PostgreSQL + pgvector · TypeScript · Next.js · React · Electron · Docker
**Sistemas de gestión:** AS400 · IWIS · gestión documental
**Idiomas:** español nativo · inglés C1

---

## Contacto

📧 marcosreciosanchez@gmail.com · 🌐 [AutomatizaCore](https://llicklair.github.io/Automatiza-Core_landing) · 📍 Valencia, España

---
<details>
<summary><b>🇬🇧 English summary</b></summary>

<br>

**AI Solutions & Automation Engineer** based in Valencia, Spain.

I build agentic AI systems that execute real business processes. My main project, **[AutomatizaCore](https://llicklair.github.io/Automatiza-Core_landing)**, is a Spanish ERP — invoicing, accounting, banking, CRM, HR, tax compliance — operated in natural language, where 14 domain agents orchestrated with LangGraph execute the actual business actions. Custom RAG with pgvector, offline embeddings, multi-tenant isolation, human approval gates, provider-agnostic across Claude/Gemini/OpenAI. ~67k LOC backend, 900+ commits, designed and shipped end-to-end solo.

I also build tooling for AI coding agents: **[galaxy-brain](https://github.com/Llicklair/galaxy-brain)** is a deterministic code-analysis harness (445 tests, 8.4k LOC source / 6.4k LOC tests, zero runtime dependencies, no model in the loop), **[Forja](https://github.com/Llicklair/forja)** an autonomous code review loop, and **[Consejo de los 7 Sabios](https://github.com/Llicklair/consejo-7-sabios)** a multi-agent adversarial review system.

I came to engineering from logistics and administration — AS400, port documentation, internal process systems — which means I spent years on the receiving end of badly built business software before I learned to build it.

**Stack:** Python · FastAPI · LangGraph · PostgreSQL/pgvector · Next.js · TypeScript · Electron · Docker
**Languages:** Spanish (native) · English (C1)

</details>

# 🤖 HR Buddy — AI Agent for Human Resources

HR Buddy es un asistente inteligente de Recursos Humanos desarrollado con n8n, Telegram, MySQL y modelos de IA.
El objetivo del proyecto es construir una arquitectura eficiente, segura y escalable para automatizar consultas internas de empleados.

---

# 🚀 Características

* 🔐 Validación de usuarios mediante `telegram_id`
* 🧠 Clasificación inteligente de intenciones antes del agente IA
* ⚡ Reducción de consumo de tokens y latencia
* 🗄️ Integración con MySQL
* 📚 Implementación de RAG + Vector Store
* 🤖 Integración con modelos LLM usando Cohere
* 💬 Automatización vía Telegram
* 🧩 Arquitectura modular en n8n

---

# 🔐 Seguridad

Antes de activar el agente IA principal:

1. Se valida el `telegram_id` del usuario en MySQL
2. Si el usuario no existe:

   * el flujo se corta inmediatamente
3. Si existe:

   * se recupera la información del empleado
   * se habilita el acceso al sistema

Esto permite:

* reducir costos innecesarios de IA
* minimizar superficie de ataque
* evitar accesos externos
* optimizar consumo de tokens

---

# 🧠 Clasificación Inteligente

El sistema incorpora un clasificador de intención utilizando un Basic LLM + Switch.

Las categorías son:

* `SALUDO`
* `RRHH`
* `FUERA_DE_REGLA`

Dependiendo del resultado:

✅ respuestas instantáneas
✅ menor latencia
✅ menos alucinaciones
✅ IA avanzada solo cuando es necesario

---

# 🛠️ Stack Tecnológico

* n8n
* Telegram API
* MySQL
* Cohere LLM
* Embeddings
* Vector Store
* RAG (Retrieval-Augmented Generation)

---

# 📂 Estructura del Proyecto

```bash
/workflows
    INM_AG_mejoras1.json
```

---

# 📥 Cómo usar

1. Clona el repositorio
2. Importa el archivo `.json` en n8n
3. Configura:

   * credenciales MySQL
   * Telegram Bot
   * Cohere API
4. Ejecuta el workflow

---

# 📌 Objetivo

Diseñar agentes IA más seguros, eficientes y preparados para entornos empresariales reales.

---

# 📜 Licencia

MIT License

# Qwiki Management System Handbook

> **A modular knowledge management system for structured FAQs, conversational journeys, and dialogue flows—built for brands, AI assistants, and customer experience teams.**

---

## What is a Qwiki?

A **Qwiki** is a modular, structured knowledge asset such as an FAQ, step-by-step customer journey, or dialogue flow—designed to be both human-readable and machine-readable.
Qwikis make it easy for brands and teams to deliver consistent, compliant, and helpful answers across websites, AI assistants, chatbots, search and answer engines.

---

## What is the Qwiki Management System?

The Qwiki Management System is a flexible, scalable approach for managing your organization’s most valuable knowledge—FAQs, customer journeys, dialogue flows, and digital brand assets.
It’s designed for **collaborative editing** (using your preferred tools—spreadsheets, databases, or knowledge platforms) and **publishing (with MkDocs)**, supporting both **human-readable documentation** and **machine-readable (JSON-LD) export** for AI, search engines, and answer platforms.

---

## Key Features

* **Qwiki Templates:** Manage structured FAQs, dialogue flows, customer journeys, assets, and personas.
* **Flexible Steps:** Model single Q\&A or complex multi-turn conversations.
* **Tool-Agnostic Data Entry:** Use Airtable, Google Sheets, Notion, or any structured editor for your workflow.
* **MkDocs-Ready:** Publish human-friendly, searchable handbooks or API docs.
* **AI & LLM Friendly:** Export to JSON-LD for AI ingestion, answer engines, and knowledge graphs.
* **Governance & Audit:** Track status, ownership, review notes, and version history.
* **Composable:** Link Qwikis to assets, personas, and each other.

---

## Handbook Structure

This handbook covers:

* **1. Introduction**: What is a Qwiki and why it matters.
* **2. System Overview**: Data model, workflow, and toolchain.
* **3. Creating a Qwiki**: Field-by-field authoring guide.
* **4. Review & Governance**: Approval and audit workflow.
* **5. Exporting & Publishing**: JSON-LD, MkDocs, and indexing.
* **6. Advanced Usage**: Integrations with Meilisearch, LLMs, etc.
* **7. Templates & Examples**: FAQs, dialogue flows, sample JSON-LD.
* **8. References**: Brando Schema, Schema.org, Airtable, MkDocs docs, etc.

---

## 🛠️ Quickstart

1. **Clone this repo**
2. **Customize your Qwiki fields and templates (see `/docs` and `/templates`).**
3. **Build your Qwiki library using Airtable, Google Sheets, Notion, or your favorite tool.**
4. **Export as Markdown and JSON-LD for MkDocs.**
5. **Publish your handbook or docs site with [MkDocs](https://www.mkdocs.org/).**

---

## Example: Qwiki Dialogue Flow

```json
{
  "@context": [
    "https://schema.org/",
    "https://brandoschema.com/context.jsonld"
  ],
  "@type": "QwikiDialogueFlow",
  "id": "QW-001",
  "name": "School Shoe Purchase Journey – Young Mum",
  "persona": {
    "role": "Customer",
    "profile": "Young mum, time-pressed, values comfort, price, and durability for her 7-year-old son"
  },
  "description": "A conversational journey for a parent buying school shoes online, covering discovery, fit, checkout, and support.",
  "steps": [
    {
      "stepId": "QW-001-001",
      "order": 1,
      "userUtterance": "What’s the best place to buy school shoes online?",
      "agentResponse": "We recommend Clarks, Schuh, and John Lewis. Are you looking for a specific size or style?",
      "parameters": [],
      "escalation": false
    },
    {
      "stepId": "QW-001-002",
      "order": 2,
      "userUtterance": "He’s 7, size 2.5 in black.",
      "agentResponse": "Classic black, UK size 2.5, is available at both Clarks and John Lewis. Would you like to see sizing guides, read parent reviews, or go straight to checkout?",
      "parameters": [
        {"name": "shoeSize", "value": "2.5", "entityType": "Size"},
        {"name": "color", "value": "black", "entityType": "Color"}
      ],
      "escalation": false
    },
    {
      "stepId": "QW-001-003",
      "order": 3,
      "userUtterance": "Show me reviews.",
      "agentResponse": "Here are parent reviews for Clarks’ black school shoes in size 2.5: ⭐⭐⭐⭐⭐ ‘Very durable!’ Would you like to proceed to purchase or ask about returns?",
      "parameters": [],
      "escalation": false
    },
    {
      "stepId": "QW-001-004",
      "order": 4,
      "userUtterance": "What is your returns policy?",
      "agentResponse": "You can return any unworn school shoes within 30 days for a full refund. Would you like to add these to your basket?",
      "parameters": [],
      "escalation": false
    },
    {
      "stepId": "QW-001-005",
      "order": 5,
      "userUtterance": "Yes, add to basket.",
      "agentResponse": "Done! Would you like to check out now or continue shopping?",
      "parameters": [],
      "escalation": false
    },
    {
      "stepId": "QW-001-006",
      "order": 6,
      "userUtterance": "I have a question about shoe width.",
      "agentResponse": "Of course! Are you looking for a standard or wide fit? I can show available options or connect you to a fitting specialist.",
      "parameters": [
        {"name": "fit", "entityType": "Fit", "prompt": "Standard or wide fit?"}
      ],
      "escalation": false
    },
    {
      "stepId": "QW-001-007",
      "order": 7,
      "userUtterance": "Can I talk to a human?",
      "agentResponse": "No problem—connecting you to a customer support specialist now.",
      "parameters": [],
      "escalation": true
    }
  ],
  "escalationPolicy": "If the customer requests help or seems confused, escalate to a human agent for support.",
  "feedbackPrompt": "Did you find this school shoe shopping journey easy and helpful? Please rate your experience."
}

```

---

## Who is this for?

* **Brand managers and CX teams:** Maintain consistent, on-brand knowledge everywhere.
* **AI & data teams:** Power LLMs, RAG, search, and chatbots with structured, trusted sources.
* **Compliance & governance:** Ensure auditability and traceability of all answers and journeys.
* **Content & docs teams:** Rapidly produce and publish living documentation.

---

## Contributing

Found a bug, want to propose a new template, or need help integrating with your stack?
**Open an issue or submit a pull request.**

---

## References

* [Brando Schema](https://brandoschema.com/)
* [Schema.org](https://schema.org/)
* [Airtable](https://airtable.com/)
* [MkDocs](https://www.mkdocs.org/)
* [Meilisearch](https://www.meilisearch.com/)

---

*Build once. Deploy everywhere.
Your brand’s answers—clear, compliant, and ready for the age of AI.*

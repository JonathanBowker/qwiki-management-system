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
  "@context": ["https://schema.org/", "https://brandoschema.com/context.jsonld"],
  "@type": "QwikiDialogueFlow",
  "id": "QW-001",
  "name": "School Shoe Purchase Journey – Young Mum",
  "persona": {
    "role": "Customer",
    "profile": "Young mum, time-pressed, values comfort, price, and durability for her 7-year-old son"
  },
  "steps": [
    {
      "stepId": "QW-001-001",
      "userUtterance": "What’s the best place to buy school shoes online?",
      "agentResponse": "We recommend Clarks, Schuh, and John Lewis. Are you looking for a specific size or style?"
    },
    {
      "stepId": "QW-001-002",
      "userUtterance": "He’s 7, size 2.5 in black.",
      "agentResponse": "Classic black, UK size 2.5, is available. Want to know about free returns or see parent reviews?"
    }
    // more steps...
  ]
}
```

---

## 👥 Who is this for?

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

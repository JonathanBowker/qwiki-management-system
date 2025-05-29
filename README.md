# Qwiki Management System Handbook

Welcome to the Qwiki Management System Handbook. This guide details how to create, review, and publish high-quality Qwikis—structured knowledge assets for brands, AI, and customer journeys.

---

## 1. Introduction

**What is a Qwiki?**

A Qwiki is a modular, structured knowledge unit—such as a FAQ, customer journey, or dialogue flow—designed for both human readers and machine consumption (AI, LLMs, chatbots). Qwikis help ensure your brand answers are accurate, compliant, and on-brand across every channel.

---

## 2. System Overview

### Qwiki Types

- **FAQ Qwiki**: Single Q&A pairs for rapid answers.
- **Dialogue Flow Qwiki**: Step-by-step conversational journeys (multi-turn interactions).
- **Asset Qwiki**: Links to digital assets (logos, PDFs, templates).
- **Persona Qwiki**: Structured customer or agent profiles.

### Data Structure

Each Qwiki is defined by:
- **Qwiki ID**: Unique identifier (e.g., QW-001)
- **Title**
- **Type**: FAQ, Dialogue Flow, etc.
- **Persona**: Who is this Qwiki for?
- **Status**: Draft, Review, Published, Archived
- **Steps/Intents**: For Dialogue Flows
- **JSON-LD**: Machine-readable export
- **Linked Assets**: Attachments, images, etc.

### Toolchain Overview

- **Airtable**: Collaborative editing and review
- **MkDocs**: Publishing for humans and search engines
- **JSON-LD**: Publishing for AI and answer engines

---

## 3. Creating a Qwiki

### Authoring Guidelines

- Use clear, inclusive, and on-brand language.
- Follow the dialogue flow schema for conversational journeys.
- Always attribute each Qwiki to a persona and intent.

### Field-by-Field Guide

| Field Name            | Description                                   |
|-----------------------|-----------------------------------------------|
| Qwiki ID              | Unique code (e.g., QW-001)                    |
| Title                 | Brief, descriptive name                       |
| Qwiki Type            | FAQ, Dialogue Flow, etc.                      |
| Persona               | Target persona for the Qwiki                  |
| Description           | Summary of what this Qwiki covers             |
| Status                | Draft, Review, Published, etc.                |
| Steps/Intents         | (Dialogue Flows) List of dialogue steps/intents|
| JSON-LD Export        | Machine-readable structured data              |
| Linked Assets         | Links or files                                |

---

## 4. Review and Governance

- Every Qwiki must be reviewed by a subject matter expert and compliance lead.
- Major changes are versioned (e.g., v1.0, v1.1) and include a changelog.
- Use the “Review Notes” field for audit trail.

---

## 5. Exporting and Publishing

### Exporting from Airtable

- Approved Qwikis are exported as JSON-LD.
- Use an automation (Zapier, Make, or script) to push Qwikis to the MkDocs repo or publishing server.

### Publishing with MkDocs

- Store each Qwiki as a markdown file.
- Attach the JSON-LD as an embedded block or downloadable file.
- Update the search index and sitemap for discoverability.

---

## 6. Advanced Usage

- **Assets**: Link logos, PDFs, templates to relevant Qwikis for complete context.
- **Personas**: Standardize persona Qwikis for customer journeys and chatbot tuning.
- **Meilisearch/LLM Integration**: Sync your Qwiki library for instant search and AI answer generation.

---

## 7. Templates & Examples

### FAQ Qwiki Example

```markdown
**Qwiki ID:** QW-002  
**Title:** Returns Policy  
**Type:** FAQ  
**Question:** What is your returns policy?  
**Answer:** You can return any item within 30 days for a full refund.

**JSON-LD:**
```json
{
  "@context": ["https://schema.org/", "https://brandoschema.com/context.jsonld"],
  "@type": "schema:Question",
  "name": "What is your returns policy?",
  "acceptedAnswer": {
    "@type": "schema:Answer",
    "text": "You can return any item within 30 days for a full refund."
  }
}

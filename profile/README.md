## WA Validator — WhatsApp Number Checker API

**Check if a phone number is registered on WhatsApp — one number or 100 at a time, in real time.**

WA Validator is a WhatsApp number validation API for developers, marketers and CRM teams. Send a phone number in international format and get back `valid` (has WhatsApp) or `invalid` (no WhatsApp) in the same HTTP response — no queue, no polling, no webhooks. Clean contact lists before a WhatsApp campaign, validate leads at signup, and stop paying to message numbers that will never receive it.

[**Website**](https://wavalidator.com) · [**API documentation**](https://wavalidator.com/api-docs/) · [**MCP server**](https://wavalidator.com/mcp-docs/) · [**Pricing**](https://wavalidator.com/pricing/) · [**Create a free account**](https://wavalidator.com/signup/) · [**API status**](https://wavalidator.com/status/)

### Official repositories

| Repository | What it does | Endpoint | Contents |
|---|---|---|---|
| **[whatsapp-number-checker-api](https://github.com/wavalidator/whatsapp-number-checker-api)** | Check one phone number for a WhatsApp account | `POST /api/v1/validate/` | OpenAPI 3.0 spec, `product.json`, `llms.txt`, examples in 7 languages |
| **[whatsapp-bulk-checker-api](https://github.com/wavalidator/whatsapp-bulk-checker-api)** | Check up to 100 numbers in one request | `POST /api/v1/bulk-check/` | OpenAPI 3.0 spec, `product.json`, `llms.txt`, examples in 7 languages, CSV list cleaner |
| **[whatsapp-checker-mcp-server](https://github.com/wavalidator/whatsapp-checker-mcp-server)** | Let Claude, ChatGPT and Cursor check WhatsApp numbers | `POST /mcp/` | Config for Claude Code, Claude Desktop, Cursor and any MCP client |
| [wavalidator-resources](https://github.com/wavalidator/wavalidator-resources) | Guides and developer articles | — | WhatsApp list cleaning, lead validation, number formatting, rate-limit handling |

Every example repository ships runnable code in **Python, Node.js, PHP, Go, Java, C# and cURL/Shell**, an **OpenAPI 3.0** contract you can import into Postman or Insomnia, and an `llms.txt` file so AI coding assistants can read the API in one pass.

### Quick start

```bash
curl -X POST https://wavalidator.com/api/v1/validate/ \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"phone_number": "14155551234"}'
```

```json
{ "phone_number": "14155551234", "status": "valid", "credits_remaining": 99 }
```

### Single check, bulk check or MCP?

- **Single check** (`/api/v1/validate/`) — one number per request. Use it in a signup form, a checkout step, a CRM webhook or a live lookup.
- **Bulk check** (`/api/v1/bulk-check/`) — up to **100 numbers per request**. Use it to clean a lead list, deduplicate a WhatsApp marketing audience or verify a CSV export.
- **MCP server** (`/mcp/`) — the same two checks exposed as tools for AI assistants. Ask *"which of these 50 leads have WhatsApp?"* in Claude or Cursor and get the answer in chat.

### One key, one balance

Every endpoint uses the same API key, the same `Authorization: Bearer` header and the same credit balance. **1 credit = 1 number checked.** Requests that fail on our side (`status: "error"`) are not charged.

### Use cases

WhatsApp marketing list cleaning · lead validation and lead scoring · CRM enrichment (HubSpot, Salesforce, Zoho) · e-commerce checkout and COD order verification · fake signup and fraud prevention · WhatsApp Business API cost reduction · call-center and sales-team prospecting · Google Sheets and Excel list verification.

### Responsible use

Results are point-in-time signals: they say whether a number had a WhatsApp account at the moment of the check. They are not identity verification and not consent to contact anyone. Only check numbers you are authorized to process and follow local privacy law (GDPR, CCPA) and WhatsApp's terms. WhatsApp is a trademark of Meta Platforms, Inc.; WA Validator is an independent service and is not affiliated with or endorsed by Meta.

<sub>Keywords: WhatsApp number checker API · WhatsApp number validator · check if a number has WhatsApp · WhatsApp verification API · bulk WhatsApp checker · WhatsApp number filter · WhatsApp lead validation · phone number validation API · WhatsApp MCP server</sub>

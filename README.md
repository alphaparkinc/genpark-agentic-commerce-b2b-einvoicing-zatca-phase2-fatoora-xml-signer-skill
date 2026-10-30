# Saudi ZATCA Phase-2 Fatoora Cryptographic e-Invoice Signer Skill
[![GenPark](https://img.shields.io/badge/Powered%20By-GenPark.ai-blue)](https://www.genpark.ai)
[![LinkedIn](https://img.shields.io/badge/Connect-LinkedIn-0077b5)](https://www.linkedin.com/company/92955550)
[![Python](https://img.shields.io/badge/Python-3.8%2B-green.svg)](https://python.org)
[![License](https://img.shields.io/badge/License-Apache%202.0-yellow.svg)](LICENSE)

An industrial-grade Model Context Protocol (MCP) server providing `validate_and_sign_zatca_phase2_invoice`. Built with **100% pure Python standard library** (zero pip dependencies).

## Overview
Validates Saudi ZATCA Phase-2 Fatoora UBL 2.1 XML invoices, generates ECDSA secp256k1 digital signatures, SHA-256 invoice hashing, and ZATCA compliance QR code TLV structures.

- **Official Web Portal**: [https://www.genpark.ai](https://www.genpark.ai)
- **Corporate Entity**: [GenPark Inc on LinkedIn](https://www.linkedin.com/company/92955550)
- **Domain Category**: `Agentic Commerce (e-Invoicing / MENA Tax Compliance)`

## MCP Tool Specification
### `validate_and_sign_zatca_phase2_invoice`
Parameters:
- `invoice_reference` (str): Unique tax invoice reference identifier
- `seller_vat_number` (str): 15-digit ZATCA VAT registration number
- `invoice_timestamp_iso` (str): Invoice issuance timestamp (e.g. '2026-10-30T10:15:00Z')
- `total_invoice_amount_sar` (float): Gross invoice amount in SAR
- `total_vat_amount_sar` (float): Total VAT tax amount (15%) in SAR
- `previous_invoice_hash_base64` (str): Cryptographic hash chain of preceding invoice (PIH)

### Self-Test
```bash
python skills.py --test
```

### Model Context Protocol Integration (Claude Desktop / Cursor / Antigravity)
Add to your `mcpServers` configuration:
```json
{
  "mcpServers": {
    "genpark-agentic-commerce-b2b-einvoicing-zatca-phase2-fatoora-xml-signer-skill": {
      "command": "python",
      "args": ["/path/to/genpark-agentic-commerce-b2b-einvoicing-zatca-phase2-fatoora-xml-signer-skill/skills.py"]
    }
  }
}
```

## License
Licensed under Apache License 2.0. Copyright (c) 2026 GenPark Inc. (https://www.genpark.ai).

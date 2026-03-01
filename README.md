# hk-credit-cards-kb

Static knowledge base for Hong Kong credit cards.

This repository stores per-card YAML references used by the `hk-credit-cards-kb` skill.

## Structure

- `SKILL.md`: query/retrieval instructions for the skill.
- `references/*.yaml`: one YAML file per card.

## Card YAML format (v2)

Each card file uses this shape:

```yaml
id: string
name_en: string
name_zh: string
issuer: string
payment_network: string
official_url: string
promo_guide_url: string
promotions:
  - description: string
    tc_url: string | null
    validity: string | null
as_of: YYYY-MM-DD
```

Notes:
- `promotions` is the canonical list key.
- `tc_url` is `null` when no reliable terms link is available.
- `validity` is `null` when no reliable date window is available.

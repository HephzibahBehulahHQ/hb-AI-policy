# Repository reorganization migration manifest

## Audit basis

Audited on the default branches before migration. All text files were reviewed. Binary assets were identified by path and size and are preserved unchanged; no images, logos, colors, themes or application code are modified by this program.

## Canonical ownership decisions

| Source | Disposition |
| --- | --- |
| `hb-AI-policy/README.md` | Modularized here into focused global policy documents and a product template. |
| `hb-design-system/AGENTS.md`, `README_AI.md`, `SYSTEM_PROMPT.md` | Design-system instructions become repository-scoped; global agent rules move to this canonical policy repository. |
| `hb-design-system/components/AdigunBot/AGENTS.md` | Split in the design system into a concise entry point and focused component standards. |
| `templates/universal-product/product.config.json` | Made product-neutral; AdigunSPs values move to an example. |
| Corporate and division READMEs | Retained as the authoritative public and domain descriptions; scoped guidance is added alongside them. |

## File-by-file disposition

| Repository | Existing path | Action |
| --- | --- | --- |
| Corporate website | `README.md`, `index.html`, `assets/images/.gitkeep`, `assets/images/hephzibah-behulah-banner.jpg` | Retain; documentation links and repository guidance only. |
| hb-AI-policy | `README.md` | Replace monolith with index; preserve requirements in `policies/`, `standards/` and `templates/`. |
| hb-design-system | `AGENTS.md`, `README.md`, `README_AI.md`, `SYSTEM_PROMPT.md`, `assets/corporate/README.md`, `assets/corporate/hephzibah-behulah-official.jpg`, `components/AdigunBot/AGENTS.md`, `docs/brand-and-product-naming.md`, `templates/universal-product/README.md`, `templates/universal-product/product.config.json`, `tokens/brands.json`, `tokens/corporate.json` | Retain assets and tokens unchanged; scope docs; split component standard; replace product-specific template defaults with example. |
| hb-elektroniker | `README.md` | Retain; add scoped agent and engineering guidance. |
| hb-trading | `README.md` | Retain; add scoped agent and financial guidance. |
| hb-evangelism | `README.md` | Retain; add scoped agent and faith-content guidance. |
| hb-politics | `README.md` | Retain; add scoped agent and editorial guidance. |
| hb-artificial-intelligence | `README.md` | Retain; add scoped agent and responsible-technology guidance. |

## Constraints

No application source, deployment configuration, visual token, color, theme, accent, image, picture, logo, mission or company identity is changed. All changes use dedicated branches and pull requests; no direct merge or deployment is included.

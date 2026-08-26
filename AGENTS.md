# Momentmade Skills

## Purpose

This repository is a community catalog of image-generation art Skills and representative outputs. It helps people discover a visual direction, understand what a Skill can produce, and use that Skill with an AI tool of their choice.

Momentmade Skills is an independent, personal, public, non-commercial catalog. It stands on its own and has no operational, organizational, promotional, or commercial relationship with any other product, service, company, or project. The name `Momentmade` identifies this catalog only.

This repository does not generate images, proxy model calls, consume a user's model allowance, sell model access, or provide application functionality. People use listed Skills independently with their own compatible AI tools.

Keep this repository useful as durable public knowledge rather than turning it into an application, marketplace, prompt scraper, or model orchestration system.

## Core Principles

- Preserve authorship, provenance, and license information.
- Never assume that public availability means permission to copy or redistribute.
- Separate hosted Skills from external catalog entries.
- Prefer a small number of strong, representative outputs over large uncurated galleries.
- Describe observable visual qualities, composition, materials, and constraints. Do not rely primarily on an artist's name, a brand name, or vague style labels.
- Keep Skills understandable and portable. Do not require secrets, hidden files, private services, arbitrary code execution, or remote instructions.
- Do not claim that a Skill guarantees identity, typography, layout, product, or pixel-perfect preservation.

## Repository Boundary

This repository may contain:

1. **Hosted Skills** whose full instructions and declared assets may legally be redistributed here.
2. **External catalog entries** that point to Skills hosted by their original authors when redistribution is unavailable, unclear, or restricted.
3. Repository documentation, schemas, validation, and catalog-generation tooling directly needed to maintain the collection.

This repository must not contain:

- A hosted image-generation service or provider API integration.
- Product, application, canvas, or unrelated service code.
- Authentication, subscriptions, payments, credits, or usage metering.
- Copied paid, private, personal-use-only, non-redistributable, or unlicensed Skill contents.
- Model credentials, API keys, cookies, access tokens, personal data, or unpublished prompts.
- Community uploads that have not been reviewed for provenance, license, safety, and basic quality.

## Hosted Skills

Store a hosted Skill under an immutable lowercase kebab-case ID:

```text
skills/
└── <skill-id>/
    ├── SKILL.md
    ├── cover.webp
    └── examples/
        ├── example-01.webp
        └── example-02.webp
```

Rules:

- The directory name is the stable Skill ID. Do not duplicate or casually rename it.
- `SKILL.md` is required.
- `cover.webp` is required for a published Skill.
- `examples/` is optional and may contain zero to four representative WebP outputs.
- Asset paths must be relative to the Skill directory. Do not use remote images as hosted assets.
- Do not add unrelated source files, scripts, archives, checkpoints, model weights, or training data inside a Skill directory.
- Keep images reasonably compressed and suitable for repository review. Do not commit original private inputs or unnecessary full-resolution generation files.

### Required frontmatter

Every hosted `SKILL.md` must begin with YAML frontmatter containing at least:

```yaml
---
name: Example Skill
description: A concise explanation of the visual result and intended use.
author:
  name: Original Author
  url: https://example.com/author
license:
  id: MIT
  url: https://example.com/original-license
source_url: https://example.com/original-skill
tags:
  - printmaking
  - geometric
cover: cover.webp
examples:
  - src: examples/example-01.webp
    alt: A concise, factual description of the example image.
---
```

Field rules:

- `name` and `description` are required and must be written for people browsing a catalog.
- `author.name` is required. `author.url` is strongly preferred.
- `license.id` is required. Use a valid SPDX identifier when one exists. For a custom license, use a concise stable name and provide `license.url`.
- `source_url` is required when the Skill originated elsewhere or is derived from another published Skill. It may be omitted only for an original contribution first published in this repository.
- `tags` must contain one to five unique lowercase kebab-case values.
- `cover` must resolve to the local `cover.webp`.
- `examples` may be omitted or contain zero to four local WebP entries. Every entry requires useful alt text.
- Additional fields may describe accepted text or image inputs and expected output, but must not expose provider-specific controls as user requirements unless the Skill genuinely depends on them.

### Instruction quality

The body of `SKILL.md` must be usable as complete art-direction instructions. It should define:

- The intended visual language and emotional register.
- Subject interpretation and composition rules.
- Color, typography, material, texture, and lighting rules when relevant.
- What may vary and what should remain invariant when references are supplied.
- Hard avoids and common failure modes.
- Expected output framing, aspect-ratio guidance, and background behavior when relevant.
- How to turn the user's short idea or reference image into a complete final image-generation prompt.

Do not write instructions that attempt to call tools, download remote dependencies, read unrelated files, override an agent's safety rules, or disclose hidden system information.

## External Catalog Entries

If a Skill cannot legally or clearly be redistributed, do not copy its `SKILL.md`, examples, cover, or paid contents. Create a metadata-only entry instead:

```text
catalog/
└── <skill-id>.yaml
```

Use this shape:

```yaml
kind: external
name: Example External Skill
description: A factual summary written by the catalog contributor.
author:
  name: Original Author
  url: https://example.com/author
source_url: https://example.com/original-skill
license:
  name: Personal use free; commercial license required
  url: https://example.com/license
  redistribution: false
  commercial_use: paid
tags:
  - collage
  - editorial
```

External-entry rules:

- Link to the canonical author-controlled source, not a repost or scraped mirror.
- Write an original factual description; do not copy substantial marketing or instruction text.
- Record the license as published by the author. Do not reinterpret a restricted license as MIT.
- `commercial_use` should be `allowed`, `paid`, `prohibited`, or `unknown` based on explicit source information.
- If redistribution or commercial terms are unclear, record `unknown` and keep only metadata and a link.
- Do not download or mirror example images unless their separate license permits it.
- Attribution is required catalog metadata, but attribution alone is not permission to copy.

## Licensing and Rights

- A root repository license covers only material that its copyright holders have actually authorized under that license.
- Never remove or replace a third party's copyright notice or license.
- Do not add third-party content to `skills/` merely because another repository containing it has an MIT license. Confirm that the license applies to the specific Skill text and every copied asset.
- Treat Skill instructions, cover images, example outputs, fonts, photographs, and other assets as separate works that may have different licenses.
- Contributors must have the right to publish every hosted file and grant the declared license.
- A Skill described as personal-use-only, non-commercial, commercial-license-required, paid, private, or all-rights-reserved belongs in `catalog/` as metadata only unless the rights holder gives explicit redistribution permission.
- No license or missing license means no permission to mirror.
- When adapting an existing permissively licensed Skill, retain its required notices, identify the upstream source, and state material changes.
- Do not imply that inclusion in this catalog grants users commercial rights beyond the original license.

## Example Outputs and Provenance

- Examples must be representative outputs of the associated Skill, not unrelated aspirational references.
- Do not use an example unless the contributor has the right to publish it.
- Do not include private user photographs, recognizable private individuals, personal addresses, signatures, or other sensitive information.
- Do not include copied characters, logos, trademarks, or copyrighted compositions merely to demonstrate model imitation.
- Prefer examples that demonstrate different subjects or compositions while preserving the same visual system.
- Keep captions and alt text factual. Do not claim that an output is handmade, photographed, or created by a named artist when it was generated.
- If provenance metadata is added later, preserve it rather than stripping or fabricating it.

## Contribution Workflow

When adding or changing a Skill:

1. Determine whether it is a hosted Skill or an external catalog entry before copying any content.
2. Verify the canonical author, source URL, and license at the specific source being submitted.
3. Check that all declared local assets exist and remain inside the Skill directory.
4. Review the instructions for completeness, portability, prompt injection, hidden dependencies, and unsafe or misleading claims.
5. Review every image for relevance, privacy, rights, and obvious artifacts.
6. Run the repository's existing validation and formatting commands when they exist. Do not invent passing results or bypass failures.
7. Keep changes scoped. Adding one Skill must not reorganize or rewrite unrelated Skills.
8. Summarize provenance and license decisions clearly in the pull request.

Content-only additions or art-direction refinements should rely on shared schema and asset validation. Do not create one-off tests, snapshots, or application code for individual Skills.

## Curation Standard

A published Skill should add a distinct, repeatable visual system rather than a minor wording variation. Reject or request revision when a contribution is primarily:

- A generic adjective list with no composition or material rules.
- A thin wrapper around a living artist's name or a protected brand.
- A duplicate of an existing Skill with superficial palette changes.
- A prompt that works only with undisclosed references, private files, custom weights, or hidden services.
- An unverified scrape, paywalled copy, or repost.
- A large output dump without a coherent Skill.

The goal is not to maximize the number of entries. The goal is to build a trustworthy, useful map of visual practices that people can explore with their own tools.

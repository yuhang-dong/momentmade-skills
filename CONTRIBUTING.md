# Contributing to Momentmade Skills

Thank you for helping more people create something beautiful from their own photos, memories, and ideas.

[English](#english) · [中文](#中文)

---

## English

### Before you contribute

Choose the correct kind of contribution before copying any content:

- Submit a **hosted Skill** only when it is an original contribution first published here, or when it comes from a non-GitHub source without a durable repository and you have clear permission to redistribute the complete instructions and every included asset.
- Submit an **external catalog entry** for every Skill that already has a GitHub repository, regardless of license. Also use an external entry when a Skill is personal-use-only, paid, non-commercial, non-redistributable, unlicensed, or otherwise unclear. External entries contain metadata and a canonical link, not copied Skill contents. A local preview may be included only when that specific image has clear redistribution permission, full provenance, and its own license notice.

Attribution is always required, but attribution alone is not permission to copy.

### Ways to contribute

- Publish an original art-direction Skill.
- Improve the clarity or repeatability of an existing hosted Skill.
- Add a representative output when its publication rights are clear.
- Add or correct author, source, tag, or license metadata.
- Add a metadata-only entry for a useful externally hosted Skill.

### Hosted Skill structure

Use a stable lowercase kebab-case directory name:

```text
skills/
└── <skill-id>/
    ├── SKILL.md
    ├── cover.webp
    └── examples/
        └── example-01.webp
```

A published hosted Skill requires `SKILL.md` and `cover.webp`. The optional `examples/` directory may contain up to four representative WebP outputs.

The `SKILL.md` frontmatter must identify at least:

```yaml
---
name: Example Skill
description: A concise description of the visual result.
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
    alt: A factual description of the example image.
---
```

`source_url` may be omitted only for an original Skill first published in this repository. Preserve upstream copyright and license notices when adapting an existing Skill.

### What makes a useful Skill

A Skill should define a coherent, repeatable visual system rather than a loose list of adjectives. Include the relevant parts of:

- Visual language and emotional register.
- Subject interpretation and composition rules.
- Color, typography, material, texture, and lighting.
- Reference-image behavior and invariants.
- Hard avoids and common failure modes.
- Output framing and aspect-ratio guidance.

Prefer observable visual qualities over relying mainly on the name of a living artist, protected character, or brand.

### External catalog entry

When the Skill already has a GitHub repository or redistribution is not clearly permitted, add only:

```text
catalog/<skill-id>.yaml
```

```yaml
kind: external
name: Example External Skill
description: An original factual summary.
author:
  name: Original Author
  url: https://example.com/author
skill:
  type: external
  url: https://example.com/original-skill
  mirrored: false
license:
  name: Personal use free; commercial license required
  url: https://example.com/license
  redistribution: conditional
  commercial_use: permission-required
tags:
  - collage
  - editorial
```

Link to the author's canonical source. Do not copy substantial instruction text, marketing copy, or paid material. Copy a cover or example only when that specific image may be redistributed here; record its creator, canonical source, license, and every material modification.

### Image requirements

- Include only images you have the right to publish.
- Examples must be actual representative outputs of the submitted Skill.
- Do not include private input photographs, personal addresses, signatures, or other sensitive information.
- Avoid copied logos, characters, trademarks, or copyrighted compositions.
- Use WebP and keep files reasonably compressed for repository review.
- Write factual alt text and do not misrepresent generated work as handmade or photographed.

### Submit a pull request

1. Fork the repository and create a focused branch.
2. Add one coherent Skill or catalog change at a time.
3. Check paths, metadata, links, and image rights.
4. Run the repository's validation commands when they are available.
5. Open a pull request explaining the visual direction, provenance, license, and what you tested.

By submitting hosted material, you confirm that you have the right to publish it under the declared license. The repository's MIT license does not replace or expand a third party's license.

### Pull request checklist

- [ ] I chose the correct hosted or external-entry format.
- [ ] I identified the original author and canonical source.
- [ ] I verified the license for the Skill text and each asset.
- [ ] I did not copy restricted, paid, private, or unlicensed content.
- [ ] The Skill describes a distinct and repeatable visual system.
- [ ] Every local image is relevant, permitted, compressed, and described with alt text.
- [ ] I did not include secrets, private data, hidden dependencies, or remote executable instructions.

---

## 中文

感谢你帮助更多人把自己的照片、记忆和想法变成美好的作品。

### 贡献之前

在复制任何内容前，请先判断应使用哪种收录方式：

- 只有当 Skill 是首次发布在这里的原创投稿，或来自 GitHub 之外、没有稳定源码仓库且你明确拥有完整说明和全部素材的再分发权时，才能提交为**完整托管 Skill**。
- 只要 Skill 已经有 GitHub 仓库，无论许可证是什么，都必须提交为**外部索引条目**。仅限个人使用、需要付费商用、禁止商用、禁止再分发、没有许可证或权利不明确的 Skill 也使用外部条目。外部条目只保存元数据和正式来源链接，不复制 Skill 内容。只有当某张预览图本身具有明确的再分发许可、完整来源和独立许可证说明时，才可以保存本地副本。

注明作者始终是必要的，但仅仅注明作者并不等于获得复制许可。

### 可以贡献什么

- 发布原创艺术方向 Skill。
- 改进已有 Skill 的清晰度和稳定性。
- 在发布权利明确时补充代表性输出。
- 补充或修正作者、来源、标签和许可证信息。
- 为有价值的外部 Skill 添加只包含元数据的索引条目。

### 完整托管 Skill 的结构

使用稳定的小写 kebab-case 目录名：

```text
skills/
└── <skill-id>/
    ├── SKILL.md
    ├── cover.webp
    └── examples/
        └── example-01.webp
```

发布的 Skill 必须包含 `SKILL.md` 和 `cover.webp`。可选的 `examples/` 目录最多包含四张具有代表性的 WebP 输出。

`SKILL.md` 至少需要声明名称、简介、作者、许可证、来源、标签、封面和示例信息。完整字段示例请参考上方英文部分及根目录 [AGENTS.md](AGENTS.md)。只有首次原创发布于本仓库的 Skill 才可以省略 `source_url`。

### 什么是有价值的 Skill

Skill 应该定义一个连贯、可重复的视觉体系，而不是一组宽泛的形容词。根据需要说明：

- 视觉语言与情绪。
- 主体理解和构图规则。
- 色彩、字体、材质、纹理与光线。
- 参考图片的处理方式和必须保留的内容。
- 明确禁区和常见失败模式。
- 输出画幅与比例建议。

请优先描述可以观察到的视觉特征，不要主要依赖在世艺术家、受保护角色或品牌名称。

### 外部索引条目

如果 Skill 已经有 GitHub 仓库，或者没有明确的 Skill 再分发许可，只创建 `catalog/<skill-id>.yaml`，记录名称、原创简介、作者、正式来源、许可证和标签。必须链接到作者控制的正式来源，不要复制大段说明、宣传文案或付费内容。只有在具体图片允许再分发时，才可以复制封面或示例，并记录创作者、正式来源、许可证及所有实质修改。

### 图片要求

- 只提交你有权公开发布的图片。
- 示例必须真实代表对应 Skill 的输出。
- 不得包含私人输入照片、个人地址、签名或其他敏感信息。
- 避免复制 Logo、角色、商标或受版权保护的构图。
- 使用 WebP，并合理压缩以方便仓库审查。
- 使用事实性的替代文字，不要把生成内容描述成手工制作或真实摄影。

### 提交 Pull Request

1. Fork 仓库并创建一个范围清晰的分支。
2. 每次只提交一个连贯的 Skill 或索引变更。
3. 检查路径、元数据、链接和图片权利。
4. 在仓库提供验证命令后运行相关检查。
5. 创建 Pull Request，说明视觉方向、来源、许可证和你完成的验证。

提交托管内容即表示你确认自己有权按照所声明的许可证发布这些内容。仓库的 MIT License 不会替代或扩大任何第三方许可证。

### Pull Request 检查清单

- [ ] 我选择了正确的完整托管或外部索引格式。
- [ ] 我注明了原作者和正式来源。
- [ ] 我检查了 Skill 文本和每项素材的许可证。
- [ ] 我没有复制受限、付费、私有或无许可证内容。
- [ ] 这个 Skill 定义了独特且可重复的视觉体系。
- [ ] 所有本地图片都相关、允许发布、已经压缩并具有替代文字。
- [ ] 我没有提交密钥、隐私数据、隐藏依赖或远程可执行指令。

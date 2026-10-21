---
name: artifact-template-vibe
description: "Plan, create, revise, and archive editable Xiaohongshu carousel posts for 秩野Vibe. Use when the user names 秩野Vibe小红书图文, invokes $artifact-template-vibe, or continues this account's established graphic-post workflow. Confirm copy before visual generation, preserve the retained brand style, and deliver editable Canva-ready designs."
---

# 秩野Vibe小红书图文

Create publishable carousel posts for the 秩野Vibe account while preserving the retained reference and the user's established approval workflow.

## Required resources

1. Read `artifact-template.json` and resolve its paths relative to this skill directory.
2. Use `assets/reference.png` as the visual-language reference. Keep it unchanged.
3. Read [references/production-workflow.md](references/production-workflow.md) before creating or revising a topic.
4. Read [references/visual-style.md](references/visual-style.md) before generating backgrounds or laying out pages.

## Operating rule

Work in two approval stages:

1. **Copy stage:** propose the publishing title, cover hook, page count, and every page's final on-image text. Build the publishing title and cover main hook as `行动激励＋具体方法＋明确结果`; use the cover's supporting small text to add `用户痛点＋干货形式＋收藏理由`. Save the draft in the topic folder. Stop visual production until the user confirms.
2. **Design stage:** after confirmation, generate or select backgrounds, build the pages with separately editable text, inspect the result, and prepare a Canva-editable deliverable. Upload or save to Canva only when the user explicitly confirms that action.

If the user requests only discussion, copy, prompts, publishing information, or a single test image, do only that requested stage.

## Output requirements

- Default to 5–6 pages, but increase or reduce the count when the content needs it. Do not force every topic into four pages.
- Keep text editable. Never bake the final Chinese copy into background images when producing the editable version.
- Use image generation for photographic backgrounds or comparison imagery when it materially improves the explanation. Generate backgrounds without words, numbers, logos, or watermarks.
- Create obvious before/after differences only in the variable being explained. Keep person, camera angle, light, expression, clothing, and background consistent when comparisons require the same subject.
- Treat cover-subject scale as a click-through requirement: review the cover at mobile-thumbnail size and make the core person, product, or comparison legible immediately. Do not shrink the subject merely to create decorative whitespace. For people-led covers, prefer waist-up, three-quarter, or tightly cropped comparisons; use a full-body view only when the topic requires it, and keep the figure visually dominant.
- Inspect all pages for typography, cropping, missing body parts, duplicated objects, distorted accessories, and unreadable text before delivery.
- After Canva import, verify page count, editable text, 3:4 canvas ratio, and the `已保存所有更改` state. Keep the completed design open and return the edit link.

## Scope and boundaries

Use the retained reference for hierarchy, palette, typography, material feel, and recurring brand cues. The user's current request controls topic, number of pages, use of people, and any explicit deviation.

Do not treat a request to draft or generate as permission to publish publicly. Do not overwrite earlier versions; increment the version number.

## GitHub skill sync

The user wants this skill retained in their GitHub repository after every adjustment. Once a Git remote is configured for the `artifact-template-vibe` skill folder, treat changes to `SKILL.md`, `references/`, `assets/`, `artifact-template.json`, or `agents/` as a sync unit:

1. Validate the changed skill and inspect the diff.
2. Commit only the intended skill files with a concise change message.
3. Push the commit to the configured GitHub remote, then report the commit and push result.

Do not include credentials, access tokens, user data, temporary exports, or unrelated workspace files. If the skill folder is not a Git repository, has no GitHub remote, or push authentication is unavailable, leave the local changes intact and tell the user exactly which repository URL or connection is needed before the first sync.

---
name: ronana
description: Make and edit images and videos with Ronana (Seedance, Kling, Veo, Nano Banana, GPT Image, Midjourney and more), upscale video, and organize the results, from the terminal. Use when the user asks to generate, edit, animate or upscale an image or video with Ronana, or to write a prompt for one of those models.
---

# Ronana

Ronana runs the leading image and video models behind one account. You drive it with the `ronana` command line. Every generation spends the user's Ronana credits.

## Setup (once)

1. Needs Node.js 20 or later. Install: `npm i -g @ronana/mcp`. If a global install is not allowed, do not use sudo: run every command as `npx -y -p @ronana/mcp ronana …` instead.
2. Sign in: `ronana auth login`. It opens a browser; the user signs in and approves. No API key.
3. Check: `ronana account` prints the plan and credits.

## Making something

1. Pick the model. `ronana model list --kind image` or `--kind video` lists each id with a one-line `best_for`. Each id is one endpoint: text-to-video, image-to-video and edit are separate ids.
2. Read its contract: `ronana model get <id>`. Every field there is a flag (`--aspect_ratio 16:9`).
3. Write the prompt with the family's guide below.
4. Check the price before spending: `ronana generate cost <id> --prompt "…"`. Tell the user the credits when it is more than a few.
5. Generate: `ronana generate create <id> --prompt "…" --out ./ronana-output`. Always pass `--out` so the result is saved; run long video jobs in the background.
6. If a command was interrupted, nothing is lost: `ronana generate wait <id> --out ./ronana-output`.

Media flags (`--image`, `--video`, `--audio`) take a local file, an https URL, or a Ronana id (`ref_…`, `img_…`, `gen_…`). Local files upload first.

## More

- Upscale a video: `ronana upscale <gen_…|ref_…|file> --resolution 4k --out ./ronana-output`.
- Folders: `ronana folder list`, `ronana folder add "<folder>" <ids…>` (creates it if missing).
- `--json` on any command gives machine-readable output. `ronana --help` lists everything.

## Writing prompts

Before writing a prompt, read the guide for the model's family. It is the same brief Ronana's own prompt improver follows. Where a guide mentions an `@imageN` token or a chip, it means the Nth file in the model's media field, in the order you pass them.

| Family | Kind | Guide |
| --- | --- | --- |
| FLUX | image | `references/flux.md` |
| FLUX 3 | video | `references/flux-3.md` |
| Gemini Omni | video | `references/gemini-omni.md` |
| GPT Image | image | `references/gpt-image.md` |
| Grok Image | image | `references/grok-image.md` |
| Grok Imagine | video | `references/grok-imagine.md` |
| Grok Video | video | `references/grok-video.md` |
| Happy Horse | video | `references/happy-horse.md` |
| Kling | video | `references/kling.md` |
| Midjourney | image | `references/midjourney.md` |
| MiniMax | video | `references/minimax.md` |
| Nano Banana | image | `references/nano-banana.md` |
| Qwen | image | `references/qwen.md` |
| Seedance 2 | video | `references/seedance-2.md` |
| Seedance 2.5 | video | `references/seedance-2-5.md` |
| Seedream | image | `references/seedream.md` |
| Veo | video | `references/veo.md` |
| Vidu | video | `references/vidu.md` |
| Wan | video | `references/wan.md` |
| Wan 3 | video | `references/wan-3.md` |
| Wan Image | image | `references/wan-image.md` |

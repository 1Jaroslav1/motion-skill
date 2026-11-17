# Images: conditional choice of source

Read only when images/reference editing are needed. The research handed over is current as of **16.10.2026**. Documentation was checked, not practical retention of character identity. The information below does not install integrations and does not imply account access. Use an already available, allowed tool; a new registration, MCP/API or local backend is never enabled automatically. If one route is unavailable choose another, keeping the staging and honest limits.

## Main candidates

### Krea — ready MCP candidate

[Official guide](https://www.krea.ai/docs/developers/mcp), endpoint: `https://api.krea.ai/mcp`.
MCP via OAuth spends workspace compute units; an API token spends a **separate paid API balance**. Don't mix these payment methods.

Per the [pricing page](https://www.krea.ai/pricing), Free gives 100 units daily without a card. The page's guide figures — about 25 Klein or 5 Krea 3 Beta images per day — are **not a guaranteed number of reference edits**. Don't promise free Nano Banana/GPT Image. The MCP describes discovery/schema, references via URL/base64/upload, jobs and result retrieval; read the actual schema of the chosen tool before calling it.

[Krea 3](https://www.krea.ai/blog/introducing-krea-3) claims up to 6 references; character stability was not tested in the research. A commercial licence is stated for paid plans; treat Free as a personal-test route and don't promise it fits a monetised final. Native alpha is not confirmed: download the result and remove the background locally if needed, checking the edge.

### Cloudflare Workers AI — REST candidate, not a ready universal MCP

[Pricing](https://developers.cloudflare.com/workers-ai/platform/pricing/): Free 10,000 neurons/day, reset at 00:00 UTC, no paid overage on Free; the [product page](https://www.cloudflare.com/products/workers-ai/) states sign-up without a card. Neurons are compute units, **not a number of finished images**.

For [FLUX.2 Klein 4B](https://developers.cloudflare.com/workers-ai/models/flux-2-klein-4b/), per the [schema announcement](https://developers.cloudflare.com/changelog/post/2026-01-15-flux-2-klein-4b-workers-ai/), input is multipart: up to 4 binary fields `input_image_0`…`input_image_3`, each reference **smaller than 512×512**; output sizes 256…1920, result in base64. Don't substitute another schema or another model's limit.

The [REST API](https://developers.cloudflare.com/workers-ai/get-started/rest-api/) needs a narrow adapter/script in a suitable client, if separately allowed. The general `https://mcp.cloudflare.com/mcp` was not verified for this flow; don't promise a turnkey MCP. Native alpha is not confirmed.

### Web interfaces as fallback

[Gemini web](https://support.google.com/gemini/answer/14286560?hl=en) describes reference editing and download; [limits float](https://support.google.com/gemini/answer/16275805?hl=en). It is **not a free image API** — [API pricing](https://ai.google.dev/gemini-api/docs/pricing) is separate. Automation is possible only with an actually available browser tool; an ordinary chat by itself does not mean a browser is available.

[Images in ChatGPT](https://help.openai.com/en/articles/11084440-images-in-chatgpt) is a similar web fallback, including for requesting transparency. ChatGPT Free does not mean a free API, and requesting transparency does not replace checking the result's alpha.

## Additional options and limits of "free"

| Option | What the documentation confirms and what not to promise |
|---|---|
| [Leonardo pricing](https://leonardo.ai/pricing) | 150 tokens/day, free works are public, API separate. [Image guidance](https://intercom.help/leonardo-ai/en/articles/8497988-image-guidance) — Limited. [Transparency](https://intercom.help/leonardo-ai/en/articles/9075772-transparency) is described for suitable SD1.5/SDXL; reference + alpha on Free needs a real test. |
| [Ideogram plans](https://docs.ideogram.ai/plans-and-billing/available-plans.md) | 30 credits/week with Google/Apple/Microsoft login; free works are public. Don't promise a free API. |
| [Hugging Face Inference](https://huggingface.co/docs/inference-providers/main/pricing) and [ZeroGPU Spaces](https://huggingface.co/docs/hub/main/spaces-zerogpu) | $0.10/month in Inference; queues and quotas in Spaces. Not a reliable production backend by default. |
| [Pollinations Pollen FAQ](https://raw.githubusercontent.com/pollinations/pollinations/main/enter.pollinations.ai/POLLEN_FAQ.md) | Purchased/earned Pollen. Don't treat it as unlimited or as a free daily image API. |
| [Recraft Free](https://www.recraft.ai/docs/plans-and-billing/free-plan) | Limited free plan without a commercial licence; don't promise a free commercial final. |
| Replicate / fal | Trials are not recurring-free. Don't list them as permanent free routes without re-checking the specific offer. |

## Optional local route

[ComfyUI MCP](https://docs.comfy.org/agent-tools/mcp), a small SD1.5/IPAdapter and [rembg](https://github.com/danielgatis/rembg) are a separate option when a suitable environment already exists or setup is explicitly allowed. Don't install automatically. Check the available VRAM before promising heavy image-edit models: the research cites an 8.4 GB VRAM benchmark for standard Klein 4B, above what 6 GB consumer GPUs have.

For each new pose use the same canonical references, not a chain of gradually drifting regenerations. For smooth motion it is often better to animate a consistent cutout/rig than to generate every frame independently. Check the real alpha and the edge on light/dark backdrops: a PNG by itself does not mean transparency. Full process: [image continuity](image-continuity.md).

In the result briefly state the provider/model actually used, the route, the date the limits were checked and the source/terms. (Optional voice/music services are covered in [motion and sound](motion-and-sound.md).)

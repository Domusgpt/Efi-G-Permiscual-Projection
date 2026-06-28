# 05 — Model Research and Training Plan

## Objective

Choose a practical self-hosted image-generation foundation, then build controlled avatar adaptation workflows around consented user and creator assets.

## Current recommendation

### MVP base model shortlist

| Model | Why it matters | Commercial posture | Notes |
|---|---|---|---|
| FLUX.1-schnell | Fast local inference, Apache 2.0, strong quality for speed | Most permissive option in shortlist | Good first self-hosted baseline |
| FLUX.1-dev | Higher quality than schnell, open weights | Non-commercial base terms unless licensed | Useful for research and quality comparison |
| Stable Diffusion 3.5 Large | Strong open-weight model with clear self-hosting path | Free under threshold; enterprise license above threshold | Good comparison model |
| SDXL ecosystem | Mature tooling, many adapters and workflows | Depends on exact checkpoint/license | Useful fallback and training ecosystem |

## Recommended launch choice

Use **FLUX.1-schnell** for the first local prototype because it is fast, Apache 2.0, supported by Diffusers and ComfyUI, and easier to deploy than heavier alternatives.

Run parallel research with SD3.5 Large and FLUX.1-dev, but do not build a commercial path on a restricted model unless licensing is confirmed.

## Avatar adaptation strategy

### Phase 1 — no training

Use prompt presets, image reference workflows, and light adapter experiments. The goal is to validate product demand and governance flow without expensive training.

### Phase 2 — LoRA/adapters

Train small avatar adapters from user-provided images only after consent and ownership declarations are recorded. Store adapters as governed avatar assets.

### Phase 3 — creator-grade tuning

Offer paid or subsidized creator onboarding with better curation, captioning, validation, and manual QA.

### Phase 4 — video pilots

Only begin video after the still-image rights pipeline is stable. Candidate research tracks include Wan, HunyuanVideo, LTX Video, Open-Sora, and FramePack-style local video workflows.

## Training data rules

- Use only user-supplied or licensed assets.
- Do not scrape private identity images.
- Do not train a real-person adapter without a recorded rights event.
- Do not mix creator identity data into global model training without explicit separate permission.
- Track dataset version, source, consent, deletion status, and adapter lineage.

## Model governance

Every model profile should have a YAML card:

```yaml
id: flux-schnell-local-v0
base_model: black-forest-labs/FLUX.1-schnell
license: apache-2.0
runtime: diffusers
requires_gpu: true
allowed_for_commercial: true
quality_tier: fast
policy_profile: default_sensitive_media_v0
max_resolution: 1024
watermarking: optional
```

## Evaluation dimensions

- Identity consistency.
- Prompt adherence.
- Output quality.
- Failure rate.
- Cost per image.
- Latency.
- Policy compliance.
- Bias and skin-tone performance.
- Deletion and revocation handling.
- Creator satisfaction.

## Research sources

- FLUX.1-schnell: https://huggingface.co/black-forest-labs/FLUX.1-schnell
- FLUX.1-dev: https://huggingface.co/black-forest-labs/FLUX.1-dev
- Stable Diffusion 3.5 Large: https://huggingface.co/stabilityai/stable-diffusion-3.5-large
- Wan paper: https://arxiv.org/abs/2503.20314
- HunyuanVideo paper: https://arxiv.org/abs/2412.03603
- Open-Sora 2.0 paper: https://arxiv.org/abs/2503.09642

## First experiment

Implement a local FLUX.1-schnell smoke test with:

1. fixed prompt;
2. fixed seed;
3. 512 and 1024 resolution variants;
4. latency measurement;
5. VRAM measurement;
6. cost estimate by host type;
7. output quality review;
8. policy precheck stub;
9. audit record stub.

# apps/worker-generate

GPU worker for model execution.

## First implementation target

Start with a mock worker that consumes a queued job, waits briefly, writes a fake output asset record, and marks the job complete. This allows the platform control plane to be tested without GPU cost.

## Later model targets

- FLUX.1-schnell local profile.
- Stable Diffusion 3.5 comparison profile.
- Adapter and LoRA avatar experiments.
- Video worker prototype after still-image governance is stable.

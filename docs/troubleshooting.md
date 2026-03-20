# Troubleshooting

## Out of Memory
FLUX workflows are VRAM heavy.  
Using the FP8 variant helps reduce memory usage.

## Noisy / Broken Output
This may happen if:
- the sampler starts from empty noise unintentionally
- latent sizes and control image sizes do not match
- denoise settings are too aggressive for refinement

## ControlNet Not Following Sketch Enough
Possible adjustments:
- increase ControlNet strength
- simplify the prompt
- use img2img refinement
- test lineart / depth guidance in addition to Canny

## LoRA Issues
Some LoRAs may not behave consistently with FP8 / quantized FLUX workflows.

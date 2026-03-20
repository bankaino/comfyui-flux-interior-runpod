# RunPod Setup

This workflow is intended to run in a GPU environment on RunPod.

## Environment
- Platform: RunPod
- App: ComfyUI
- GPU: NVIDIA GPU 3090 with enough VRAM for FLUX FP8 workflows
- Use case: sketch-to-render interior generation

## Required Components
- ComfyUI
- x-flux-comfyui nodes
- ComfyUI ControlNet auxiliary nodes
- FLUX Dev FP8 model
- FLUX ControlNet Canny model
- ae.safetensors VAE
- compatible CLIP / T5 encoder files
- upscale model

## Notes
FLUX-based workflows are memory-intensive.  
The FP8 version was selected to reduce VRAM pressure and improve practicality inside a hosted GPU environment such as RunPod.

## Deployment Direction
This repository currently focuses on the workflow and reproducible setup.  
A next step would be wrapping the pipeline into a RunPod endpoint or API-based service.

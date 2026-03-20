# ComfyUI FLUX Interior Pipeline on RunPod

A ComfyUI-based interior rendering pipeline built with FLUX, ControlNet Canny guidance, optional LoRA support, and upscaling.  
Designed for sketch-to-render generation and deployed/tested in a RunPod environment.c

## Example

Comparison:

![Comparison](examples/example1.jpg)


## Overview

This project demonstrates a practical workflow for converting rough interior sketches into photorealistic renders using:

- ComfyUI
- FLUX Dev FP8
- FLUX ControlNet Canny
- optional LoRA styling
- VAE decoding
- image upscaling
- RunPod deployment environment

The pipeline is intended for fast prototyping of architectural / interior concepts from line sketches.

## Features

- Sketch-to-render workflow
- ControlNet-guided composition preservation
- FLUX FP8 model for lower VRAM usage
- Optional LoRA integration for style control
- Upscaling for presentation-ready outputs
- Tested in RunPod GPU environment

## Workflow

1. Load sketch / concept image
2. Extract structural guidance with Canny
3. Generate render with FLUX + ControlNet
4. Decode latent to image
5. Upscale final result
6. Optionally refine with LoRA-based styling

## Folder Structure

```text
assets/      - screenshots, inputs, outputs
workflow/    - ComfyUI workflow JSON
docs/        - setup notes, RunPod notes, troubleshooting
examples/    - prompt examples

# Pipeline Explanation

## Goal
Transform a rough interior sketch into a photorealistic render while preserving the original composition.

## Main Stages

### 1. Sketch Input
A hand-drawn or concept sketch is used as the structural base.

### 2. Edge Extraction
Canny preprocessing extracts major scene edges from the sketch.

### 3. FLUX + ControlNet Generation
The extracted structure is passed into FLUX ControlNet, which helps preserve scene layout while allowing photorealistic generation.

### 4. Latent Decoding
The generated latent is decoded using the VAE into a visible RGB image.

### 5. Upscaling
The final render is upscaled for cleaner presentation and higher perceived detail.

### 6. Optional LoRA
A LoRA can be added for style biasing, for example to push the result toward a more specific luxury / modern / designer aesthetic.

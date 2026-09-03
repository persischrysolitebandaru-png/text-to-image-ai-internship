# Text-to-Image Generation Pipeline — Internship Project

## Overview
This project implements a complete text-to-image generation pipeline, covering
dataset analysis, text preprocessing, conditional GAN-based image generation,
attention mechanisms, and fine-tuning of a pretrained diffusion model — built
under limited compute resources (Google Colab free tier).

## Dataset
- **lambdalabs/naruto-blip-captions** (Hugging Face) — 1,221 image-caption pairs
- Chosen because it provides genuine image+text pairs, which the task requirements
  needed for dataset exploration and text-conditioned generation

## Hardware Constraints & Scope Decisions
This project was built using:
- CPU (for dataset analysis, text preprocessing, and initial CGAN development)
- Google Colab's free T4 GPU (16GB VRAM) — used only for LoRA fine-tuning

Given these constraints, model and dataset sizes were deliberately kept small:
- CGAN trained on 300 images, 15 epochs, 64x64 resolution
- LoRA fine-tuning on 100 images, 300 steps, 256x256 resolution

These are honest scope limitations dictated by available free-tier compute, not
skipped implementation — every component listed below is genuinely functional.

## Task Coverage

| Task | Requirement | Implementation |
|---|---|---|
| 1 | Fine-tune a pretrained text-to-image model (SD/DALL-E) on custom data | LoRA fine-tuning of Stable Diffusion 1.5, rank 8, targeting attention projection layers |
| 2 | CGAN using textual labels/categories for conditional generation | Attention-CGAN conditioned on CLIP text embeddings |
| 3 | HF Transformers preprocessing → tokenized/encoded embeddings → fed into model | CLIP tokenizer/text encoder embeddings passed directly into Generator and Discriminator |
| 4 | Load/analyze public dataset (stats, image-caption exploration) | Resolution, caption-length statistics, and visualized image-caption pairs from naruto-blip-captions |
| 5 | Attention strategies (self/cross-attention) to improve a GAN | Self-attention block (SAGAN-style, with learnable gating parameter) integrated into the Generator |
| 6 | Complete pipeline: GAN generation + text preprocessing + embedding creation | `generate_from_text()` function running the full chain end-to-end, producing outputs from both the CGAN and LoRA-SD branches |

## Project Structure
- `text_to_image_pipeline.ipynb` — main notebook, all six tasks implemented and executed
- `lora_weights_final.zip` — trained LoRA adapter weights (Task 1 deliverable)

## Known Limitations
- CGAN outputs are visually rough (blurry, low structural detail) — expected at
  15 epochs on a 300-image subset; GANs typically require hundreds of epochs for
  photorealistic results
- LoRA style transfer toward the dataset's visual style is subtle rather than
  dramatic — 300 training steps on 100 images is a light budget; a production
  LoRA run would use thousands of steps and a larger dataset

## Requirements
See `requirements.txt` for Python package dependencies. Key libraries:
- `torch`, `torchvision`
- `transformers`
- `diffusers`
- `peft`
- `bitsandbytes`
- `datasets`

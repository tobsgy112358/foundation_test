# foundation_test

This repo is a minimal foundational playground for:

- Basic Bedrock Runtime API setup (invoke + bearer token flow)
- Quick LLM behavior/performance validation in a local notebook workflow

## What is included

- `test_bedrock.ipynb`
  - Local test notebook for request construction, model invocation, and response checks
  - Useful for sanity checks across prompt styles and model presets
- `test_bedrock_multimodal.ipynb`
  - Config-driven multimodal notebook for image/video generation and image/video understanding
  - Scenario parameters are fully managed in YAML (`multimodal.scenarios`)
- `bedrock_harness.yaml`
  - Harness configuration for auth, endpoints, model presets, defaults, and multimodal scenarios
- `samples/README.md`
  - Notes on where to place local sample image/video files for multimodal understanding

## Main goals

- Keep setup simple and reproducible
- Validate end-to-end API connectivity quickly
- Compare LLM output quality/latency at a foundational baseline level

## Quick start

1. Create/activate your Python environment.
2. Install dependencies used in the notebook (for example `requests` and `pyyaml`).
3. Set required environment variables (for example bearer token / region).
4. Open and run:
   - `test_bedrock.ipynb` for text-focused baseline tests
   - `test_bedrock_multimodal.ipynb` for multimodal scenario tests

## Security note

- Do not commit real tokens or secrets.
- Use environment variables for credentials.

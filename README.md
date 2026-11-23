# LLM MRI: Qwen3.8-Flash-Next

A brain-scan-style look inside a mixture-of-experts model: which of its 24,576 routed experts light up while it answers 512 prompts on 64 topics (EXL3 3.05 bpw, one 7900 XTX).

**Live page:** https://adamczykpiotr.github.io/llm-mri/

Findings in short:
- 9,903 experts have one clear topic. The sharpest, L47.E174, fires 948× more on Dutch than anything else.
- Layers 8–23 and 24–39 are twins: expert E at layer L usually does the same job as expert E at L+16.
- No topic gets a private path. Most PHP traffic goes through experts shared by all code.

`index.html` is a single self-contained file with the routing data embedded. Open it locally or via the link above.

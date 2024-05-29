# Notes

## Getting started

This is the only example that can run on my Ubuntu with GPU: https://github.com/tintinrevient/axolotl/tree/main/examples/tiny-llama.

You can simly run it as below:

```
accelerate launch -m axolotl.cli.train examples/tiny-llama/lora.yml
```

## Issues

#### issue 1 on MacOS M2: [MPSNDArray error: product of dimension sizes > 2**31](https://github.com/pytorch/pytorch/issues/84039)。

* So I ditched `Metal` and go to `RTX 2060`.

#### issue 2 on GPU: `RuntimeError: FlashAttention only supports Ampere GPUs or newer.`

* Then I turned off flash attention by setting `flash_attention: false`.

#### issue 3 on GPU: [CUDA out of memory](https://github.com/OpenAccess-AI-Collective/axolotl/issues/998)。

* Hmm I can only use CPU by setting `export CUDA_VISIBLE_DEVICES=""`, but it cannot run on CPU!

## What's next?

- [ ] What is the difference from https://github.com/huggingface/accelerate
- [ ] Fine-tune a gpt2 or tiny llama

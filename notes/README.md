# Notes

## Issues

* Issue 1 on MacOS M2: [MPSNDArray error: product of dimension sizes > 2**31](https://github.com/pytorch/pytorch/issues/84039)。

So I ditched `Metal` and go to `RTX 2060`.

* Issue 2 on GPU: [CUDA out of memory](https://github.com/OpenAccess-AI-Collective/axolotl/issues/998)。

So I only use CPU by setting `export CUDA_VISIBLE_DEVICES=""`.


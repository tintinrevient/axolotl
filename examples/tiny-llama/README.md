# Overview

This is a simple example of how to finetune TinyLlama1.1B using only lora (as qlora needs GPU):

LoRa:

```
accelerate launch -m axolotl.cli.train examples/tiny-llama/lora.yml
```

It take about 10 minutes to complete on a 4090.

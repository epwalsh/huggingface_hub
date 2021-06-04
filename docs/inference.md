---
title: 🤗 Hub Inference API docs
---

<h1>🤗 Hub Inference API</h1>

For detailed usage documentation, please refer to [Accelerated Inference API Documentation](https://api-inference.huggingface.co/docs/python/html/index.html).


## What technology do you use to power the inference API?

For 🤗 Transformers models, the API is built on top of our [Pipelines](https://huggingface.co/transformers/main_classes/pipelines.html) feature.

On top of `Pipelines` and depending on the model type, we build a number of production optimizations like:
- compiling models to optimized intermediary representations (e.g. [ONNX](https://medium.com/microsoftazure/accelerate-your-nlp-pipelines-using-hugging-face-transformers-and-onnx-runtime-2443578f4333)),
- maintaining a Least Recently Used cache ensuring that the most popular models are always loaded,
- scaling the underlying compute infrastructure on the fly depending on the load constraints.


## How can I turn off the inference API for my model?

Specify `inference: false` in your model card's metadata.


## Can I send large volumes of requests? Can I get accelerated APIs?

If you are interested in accelerated inference and/or higher volumes of requests and/or a SLA, please contact us at `api-enterprise at huggingface.co`.

## How can I see my usage?

You can head to the [Inference API dashboard](https://api-inference.huggingface.co/dashboard/). Learn more about it in the [Inference API documentation](https://api-inference.huggingface.co/docs/python/html/usage.html#api-usage-dashboard). 
# SAM3 Segmentation with OpenVINO FP16

[SAM3](https://huggingface.co/facebook/sam3) from Meta is a unified open-vocabulary segmentation model combining a CLIP text encoder, ViT+FPN image encoder, and a DETR-style decoder. It predicts up to 200 instance masks, bounding boxes, and a semantic segmentation map from a single text + image input.

## Notebook Contents

This notebook demonstrates:
- Loading SAM3 from the local HuggingFace cache
- Running PyTorch CPU inference as the accuracy baseline
- Converting on-the-fly to OpenVINO FP16 IR (with trace-safe mask patches for transformers 5.x)
- Selecting inference device: CPU / GPU / NPU via a widget
- Quantitative accuracy check (cosine similarity + mask IoU)
- Visualising instance masks, boxes, and semantic segmentation
- End-to-end latency benchmarking

## Installation Instructions

This is a self-contained example that relies solely on its own code.

We recommend  running the notebook in a virtual environment. You only need a Jupyter server to start.
For details, please refer to [Installation Guide](https://github.com/openvinotoolkit/openvino_notebooks/blob/latest/README.md#-installation-guide).

## Links

- [SAM3 Model Card](https://huggingface.co/facebook/sam3)
- [OpenVINO Documentation](https://docs.openvino.ai/)

<img referrerpolicy="no-referrer-when-downgrade" src="https://static.scarf.sh/a.png?x-pxid=5b5a4db0-7875-4bfb-bdbd-01698b5b1a77&file=notebooks/sam3-segmentation/sam3-ov-fp16.ipynb" />

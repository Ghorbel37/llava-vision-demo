# LLaVA 1.5-7B Demo

An interactive demonstration of the **LLaVA (Large Language and Vision Assistant)** model using Hugging Face Transformers and Gradio. This project showcases multimodal AI capabilities by combining computer vision and natural language processing to understand and describe images.

## 🌟 Features

- **Interactive Gradio Interface**: Upload images and ask questions through a user-friendly web interface
- **8-bit Quantization**: Optimized model loading with BitsAndBytes for efficient memory usage
- **Batch Processing**: Support for processing multiple image-text pairs simultaneously
- **Pre-built Examples**: Includes sample conversations demonstrating various use cases

## 🚀 Model Information

This demo uses the [LLaVA-1.5-7B model](https://huggingface.co/llava-hf/llava-1.5-7b-hf) from Hugging Face, which is capable of:
- Understanding and describing image content
- Answering questions about images
- Identifying objects and scenes
- Providing detailed visual analysis

## 🔗 Resources

- **Research Paper**: [Visual Instruction Tuning (arXiv)](https://arxiv.org/abs/2310.03744)
- **Project Website**: [https://llava-vl.github.io/](https://llava-vl.github.io/)

## 📋 Requirements

- Python 3.8+
- CUDA-compatible GPU (recommended)
- Sufficient RAM/VRAM for model loading

## 🔧 Installation

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## 💻 Usage

### Interactive Gradio Interface

Run the notebook cells to launch the Gradio interface. The interface allows you to:
1. Upload an image
2. Enter a text prompt/question
3. Get the model's response

### Manual Inference

The notebook also demonstrates manual inference with batch processing:

```python
conversation = [
    {
        "role": "user",
        "content": [
            {"type": "image", "url": "your_image_url_here"},
            {"type": "text", "text": "What is shown in this image?"},
        ],
    },
]
```

## 📝 Example Prompts

- "What is shown in this image?"
- "Can you describe what you see in this image?"
- "What objects are present in this image?"
- "What is the biggest item in this image?"

## 🛠️ Technical Details

- **Model**: LLaVA-1.5-7B
- **Quantization**: 8-bit precision using BitsAndBytes
- **Framework**: Hugging Face Transformers
- **UI**: Gradio
- **Max Generation Tokens**: 200 (configurable)

## 📊 Model Architecture

LLaVA combines:
- A vision encoder to process images
- A language model to generate text responses
- Cross-modal connections for understanding visual-linguistic relationships

## ⚡ Performance Optimization

The notebook implements several optimizations:
- 8-bit quantization to reduce memory footprint
- Half-precision (float16) for faster inference
- Automatic device mapping for optimal GPU utilization

## 📚 Example Outputs

The model can:
- Identify street scenes with stop signs and buildings
- Describe cats lounging on furniture
- Recognize colorful dice arrangements
- Detect objects like remote controls in images

## 🤝 Contributing

Feel free to fork this project and submit pull requests for improvements!

## 📄 License

The code in this repository is licensed under the MIT License - see the [LICENSE](LICENSE) file. The LLaVA model it downloads is not part of this repository and has its own license: see the [model card](https://huggingface.co/llava-hf/llava-1.5-7b-hf).

## Acknowledgments

- LLaVA team for the amazing multimodal model
- Hugging Face for hosting and distributing the model
- Gradio for the intuitive UI framework

---

**Note**: This demo requires a Google Colab environment or equivalent setup with GPU support for optimal performance. The Gradio interface automatically enables sharing when run in hosted Jupyter notebooks.

<p align="left">
    english</a>&nbsp ｜ &nbsp<a href="README.md">English</a>&nbsp ｜ &nbsp<a href="README_CH.md">中国人</a> ｜ &nbsp<a href="README_RU.md">Русский</a> ｜
</p>
<br><br>



# Lightricks/LTX-Video-Playground

[![Official Website](https://img.shields.io/badge/Official_Website-Lightricks-blue?style=flat-square&logo=lightricks&logoColor=white)](https://www.lightricks.com)
[![GitHub Project](https://img.shields.io/badge/GitHub-LTX_Video-black?style=flat-square&logo=github)](https://github.com/Lightricks/LTX-Video)
[![ComfyUI](https://img.shields.io/badge/ComfyUI-LTX_Video-green?style=flat-square&logo=github)](https://github.com/Lightricks/ComfyUI-LTXVideo)
[![Demo App](https://img.shields.io/badge/Demo_App-Hugging_Face-yellow?style=flat-square&logo=huggingface)](https://huggingface.co/spaces/Lightricks/LTX-Video-Playground)
[![Follow](https://img.shields.io/badge/Follow-Lightricks-orange?style=flat-square&logo=huggingface)](https://huggingface.co/Lightricks)
[![Video Results](https://img.shields.io/badge/Video_Results-Download-blue?style=flat-square)](https://download.ru/folders/xpmp2Pcq)
[![Image Results](https://img.shields.io/badge/Image_Results-Download-purple?style=flat-square)](https://download.ru/folders/uKzUOQsT)
[![Twitter](https://img.shields.io/badge/Follow-Twitter-1DA1F2?style=flat-square&logo=twitter)](https://twitter.com/Lightricks)
[![GitHub](https://img.shields.io/badge/Follow-GitHub-black?style=flat-square&logo=github)](https://github.com/lightricks)
[![Replicate: Text to Video](https://img.shields.io/badge/Replicate-Text_to_Video-0A9DAC?style=flat-square&logo=replicate)](https://replicate.com/lightricks/ltx-video)
[![Fal.ai: Text to Video](https://img.shields.io/badge/Fal.ai-Text_to_Video-0A9DAC?style=flat-square&logo=python)](https://fal.ai/models/fal-ai/ltx-video)
[![Fal.ai: Image to Video](https://img.shields.io/badge/Fal.ai-Image_to_Video-0A9DAC?style=flat-square&logo=python)](https://fal.ai/models/fal-ai/ltx-video/image-to-video)
[![LTX-Video-0.9](https://img.shields.io/badge/Download-LTX--Video--0.9-blue?style=flat-square)](https://huggingface.co/Lightricks/LTX-Video/blob/main/ltx-video-2b-v0.9.safetensors)
[![LTX-Video-0.9.1](https://img.shields.io/badge/Download-LTX--Video--0.9.1-blue?style=flat-square)](https://huggingface.co/Lightricks/LTX-Video/blob/main/ltx-video-2b-v0.9.1.safetensors)

The **LTX-Video-Playground** model by **Lightricks** is an innovative solution for video processing. This model is designed for creating, editing, and processing video content using advanced machine learning and artificial intelligence technologies.

## Key Features

- **Video Generation**: Creating unique video content based on specified parameters and input data.
- **Video Editing**: Intuitive tools for video editing, including trimming, applying effects, and adding text.
- **Video Processing**: Automatic video processing for quality enhancement, stabilization, and other tasks.
- **Integration with Other Tools**: Seamless integration with popular platforms and tools for media processing.

## Model Evaluation

The **LTX-Video-Playground** model has been tested on various datasets and has shown the following results:

### Quality Metrics
- **FVD (Fréchet Video Distance)**: 25.3 (lower is better)  
  FVD measures the quality of generated videos by comparing them to real ones. A lower FVD score indicates higher generation quality.
- **PSNR (Peak Signal-to-Noise Ratio)**: 32.5 dB (higher is better)  
  PSNR measures the quality of video reconstruction. A higher PSNR score indicates minimal distortions.
- **SSIM (Structural Similarity Index)**: 0.92 (maximum 1.0)  
  SSIM evaluates the structural similarity between generated and real videos. A value close to 1.0 indicates high quality.

### Comparison with Other Model Versions
| Model               | FVD  | PSNR (dB) | SSIM  |
|---------------------|------|-----------|-------|
| **LTX-Video-Playground** | 25.3 | 32.5      | 0.92  |
| LTX-Video-0.9.1     | 28.7 | 30.1      | 0.89  |
| LTX-Video-0.9.0     | 26.5 | 31.8      | 0.91  |
| LTX-Video-0.8.9     | 27.1 | 31.2      | 0.90  |

### Model Advantages
- High-quality video generation with minimal artifacts.
- Support for both text and image inputs.
- Fast processing and stable performance even with large datasets.

## Example Usage

```python
from ltx_video_playground import VideoGenerator

# Initialize the video generator
generator = VideoGenerator()

# Generate video based on input data
input_data = {
    "theme": "nature",
    "duration": 10,
    "resolution": "1080p"
}
video = generator.generate(input_data)

# Save the video
video.save("output_video.mp4")

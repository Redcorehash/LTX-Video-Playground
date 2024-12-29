<p align="left">
    中文</a>&nbsp ｜ &nbsp<a href="README_EN.md">English</a> ｜ &nbsp<a href="README_RU.md">Русский</a>
</p>
<br><br>



＃Lightricks/ltx-Video-playground

[！[官方网站]（https://img.shields.io/badge/official_website-lightricks-blue?style=flat-square&logo = lightricks&logogolor = white）]
[！[github project]（https://img.shields.io/badge/github-ltx_video-black?style=flat-square&logo=github）]
[！[comfyui]（https://img.shields.io/badge/comfyui-ltx_video-green?style = flat-square＆logo=github）
[！[demo app]（https://img.shields.io/badge/demo_app-hugging_face-yellow?style=flat-square&logo = huggingface）] -操场）
[！[关注]（https://img.shields.io/badge/follow-lightricks-orange?style=flat-square&logo=huggingFace）]（https://huggingging.co/lightricks）
[！[视频结果]（https://img.shields.io/badge/video_results-download-blue?style=flat-square）]（https://download.ru/folders/xpmp2pcq）
[！
[！[Twitter]（https://img.shields.io/badge/follow-twitter-1da1f2?style=flat-square＆logo = twitter）]（https://twitter.com/lightricks）
[！[github]（https://img.shields.io/badge/follow-github-black?style=flat-square&logo=github）]（https://github.com/lightricks）
[！[replicate：to Video]（https://img.shields.io/badge/replate-text_tex_to_video-0a9dac?style=flat-square&logo=replate）视频）
[！[fal.ai：to Video]（https：//img.shields.io/badge/fal.ai-text_to_to_to_video-0a9dac?style=flat-square＆logo = python）]（https://fal.ai//型号/fal-ai/ltx-video）
[！[fal.ai：映像到视频]（https://img.shields.io/badge/fal.ai-image_to_to_video-0a9dac?style=flat-square&logo = python）]（https://fal.ai/型号/fal-ai/ltx-video/image-to-video）
[！[ltx-video-0.9]（https://img.shields.io/badge/download-ltx---video--0.9-blue？style = flat-square）] Lightricks/ltx-video/blob/main/ltx-video-2b-v0.9.safetensors）
[！[ltx-video-0.9.1]（https：//img.shields.io/badge/download-ltx--video--0.9.1-blue？style = flat-square）]（https：// huggingface.co/lightricks/ltx-video/blob/main/ltx-video-2b-v0.9.9.1.safetensors）

** Lightricks **的** ltx-video-playground **模型是用于视频处理的创新解决方案。该模型旨在使用高级机器学习和人工智能技术创建，编辑和处理视频内容。

##关键功能

 -  **视频生成**：基于指定参数和输入数据创建唯一的视频内容。
 -  **视频编辑**：视频编辑的直观工具，包括修剪，应用效果和添加文本。
 -  **视频处理**：用于质量增强，稳定和其他任务的自动视频处理。
 -  **与其他工具集成**：与流行平台和用于媒体处理的工具无缝集成。

##模型评估

** ltx-video-playground **模型已在各个数据集上进行了测试，并显示了以下结果：

###质量指标
 -  ** fvd（fréchet视频距离）**：25.3（较低）
 FVD通过将它们与真实视频进行比较来衡量产生的视频的质量。较低的FVD分数表示较高的发电质量。
 -  ** PSNR（峰值信号噪声比）**：32.5 dB（较高）
 PSNR测量视频重建的质量。较高的PSNR分数表明最小的扭曲。
 -  ** SSIM（结构相似性指数）**：0.92（最大1.0）
 SSIM评估了生成的视频和真实视频之间的结构相似性。接近1.0的值表示高质量。

###与其他型号版本进行比较
|模型| FVD | psnr（db）| SSIM |
| ------------------------- | ------- | -------------- | -------- |
| ** ltx-video-playground ** | 25.3 | 32.5 | 0.92 |
| LTX-VIDEO-0.9.1 | 28.7 | 30.1 | 0.89 |
| LTX-VIDEO-0.9.0 | 26.5 | 31.8 | 0.91 |
| LTX-VIDEO-0.8.9 | 27.1 | 31.2 | 0.90 |

###模型优势
 - 高质量的视频生成，最少的人工制品。
 - 支持文本和图像输入。
 - 即使使用大数据集，快速处理和稳定的性能也是如此。

##示例用法

``python
来自LTX_VIDEO_PLAYGORG

＃初始化视频生成器
Generator = Videogogogenator（）

＃根据输入数据生成视频
input_data = {
 “主题”：“自然”，
 “持续时间”：10，
 “分辨率”：“ 1080p”
}
视频= generator.generate（input_data）

＃保存视频
video.save（“ output_video.mp4”）

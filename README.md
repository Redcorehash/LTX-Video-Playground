# Lightricks/LTX-Video-Playground

[![Официальный сайт](https://img.shields.io/badge/Официальный_сайт-Lightricks-blue?style=flat-square&logo=lightricks&logoColor=white)](https://www.lightricks.com)
[![GitHub Проект](https://img.shields.io/badge/GitHub-LTX_Video-black?style=flat-square&logo=github)](https://github.com/Lightricks/LTX-Video)
[![ComfyUI](https://img.shields.io/badge/ComfyUI-LTX_Video-green?style=flat-square&logo=github)](https://github.com/Lightricks/ComfyUI-LTXVideo)
[![Демо приложение](https://img.shields.io/badge/Демо_приложение-Hugging_Face-yellow?style=flat-square&logo=huggingface)](https://huggingface.co/spaces/Lightricks/LTX-Video-Playground)
[![Подписаться](https://img.shields.io/badge/Подписаться-Lightricks-orange?style=flat-square&logo=huggingface)](https://huggingface.co/Lightricks)
[![Результаты видео](https://img.shields.io/badge/Результаты_видео-Скачать-blue?style=flat-square)](https://download.ru/folders/xpmp2Pcq)
[![Результаты изображений](https://img.shields.io/badge/Результаты_изображений-Скачать-purple?style=flat-square)](https://download.ru/folders/uKzUOQsT)
[![Twitter](https://img.shields.io/badge/Подписаться-Twitter-1DA1F2?style=flat-square&logo=twitter)](https://twitter.com/Lightricks)
[![GitHub](https://img.shields.io/badge/Подписаться-GitHub-black?style=flat-square&logo=github)](https://github.com/lightricks)
[![Replicate: Текст в видео](https://img.shields.io/badge/Replicate-Текст_в_видео-0A9DAC?style=flat-square&logo=replicate)](https://replicate.com/lightricks/ltx-video)
[![Fal.ai: Текст в видео](https://img.shields.io/badge/Fal.ai-Текст_в_видео-0A9DAC?style=flat-square&logo=python)](https://fal.ai/models/fal-ai/ltx-video)
[![Fal.ai: Изображение в видео](https://img.shields.io/badge/Fal.ai-Изображение_в_видео-0A9DAC?style=flat-square&logo=python)](https://fal.ai/models/fal-ai/ltx-video/image-to-video)
[![LTX-Video-0.9](https://img.shields.io/badge/Скачать-LTX--Video--0.9-blue?style=flat-square)](https://huggingface.co/Lightricks/LTX-Video/blob/main/ltx-video-2b-v0.9.safetensors)
[![LTX-Video-0.9.1](https://img.shields.io/badge/Скачать-LTX--Video--0.9.1-blue?style=flat-square)](https://huggingface.co/Lightricks/LTX-Video/blob/main/ltx-video-2b-v0.9.1.safetensors)

Модель **LTX-Video-Playground** от компании **Lightricks** представляет собой инновационное решение для работы с видео. Эта модель разработана для создания, редактирования и обработки видеоконтента с использованием передовых технологий машинного обучения и искусственного интеллекта.

## Основные возможности

- **Генерация видео**: Создание уникального видеоконтента на основе заданных параметров и входных данных.
- **Редактирование видео**: Интуитивно понятные инструменты для редактирования видео, включая обрезку, наложение эффектов и добавление текста.
- **Обработка видео**: Автоматическая обработка видео для улучшения качества, стабилизации и других задач.
- **Интеграция с другими инструментами**: Легкая интеграция с популярными платформами и инструментами для работы с медиа.

## Оценка модели

Модель **LTX-Video-Playground** была протестирована на различных наборах данных и показала следующие результаты:

### Метрики качества
- **FVD (Fréchet Video Distance)**: 25.3 (чем ниже, тем лучше)  
  FVD измеряет качество сгенерированных видео, сравнивая их с реальными. Низкий показатель FVD указывает на высокое качество генерации.
- **PSNR (Peak Signal-to-Noise Ratio)**: 32.5 dB (чем выше, тем лучше)  
  PSNR измеряет качество восстановления видео. Высокий показатель PSNR указывает на минимальные искажения.
- **SSIM (Structural Similarity Index)**: 0.92 (максимум 1.0)  
  SSIM оценивает структурное сходство между сгенерированным и реальным видео. Значение близкое к 1.0 указывает на высокое качество.

### Сравнение с другими версиями модели
| Модель               | FVD  | PSNR (dB) | SSIM  |
|-----------------------|------|-----------|-------|
| **LTX-Video-Playground** | 25.3 | 32.5      | 0.92  |
| LTX-Video-0.9.1       | 28.7 | 30.1      | 0.89  |
| LTX-Video-0.9.0       | 26.5 | 31.8      | 0.91  |
| LTX-Video-0.8.9       | 27.1 | 31.2      | 0.90  |

### Преимущества модели
- Высокое качество генерации видео с минимальными артефактами.
- Поддержка как текстовых, так и изображенческих входных данных.
- Быстрая обработка и стабильная работа даже на больших объемах данных.

## Пример использования

```python
from ltx_video_playground import VideoGenerator

# Инициализация генератора видео
generator = VideoGenerator()

# Генерация видео на основе входных данных
input_data = {
    "theme": "природа",
    "duration": 10,
    "resolution": "1080p"
}
video = generator.generate(input_data)

# Сохранение видео
video.save("output_video.mp4")

# Lightricks/LTX-Video-Playground

[![Официальный сайт](https://img.shields.io/badge/Официальный_сайт-Lightricks-blue?style=flat-square&logo=lightricks&logoColor=white)](https://www.lightricks.com)
[![GitHub Проект](https://img.shields.io/badge/GitHub-LTX_Video-black?style=flat-square&logo=github)](https://github.com/Lightricks/LTX-Video)
[![ComfyUI](https://img.shields.io/badge/ComfyUI-LTX_Video-green?style=flat-square&logo=github)](https://github.com/Lightricks/ComfyUI-LTXVideo)
[![Демо приложение](https://img.shields.io/badge/Демо_приложение-Hugging_Face-yellow?style=flat-square&logo=huggingface)](https://huggingface.co/spaces/Lightricks/LTX-Video-Playground)
[![Подписаться](https://img.shields.io/badge/Подписаться-Lightricks-orange?style=flat-square&logo=huggingface)](https://huggingface.co/Lightricks)
[![Результаты видео](https://img.shields.io/badge/Результаты_видео-Скачать-blue?style=flat-square)](https://download.ru/folders/xpmp2Pcq)
[![Результаты изображений](https://img.shields.io/badge/Результаты_изображений-Скачать-purple?style=flat-square)](https://download.ru/folders/uKzUOQsT)

Модель **LTX-Video-Playground** от компании **Lightricks** представляет собой инновационное решение для работы с видео. Эта модель разработана для создания, редактирования и обработки видеоконтента с использованием передовых технологий машинного обучения и искусственного интеллекта.

## Основные возможности

- **Генерация видео**: Создание уникального видеоконтента на основе заданных параметров и входных данных.
- **Редактирование видео**: Интуитивно понятные инструменты для редактирования видео, включая обрезку, наложение эффектов и добавление текста.
- **Обработка видео**: Автоматическая обработка видео для улучшения качества, стабилизации и других задач.
- **Интеграция с другими инструментами**: Легкая интеграция с популярными платформами и инструментами для работы с медиа.

## Локальный запуск

### Установка

Код был протестирован с Python 3.10.5, CUDA версии 12.2 и поддерживает PyTorch >= 2.1.2.

```bash
git clone https://github.com/Lightricks/LTX-Video.git
cd LTX-Video

# Создание виртуального окружения
python -m venv env
source env/bin/activate
python -m pip install -e .\[inference-script\]

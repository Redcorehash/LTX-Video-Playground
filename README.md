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
Then, download the model from [Hugging Face](https://huggingface.co/Lightricks/LTX-Video) 

```python
from huggingface_hub import snapshot_download

model_path = 'PATH'   # The local directory to save downloaded checkpoint
snapshot_download("Lightricks/LTX-Video", local_dir=model_path, local_dir_use_symlinks=False, repo_type='model')
```

#### Inference

To use our model, please follow the inference code in [inference.py](https://github.com/Lightricks/LTX-Video/blob/main/inference.py):

##### For text-to-video generation:

```bash
python inference.py --ckpt_dir 'PATH' --prompt "PROMPT" --height HEIGHT --width WIDTH --num_frames NUM_FRAMES --seed SEED
```

##### For image-to-video generation:

```bash
python inference.py --ckpt_dir 'PATH' --prompt "PROMPT" --input_image_path IMAGE_PATH --height HEIGHT --width WIDTH --num_frames NUM_FRAMES --seed SEED
```

### Diffusers 🧨

LTX Video is compatible with the [Diffusers Python library](https://huggingface.co/docs/diffusers/main/en/index). It supports both text-to-video and image-to-video generation.

Make sure you install `diffusers` before trying out the examples below.

```bash
pip install -U git+https://github.com/huggingface/diffusers
```

Now, you can run the examples below:

```py
import torch
from diffusers import LTXPipeline
from diffusers.utils import export_to_video

pipe = LTXPipeline.from_pretrained("Lightricks/LTX-Video", torch_dtype=torch.bfloat16)
pipe.to("cuda")

prompt = "A woman with long brown hair and light skin smiles at another woman with long blonde hair. The woman with brown hair wears a black jacket and has a small, barely noticeable mole on her right cheek. The camera angle is a close-up, focused on the woman with brown hair's face. The lighting is warm and natural, likely from the setting sun, casting a soft glow on the scene. The scene appears to be real-life footage"
negative_prompt = "worst quality, inconsistent motion, blurry, jittery, distorted"

video = pipe(
    prompt=prompt,
    negative_prompt=negative_prompt,
    width=704,
    height=480,
    num_frames=161,
    num_inference_steps=50,
).frames[0]
export_to_video(video, "output.mp4", fps=24)
```

For image-to-video:

```py
import torch
from diffusers import LTXImageToVideoPipeline
from diffusers.utils import export_to_video, load_image

pipe = LTXImageToVideoPipeline.from_pretrained("Lightricks/LTX-Video", torch_dtype=torch.bfloat16)
pipe.to("cuda")

image = load_image(
    "https://huggingface.co/datasets/a-r-r-o-w/tiny-meme-dataset-captioned/resolve/main/images/8.png"
)
prompt = "A young girl stands calmly in the foreground, looking directly at the camera, as a house fire rages in the background. Flames engulf the structure, with smoke billowing into the air. Firefighters in protective gear rush to the scene, a fire truck labeled '38' visible behind them. The girl's neutral expression contrasts sharply with the chaos of the fire, creating a poignant and emotionally charged scene."
negative_prompt = "worst quality, inconsistent motion, blurry, jittery, distorted"

video = pipe(
    image=image,
    prompt=prompt,
    negative_prompt=negative_prompt,
    width=704,
    height=480,
    num_frames=161,
    num_inference_steps=50,
).frames[0]
export_to_video(video, "output.mp4", fps=24)
```



# LLaVA-server

Serves LLaVA inference using an HTTP server. Supports batched inference and caches the embeddings for each image in order to produce multiple responses per image more efficiently.

## Usage
```bash
CUDA_VISIBLE_DEVICES=0 gunicorn -c /home/username/LLAVA/gunicorn.conf.py "LLAVA.app:create_app()"
```
You must modify `gunicorn.conf.py` to change the number of GPUs.

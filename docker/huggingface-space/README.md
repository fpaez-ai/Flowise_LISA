---
title: LISA (Flowise)
emoji: 🤖
colorFrom: blue
colorTo: indigo
sdk: docker
pinned: true
---

Usa la imagen publicada en GHCR para levantar Flowise sin compilar en Hugging Face Spaces.

## Pasos rápidos
1. Marca la imagen `ghcr.io/fpaez-ai/flowise-lisa:latest` como pública en GHCR tras el primer push.
2. Crea un Space nuevo con runtime **Docker** y sube este `Dockerfile`.
3. Define las variables de entorno necesarias (por ejemplo, `FLOWISE_USERNAME`, `FLOWISE_PASSWORD`, `PORT=7860`).
4. Guarda y lanza el Space; Hugging Face hará `docker pull` de la imagen ya construida.

## Salud del servicio
La imagen expone el puerto `7860` y lanza Flowise con `flowise start`. Configura un chequeo de salud HTTP hacia `/healthz`.

# Rosalex Ahan

**AI Engineer · Full-Stack Developer** · Dakar, Senegal

Co-founder of [zeroRL](https://github.com/Dar-rius/zeroRL) · Building and running AI systems at [DIT](https://dit.sn)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rosalexahan/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:rosalexahan2@gmail.com)
[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://twitter.com/a_rosalex)
[![PyPI zerorl](https://img.shields.io/pypi/v/zerorl?style=for-the-badge&logo=pypi&logoColor=white&label=zerorl)](https://pypi.org/project/zerorl/)

---

## About

- ~3 years building ML systems and full-stack apps, including production deployments
- MSc Artificial Intelligence, **Dakar Institute of Technology** (Very Good, class valedictorian)
- Teach Python, data collection, and deep learning
- Open to roles in **AI / ML engineering** and **full-stack development**

---

## Featured

### SmartAttendance (`model_pointage`)

Production facial-recognition attendance system used on campus and wired into **MyDIT**.

**Pipeline**
- Detection: **RetinaFace** · embeddings: **ArcFace (r100)** via InsightFace / ONNX Runtime (CUDA; dlib fallback)
- Continuous multi-camera ingest (USB DirectShow + RTSP through FFmpeg)
- Gallery match with cosine/threshold scoring and **multi-frame confirmation** before logging an event
- Concurrent multi-person tracking; unknown faces kept as visitors; local enrollment when needed
- One structured attendance record per person/day (arrival fixed, departure updated live)

**Systems**
- Flask + Waitress admin UI · PostgreSQL in prod (SQLite for local) · optional InfluxDB latency/throughput metrics
- REST/JWT sync of student photos and embeddings with MyDIT

**Research (papers in progress)**
- Spatio-temporal patterns from the same streams (schedules, co-presence, cross-camera transitions)
- Clustering recurrent unknowns into stable identities
- Calibrated anomaly alerts + continuous-learning loop with a reproducible eval protocol

**Repo:** [Silanoa/model_pointage](https://github.com/Silanoa/model_pointage)

### zeroRL *(co-founder)*

[zeroRL](https://github.com/Dar-rius/zeroRL) is a full **PyTorch** reinforcement-learning framework built for experiment control — not a thin wrapper around a single algo.

You can work at three levels of abstraction:
- **High-level** — `easy_train_ppo` for a complete PPO run (agent, vectorized envs, buffer, logging) in a few lines
- **Mid-level** — `BaseTrain` with swappable agent, env, buffer, and update function
- **Low-level** — primitives to assemble the training loop yourself (`Buffer`, GAE/PPO ops, logging, env helpers)

Includes Gymnasium integration, custom **MuJoCo** environments, config system (`TrainConfig` / `AlgoConfig`), TensorBoard / W&B tracking, checkpointing, and a growing example suite. On PyPI: [`zerorl`](https://pypi.org/project/zerorl/) (Apache-2.0).

I contribute across the stack: training pipeline, envs & examples, Windows support, logging/export, and CI.

### MyDIT

University platform (admin + students) I helped take to production: Laravel modules, integrations, deploy — including connecting SmartAttendance to campus workflows.

---

## Teaching labs

Built for courses I teach (IoT / data / ML practice):

| Repo | Focus |
| --- | --- |
| [projet1-dht22-thingsboard-](https://github.com/Silanoa/projet1-dht22-thingsboard-) | ESP32 DHT22 → ThingsBoard (MQTT) + PC simulation |
| [projet2-pompe-meteo-ml](https://github.com/Silanoa/projet2-pompe-meteo-ml) | Greenhouse: ESP32 pump + weather ML agent + ThingsBoard |
| [projet3-iot-telegram](https://github.com/Silanoa/projet3-iot-telegram) | IoT alerts via Telegram bot |

### Hotel chatbot

Hotel ops chatbot (booking, services, cancellations): PyTorch intent model, NLTK, MySQL, plus an RL loop to improve replies over time — [Silanoa/hotel-chatbot](https://github.com/Silanoa/hotel-chatbot).

---

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

ML / DL · Computer Vision · NLP · RL · data pipelines

---

## Currently

- Extending **SmartAttendance** toward adaptive video analytics and writing papers on that track
- Pushing **[zeroRL](https://github.com/Dar-rius/zeroRL)** further — APIs, algorithms, envs, developer experience
- Actively exploring opportunities in **AI / ML** and **full-stack**
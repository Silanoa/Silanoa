# Rosalex Ahan

**AI Engineer · Full-Stack Developer** · Dakar, Senegal

Co-founder of [zeroRL](https://github.com/Dar-rius/zeroRL) · Building and running AI systems at [DIT](https://dit.sn)

[LinkedIn](https://www.linkedin.com/in/rosalexahan/) · [Email](mailto:rosalexahan2@gmail.com) · [X](https://twitter.com/a_rosalex)

---

## About

- ~3 years building ML systems and full-stack apps, including production deployments
- MSc Artificial Intelligence, **Dakar Institute of Technology** (Very Good, class valedictorian)
- Teach Python, data collection, and deep learning
- Open to **AI / ML engineering roles** (computer vision, applied ML, RL tooling)

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

**Research direction (papers in progress)**  
Operational stack today = perception + thresholded decisions + persistence. Next layer from the same video streams: spatio-temporal patterns (schedules, co-presence, cross-camera transitions), clustering recurrent unknowns into stable identities, calibrated behavioral anomaly alerts, and a continuous-learning loop with a reproducible evaluation protocol.

**Repo:** [Silanoa/model_pointage](https://github.com/Silanoa/model_pointage)

### zeroRL *(co-founder)*

[zeroRL](https://github.com/Dar-rius/zeroRL) is a modular **PyTorch** RL framework: high-level PPO (`easy_train_ppo`), mid-level `BaseTrain` with swappable agent/env/buffer/update, and low-level primitives for custom loops. Gymnasium + custom MuJoCo. On PyPI: [`zerorl`](https://pypi.org/project/zerorl/).

I work on the library itself — training stack, envs/examples, Windows support, logging/export, CI — not only MuJoCo demos. Goal: keep the pipeline explicit and usable for research experiments.

### MyDIT

University platform (admin + students) I helped take to production: Laravel modules, integrations, deploy — including connecting SmartAttendance to campus workflows.

---

## Teaching labs

Built for courses I teach (IoT / data / ML practice):

| Repo | Focus |
| --- | --- |
| [projet1-dht22-thingsboard-](https://github.com/Silanoa/projet1-dht22-thingsboard-) | ESP32 DHT22 → ThingsBoard (MQTT) + PC simulation |
| [projet2-pompe-meteo-ml](https://github.com/Silanoa/projet2-pompe-meteo-ml) | Greenhouse: ESP32 pump + weather ML agent + ThingsBoard |

### Hotel chatbot

Hotel ops chatbot (booking, services, cancellations): PyTorch intent model, NLTK, MySQL, plus an RL loop to improve replies over time — [Silanoa/hotel-chatbot](https://github.com/Silanoa/hotel-chatbot).

---

## Stack

`Python` · `PyTorch` · `OpenCV` · `InsightFace` · `CUDA/ONNX` · `Laravel` · `Django` · `Flask` · `Vue` · `React` · `PostgreSQL` · `Docker`

ML / DL · Computer Vision · NLP · RL · data pipelines

---

## Currently

- Extending **SmartAttendance** toward adaptive video analytics and writing papers on that track
- Improving **[zeroRL](https://github.com/Dar-rius/zeroRL)** as a serious research RL toolkit (APIs, algorithms, envs, DX)
- Looking for my next role in **AI / ML engineering**
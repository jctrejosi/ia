# Guía de Modelos LLM y Interfaces Gráficas para Ejecución Local

Este documento presenta una lista de modelos de lenguaje que puedes correr localmente en CPU con aproximadamente 13 GB de RAM y un procesador Intel i7-13700H, junto con frameworks e interfaces gráficas compatibles para facilitar su uso.

---

## Modelos LLM compatibles con CPU (13 GB RAM)

| Modelo                      | Tamaño (paráms.) | Cuantizaciones CPU                    | RAM recomendada | Casos de uso especializados                              | Idiomas                  | Formato | Fuente confiable           | Frameworks compatibles                            |
|-----------------------------|------------------|-------------------------------------|-----------------|---------------------------------------------------------|--------------------------|---------|----------------------------|-------------------------------------------------|
| **Meta LLaMA 7B**           | 7 000M           | Q3_K, Q4_0, Q4_K, Q5_K, Q6_K, Q8_0 | ~6–7 GB         | Generación de texto/instrucciones                       | Múltiples (inglés, etc.)  | GGUF    | HuggingFace (TheBloke)     | llama.cpp, GPT4All, text-generation-webui, KoboldCpp |
| **Meta LLaMA 2 – 7B**       | 7 000M           | Q2_K, Q3_K, Q4_0, Q4_K, Q5_K, Q6_K | ~6–7 GB         | Conversación e instructivo                              | Inglés (multilingüe)      | GGUF    | HuggingFace (TheBloke)     | llama.cpp, GPT4All, text-generation-webui, KoboldCpp |
| **Nous Hermes 2 (Mistral 7B)** | 7 000M         | Q4_K, Q5_K, Q6_K, Q8_0 (K-quant)   | ~6–8 GB         | Generación texto, automatización, análisis, código     | Inglés                   | GGUF    | HuggingFace (NousResearch) | llama.cpp, GPT4All, text-generation-webui        |
| **Phi-3 Mini Instruct**     | 3 800M           | Q4_K (int4)                        | ~2–3 GB         | Chat e instrucción general                             | Inglés                   | GGUF    | HuggingFace (llmware)      | llama.cpp, GPT4All                               |
| **Orca Mini v3 – 7B**       | 7 000M           | Q3_K, Q4_0, Q4_K, Q5_K, Q6_K, Q8_0 | ~6–7 GB         | Chatbot, traducción, resúmenes                         | Multilingüe (EN, ES, FR, DE) | GGUF  | HuggingFace (TheBloke)     | llama.cpp, GPT4All, text-generation-webui        |
| **GPT4All-Falcon 7B**       | 7 000M           | Q4_0, Q4_1, Q5_0, Q5_1, Q6_K, Q8_0 | ~6–7 GB         | Chat general y programación                            | Inglés                   | GGUF    | HuggingFace (maddes8cht)   | GPT4All, llama.cpp                              |
| **Vicuna 7B v1.5**          | 7 000M           | Q2_K, Q3_K, Q4_K, Q5_K, Q6_K       | ~6–7 GB         | Asistente de chat (conversaciones)                     | Inglés (base Llama)      | GGUF    | HuggingFace (TheBloke)     | llama.cpp, GPT4All, text-generation-webui        |
| **MPT-7B**                  | 7 000M           | Q4_0, Q4_1, Q5_0, Q5_1, Q8_0       | ~6–7 GB         | Texto y código (entrenado en 1T tokens)                | Inglés                   | GGML    | HuggingFace (TheBloke)     | llama.cpp, text-generation-webui                 |
| **StableLM Zephyr – 3B**    | 3 000M           | Q3_K, Q4_K, Q5_K, Q6_K             | ~4–5 GB         | Conversación en inglés, LLM general                    | Inglés                   | GGUF    | HuggingFace (TheBloke)     | llama.cpp, GPT4All                               |
| **CodeLlama 7B Instruct**   | 7 000M           | Q2_K, Q3_K, Q4_K, Q5_K, Q6_K, Q8_0 | ~6–7 GB         | Generación y asistencia en código                      | Inglés (código)          | GGUF    | HuggingFace (TheBloke)     | llama.cpp, GPT4All, text-generation-webui        |

---

## Interfaces gráficas compatibles con modelos LLM

| Interfaz gráfica                                       | Compatibilidad                           | Funcionalidad clave                          | Soporte para modelos         | Links                                                                                                    |
| ----------------------------------------------------- | --------------------------------------- | -------------------------------------------- | ---------------------------- | -------------------------------------------------------------------------------------------------------- |
| **Text Generation Web UI** (o `text-generation-webui`) | Soporta GGML, GGUF, llama.cpp, GPT4All | Chat, generación texto, ajuste de parámetros | Modelos 7B, 13B, cuantizados | [https://github.com/oobabooga/text-generation-webui](https://github.com/oobabooga/text-generation-webui) |
| **Hugging Face Spaces (local)**                        | Carga modelos en HuggingFace con GUI web | Chat y demo web                              | Modelos LLaMA 7B y más       | [https://huggingface.co/spaces](https://huggingface.co/spaces)                                           |
| **KoboldCpp**                                          | Compatible con GGML, llama.cpp           | Chat, generación narrativa                   | Modelos 7B, 13B, optimizados | [https://github.com/KoboldAI/KoboldCpp](https://github.com/KoboldAI/KoboldCpp)                           |
| **Vicuna GUI** (basada en llama.cpp)                   | Especializada en modelos Vicuna 7B       | Chat para asistentes AI                      | Vicuna 7B y compatibles      | [https://github.com/lm-sys/FastChat](https://github.com/lm-sys/FastChat)                                 |
| **Alpaca-LoRA GUI**                                    | Carga modelos Alpaca y variantes LoRA    | Chat y fine-tuning simple                    | Alpaca 7B, Vicuna            | [https://github.com/tloen/alpaca-lora](https://github.com/tloen/alpaca-lora)                             |

---

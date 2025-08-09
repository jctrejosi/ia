# Modelos LLM

Este documento presenta una lista de modelos de lenguaje que puedes correr localmente en CPU con aproximadamente 13 GB de RAM y un procesador Intel i7-13700H, junto con frameworks e interfaces gráficas compatibles para facilitar su uso.

---

## Modelos LLM compatibles con CPU i7 y RAM 8 GB

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

## Modelos de Gama Media Compatibles con CPU i7 y 13 GB RAM

A continuación, se presentan modelos de lenguaje (LLMs) de aproximadamente 8 a 13 mil millones de parámetros, optimizados para correr en CPU sin GPU, usando hasta 13 GB de RAM. Estos modelos están cuantizados (Q4_K, Q5_K, etc.) para ajustarse a estas restricciones y son compatibles con frameworks como llama.cpp, GPT4All o KoboldCpp.

| Nombre del modelo          | Parámetros | Cuantizaciones disponibles                      | RAM recomendada | Casos de uso                                      | Idiomas soportados          | Formato | Fuente de descarga                                   |
|---------------------------|------------|------------------------------------------------|-----------------|--------------------------------------------------|----------------------------|---------|------------------------------------------------------|
| **Llama 2 13B**           | 13B        | Q2_K, Q3_K (S/M/L), Q4_0, Q4_K_S/M, Q4_1, Q5_0, Q5_K_S/M | ≈12–13 GB      | Asistente conversacional e inferencia de texto   | Inglés                     | GGUF    | Hugging Face (TheBloke/Llama-2-13B-GGUF)             |
| **LLaMA 13B**             | 13B        | Q2_K, Q3_K (S/M/L), Q4_0, Q4_K_S/M, Q5_0, Q5_K_S/M           | ≈12 GB        | Generación de texto general, chat e instrucciones | Inglés                     | GGUF    | Hugging Face (TheBloke/LLaMA-13b-GGUF)               |
| **Vicuna 13B v1.5**       | 13B        | Q2_K, Q3_K (S/M/L), Q4_0, Q4_K_S/M, Q5_0, Q5_K_S/M           | ≈12 GB        | Chatbot conversacional                             | Inglés (limitado multilingüe) | GGUF  | Hugging Face (TheBloke/vicuna-13B-v1.5-GGUF)         |
| **WizardLM 13B V1.2**     | 13B        | Q2_K, Q3_K (S/M/L), Q4_0, Q4_K_S/M, Q5_0, Q5_K_S/M           | ≈12 GB        | Asistente conversacional e instructivo            | Inglés                     | GGUF    | Hugging Face (TheBloke/WizardLM-13B-V1.2-GGUF)       |
| **WizardLM 13B Uncensored** | 13B      | Q2_K, Q3_K (S/M/L), Q4_0, Q4_K_S/M, Q5_0, Q5_K_S/M           | ≈12 GB        | Asistente conversacional sin filtros              | Inglés                     | GGUF    | Hugging Face (TheBloke/WizardLM-13B-Uncensored-GGUF) |

> **Nota:** Todos estos modelos están cuantizados para ajustarse a la memoria RAM disponible y correr eficientemente en CPU sin requerir GPU dedicada. Son ideales para tareas de chat, generación de texto y asistencia conversacional en inglés, y compatibles con frameworks populares como llama.cpp, GPT4All y KoboldCpp.

## Interfaces gráficas compatibles con modelos LLM

| Interfaz gráfica                                       | Compatibilidad                           | Funcionalidad clave                          | Soporte para modelos             | Links                                                                                                    |
| ----------------------------------------------------- | --------------------------------------- | -------------------------------------------- | -------------------------------- | -------------------------------------------------------------------------------------------------------- |
| **Text Generation Web UI** (o `text-generation-webui`) | Soporta GGML, GGUF, llama.cpp, GPT4All | Chat, generación texto, ajuste de parámetros | Modelos 7B a 13B, cuantizados    | [https://github.com/oobabooga/text-generation-webui](https://github.com/oobabooga/text-generation-webui) |
| **Hugging Face Spaces (local)**                        | Carga modelos en HuggingFace con GUI web | Chat y demo web                              | Modelos LLaMA 7B, 13B y más     | [https://huggingface.co/spaces](https://huggingface.co/spaces)                                           |
| **KoboldCpp**                                          | Compatible con GGML, llama.cpp           | Chat, generación narrativa                   | Modelos 7B a 13B, optimizados    | [https://github.com/KoboldAI/KoboldCpp](https://github.com/KoboldAI/KoboldCpp)                           |
| **Vicuna GUI (FastChat)**                              | Especializada en modelos Vicuna 7B y 13B | Chat para asistentes AI                      | Vicuna 7B y 13B                 | [https://github.com/lm-sys/FastChat](https://github.com/lm-sys/FastChat)                                 |
| **Alpaca-LoRA GUI**                                    | Carga modelos Alpaca y variantes LoRA    | Chat y fine-tuning simple                    | Alpaca 7B, Vicuna               | [https://github.com/tloen/alpaca-lora](https://github.com/tloen/alpaca-lora)                             |

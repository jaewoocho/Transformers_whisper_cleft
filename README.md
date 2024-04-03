# Fine-tuning Whisper on Speech Pathology
![image](https://github.com/jaewoocho/Transformers_whisper_cleft/assets/25238652/3d47cdc3-ee14-4913-81ab-4c2efb6e1932)
# 00. Fine-tuning Whisper on Speech Language Pathology
# 01. Overview
- The goal of the Cleft Palate project at Vanderbilt DSI is to classify audio clips of patients' voices as containing hypernasality (a speech impediment) or not. The patients with hypernasality can then be recommended for speech pathology intervention. This is currently evaluated by human speech pathologists, which requires access to these medical providers. Our hope is to train a model that can classify this speech impediment for expedited patient access to a speech pathologist.
- We plan to use the Whisper embedings from OpenAI and train a classification model, either using Whisper with a sequence classification head or another classification LLM.
- This project will be presented to the 2024 VOICE AI SYMPOSIUM at Tampa, Florida

# 02. OPENAI Whisper Model 
- The Whisper model from OpenAI is an automatic speech recognition (ASR) system designed to provide highly accurate transcriptions. It's known for its capability to handle a wide range of audio qualities and accents. The model was trained on a diverse dataset comprising various languages and noisy environments, which contributes to its robustness and versatility. Whisper's proficiency lies in not just transcribing but also in its ability to identify the language being spoken. This feature makes it a valuable tool for multilingual transcription tasks. OpenAI developed Whisper with the aim of enhancing accessibility and bridging communication barriers in various applications, from voice assistants to transcription services.
![image](https://github.com/jaewoocho/Transformers_whisper_cleft/assets/25238652/bad84052-3c7c-4524-b8d5-f0da8bc0f86f)
![image](https://github.com/jaewoocho/Transformers_whisper_cleft/assets/25238652/422985cb-39ca-4de6-9a83-8733bc4240d8)


# 03. Interactive Demonstration
- Interactive demonstration: https://huggingface.co/spaces/jcho02/Transformers_whisper_cleft 

# 04. Model card
- [Descriptive card covering uses, sources, permissions, code](https://huggingface.co/jcho02/whisper_cleft)
  
# 05. Code Demonstration 
 - Whisper Model Code Explanation - Pure audio data without noise:
   - https://github.com/jaewoocho/Transformers_whisper_cleft/blob/main/Explaning_whisper_model_code_without_noise.ipynb
 - Whisper Model Results - audio data with noise:
   - https://github.com/jaewoocho/Transformers_whisper_cleft/blob/main/cleft_palate_notebook_with_noise.ipynb 
   
# 06. Critical Anaylsis 
  - What is the impact of this project?
  - What does it reveal or suggest?
  - What is the next step?

# 07. Resource Links
  - https://arxiv.org/abs/2212.04356
  - https://openai.com/research/whisper 
  - https://github.com/openai/whisper 
  - https://platform.openai.com/docs/guides/speech-to-text
  - https://replicate.com/openai/whisper
  - https://learn.microsoft.com/en-us/azure/ai-services/speech-service/whisper-overview
  - Special Thanks for Myranda for helping!

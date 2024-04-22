# Fine-tuning Whisper on Speech Pathology
![image](https://github.com/jaewoocho/Transformers_whisper_cleft/assets/25238652/3d47cdc3-ee14-4913-81ab-4c2efb6e1932)
# 00. Fine-tuning Whisper on Speech Language Pathology
# 01. Overview
- The goal of the Cleft Palate project at Vanderbilt DSI is to classify audio clips of patients' voices as containing hypernasality (a speech impediment) or not. The patients with hypernasality can then be recommended for speech pathology intervention. This is currently evaluated by human speech pathologists, which requires access to these medical providers. Our hope is to train a model that can classify this speech impediment for expedited patient access to a speech pathologist.
- We plan to use the Whisper embedings from OpenAI and train a classification model, either using Whisper with a sequence classification head or another classification LLM.
- This project will be presented to the 2024 VOICE AI SYMPOSIUM at Tampa, Florida
![image](https://github.com/jaewoocho/Transformers_whisper_cleft/assets/25238652/c63a21d4-c0ee-40c4-94ce-d6e4ccc2a2da)
![image](https://github.com/jaewoocho/Transformers_whisper_cleft/assets/25238652/a80b9fdf-0eb3-494c-99fb-cd91f29637ba)

# 02. OPENAI Whisper Model 
- The Whisper model from OpenAI is an automatic speech recognition (ASR) system designed to provide highly accurate transcriptions. It's known for its capability to handle a wide range of audio qualities and accents. The model was trained on a diverse dataset comprising various languages and noisy environments, which contributes to its robustness and versatility. Whisper's proficiency lies in not just transcribing but also in its ability to identify the language being spoken. This feature makes it a valuable tool for multilingual transcription tasks. OpenAI developed Whisper with the aim of enhancing accessibility and bridging communication barriers in various applications, from voice assistants to transcription services.
![image](https://github.com/jaewoocho/Transformers_whisper_cleft/assets/25238652/bad84052-3c7c-4524-b8d5-f0da8bc0f86f)
![image](https://github.com/jaewoocho/Transformers_whisper_cleft/assets/25238652/422985cb-39ca-4de6-9a83-8733bc4240d8)

## The Original Whisper Model
  - Takes audio data as input and translates it into text as output.
  - Input: Audio - "This apple is red"
  - Output: Text - "This apple is red"
    
## The Finetuned Whisper Model
  - Takes audio data as input and classifies it as hypernasility or not as output
  - Input: Audio file "This apple is red"
  - Output: 0 or 1, which translates into Text - "Hypernasility(Speech impediment) is Detected"

## What has changed?
  - A new class called SpeechClassifier is created, which utilizes Whisper's encoder and adds a series of dense layers for classification.
  - This class modifies the Whisper model's output to make it suitable for audio classification tasks by implementing a custom forward method that processes encoder outputs through these additional layers to classify different sounds .
![image](https://github.com/jaewoocho/Transformers_whisper_cleft/assets/25238652/20c2a213-ee53-423e-96e0-faff91fc6d4e)


# 03. Interactive Demonstration
- Interactive demonstration: https://huggingface.co/spaces/jcho02/Transformers_whisper_cleft 

# 04. Model card
- Model Card: [Descriptive card covering uses, sources, permissions, code](https://huggingface.co/jcho02/whisper_cleft)
  
# 05. Code Demonstration 
 - Whisper Model Code Explanation - Pure audio data without noise:
   - https://github.com/jaewoocho/Transformers_whisper_cleft/blob/main/Explaning_whisper_model_code_without_noise.ipynb
 - Whisper Model Results - audio data with noise:
   - https://github.com/jaewoocho/Transformers_whisper_cleft/blob/main/cleft_palate_notebook_with_noise.ipynb
  
# 05A - Results
![image](https://github.com/jaewoocho/Transformers_whisper_cleft/assets/25238652/e081f5e2-2c09-4050-b573-04943afc0331)

   
# 06. Critical Anaylsis 
  - What is the impact of this project?
    -  This project could make speech disorder diagnosis quicker and more accessible, especially in areas where speech pathologists are scarce. It has the potential to:
      - Streamline hypernasality detection, speeding up patient access to treatment.
      - Help speech pathologists by handling initial assessments, allowing them to focus on treatment plans.
  - What is the next step?
    -  Undergo extensive testing to ensure reliability across various speech patterns.
    -  Conduct clinical trials to validate its practical effectiveness.
    -  Continuously improve based on real-world feedback and data.
    -  Explore applications for other speech disorders and different languages.
    -  Presenting at the 2024 VOICE AI SYMPOSIUM will be a chance to gather expert insights and explore further development opportunities.

# 07. Resource Links
  - https://arxiv.org/abs/2212.04356
  - https://openai.com/research/whisper 
  - https://github.com/openai/whisper 
  - https://platform.openai.com/docs/guides/speech-to-text
  - https://replicate.com/openai/whisper
  - https://learn.microsoft.com/en-us/azure/ai-services/speech-service/whisper-overview
  - Special Thanks for Myranda & Team for helping!

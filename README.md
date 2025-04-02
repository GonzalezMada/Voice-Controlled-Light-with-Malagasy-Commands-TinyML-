# 🎤Voice-Controlled Light with Malagasy Commands & TinyML  

**Control lights using voice commands in Malagasy**, a TinyML project deployed on Arduino Nano 33 BLE Sense.  
*"Mirehitra" (Light On) | "Maty" (Light Off)*  

---

## 🌟 Project Overview  
This project demonstrates how to train a **Convolutional Neural Network (CNN)** to recognize Malagasy voice commands and deploy it on a microcontroller using **TensorFlow Lite Micro**. The AI model processes audio signals to control a light bulb via Malagasy keywords, bridging language gaps in voice technology.  

**Key Features**:  
- 🗣️ Supports **Malagasy language** (under-resourced in voice tech).  
- 🔋 Runs on a **coin-cell battery** with Arduino Nano 33 BLE Sense.  

---

## 🛠️ Hardware & Software  
**Hardware**:  
- Arduino Nano 33 BLE Sense Rev2 (with built-in microphone).  
- Light bulb
- Relay module
- 5V-6V battery

**Software**:  
- Google Colab (GPU for training)  
- TensorFlow
- Arduino IDE  

---

## 📂 Project Structure  
```bash
├── Training/  
│   └── train_voice_control_model_with_malagasy_words.ipynb  # Model training & quantization  
├── voice_command_based_on_TinyML/  
     └── voice_command_based_on_TinyML.ino                    # Arduino deployment code  
     └── arduino_audio_provider.cpp
     └── arduino_command_responder.cpp
     └── arduino_main.cpp
     └── audio_provider.h
     └── command_responder.h
     └── feature_provider.cpp
     └── feature_provider.h
     └── main_functions.h
     └── micro_features_micro_features_generator.cpp
     └── micro_features_micro_features_generator.h
     └── micro_features_micro_model_settings.cpp
     └── micro_features_micro_model_settings.h
     └── micro_features_model.cpp
     └── micro_features_model.h
     └── recognize_commands.cpp
     └── recognize_commands.h

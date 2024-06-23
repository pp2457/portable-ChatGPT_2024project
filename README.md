# portable-ChatGPT

## Team Workers
```電機3B 01053104 游恩傑```
```電機3B 01089001 陳宜真```
```電機3B 01153205 彭姸蓁```

---

## Product Definition
可攜式的ChatGPT裝置在設計上應該具有以下功能：<br>
1. 語音交互: 能夠透過語音與使用者進行交互，讓使用者能夠自然地與ChatGPT進行對話。
2. 文字輸入: 除了語音交互外，也應該支援文字輸入，以便在需要時進行靜默操作或者在環境不適合語音交互時使用。
3. 智能對話能力: 具有ChatGPT的核心功能，能夠理解和回應使用者的提問、請求、指令等，並提供相應的回答或解決方案。
4. 個性化設定: 允許使用者根據自己的喜好和需求，對ChatGPT的個性、口吻、語調等進行設定，以使對話更加符合使用者的期望。
5. 即時翻譯: 具有即時翻譯功能，能夠將不同語言的對話翻譯成使用者所選擇的目標語言，從而促進跨語言溝通。
6. 智能建議與推薦: 根據使用者的對話內容和需求，提供相應的建議、推薦或資訊，以幫助使用者解決問題或者滿足需求。
7. 本地化: 考慮到不同地區的文化和語言特點，應該支援多種語言和地區的本地化設定，以提供更加貼近當地用戶的使用體驗。
8. 隱私保護: 尊重使用者的隱私，不收集或者僅收集必要的個人信息，並提供選項讓使用者控制其數據的使用和共享。
9. 學習能力: 具有一定程度的學習能力，能夠根據與使用者的互動不斷優化自身的回答和表現，提供更加智能和個性化的服務
10. 連接性: 具有Wi-Fi或藍牙等連接功能，以便與互聯網或其他設備進行連接，從而擴展其功能或者進行遠程更新和管理。

---
## Project Overview

### 內容
旨在設計並實作一個智慧語音回覆系統。系統以AMB82-mini微控制器和ILI9341 TFT LCD顯示屏為硬體基礎，透過與伺服器的連接，使用先進的LLM進行語音處理和答案生成。最終目標是接受語音輸入並在顯示屏上顯示相應的回覆。

### Prototype Features
1. Audio/Speech Recognition
2. Post Audio to LLM server
3. Receive Generated-Text from LLM server
4. Display Text on TFT-LCD

在伺服器上配置高性能的大規模語言模型（如GPT-4）進行語音識別和自然語言處理。
通過API接口實現微控制器與伺服器之間的數據交互。

### 顯示與回覆
* 設計簡潔俐落的顯示界面，確保回覆內容清晰易讀。
* 優化顯示刷新率和數據傳輸速度，確保系統即時響應能力。

### 預期成果
實現一個完整的語音回覆系統，使用者透過語音輸入問題，系統能夠快速生成並顯示答案。不僅展示了語音處理技術與LLM模型應用潛力，也為智慧家居、自動問答系統等領域提供了實踐基礎。

### 應用前景
本系統可應用於多種場景，包括但不限於智慧家居中的語音助手、客服機器人提供的自動問答以及教育領域中的智能教學助手。通過這次專題的研究和實作，我們希望進一步推動語音技術與人工智慧的融合發展，為未來的智慧生活帶來更多可能性。

---
## System Architecture
### 硬體部分

* AMB82-mini微控制器：負責初步處理語音輸入和數據傳輸。

* ILI9341 TFT LCD顯示屏：用於顯示系統的回覆和相關信息。

### 軟體部分

* 語音輸入處理：透過麥克風模組捕獲使用者的語音輸入並轉換為數據格式。

* 數據傳輸：通過無線網路或其他方式將處理後的語音數據發送至伺服器。

* 伺服器端LLM模型處理：伺服器接收語音數據後，使用大規模語言模型進行語音識別和生成相應的文本回覆。

* 回覆顯示：將伺服器生成的回覆傳送至AMB82-mini，並在ILI9341 TFT LCD顯示屏上顯示。

---

## Development Board Introduction
### AMB82-MINI overview
<p><img width="50%" height="50%" src="https://www.amebaiot.com/wp-content/uploads/2023/03/amb82_mini.png"></p>

[RTL8735B](https://www.amebaiot.com/en/amebapro2/): 32-bit Arm v8M, up to 500MHz, 768KB ROM, 512KB RAM, 16MB Flash (MCM embedded DDR2/DDR3L up to 128MB) 802.11 a/b/g/n WiFi 2.4GHz/5GHz, BLE 5.1, NN Engine 0.4 TOPS, Crypto Engine, Audo Codec, …

* [Ameba Arduino](https://www.amebaiot.com/en/ameba-arduino-summary/)

* [Amebapro2 AMB82-mini Arduino Example Guides](https://www.amebaiot.com/en/amebapro2-amb82-mini-arduino-peripherals-examples)

* [Amebapro2 AMB82-mini Arduino getting started](https://www.amebaiot.com/en/amebapro2-amb82-mini-arduino-getting-started/)

---
## System Block Diagram
* Portable-ChatGPT System Diagrams
<p><img width="50%" height="50%" src="https://github.com/pp2457/portable_ChatGPT/blob/85dcdfbe61561577165294c484b3548a1e87047e/assets/Portable-ChatGPT_System_Diagram.png?raw=true"></p>

* Development Kit Diagram : AMB82-MINI, ILI9341 LCD 240x320, PAM8403
<p><img width="50%" height="50%" src="https://github.com/pp2457/portable_ChatGPT/blob/d3523de57f00304110b467f539701af62c7ad2a1/assets/FlowChart.jpg?raw=true"></p>

---
## Code
AMB82-mini in Arduino IDE: [https://github.com/pp2457/portable_ChatGPT/blob/4c51eb501ad28c4968a9be072aff64677aa69bdc/gistfile1.py](https://github.com/pp2457/portable_ChatGPT/blob/4c51eb501ad28c4968a9be072aff64677aa69bdc/gistfile1.py)
```
/*

 Example guide:
 https://www.amebaiot.com/en/amebapro2-arduino-neuralnework-face-audio-classification/
  
 1. To run Server on PC:
    cd ~/Arduino/examples/AMB82-MINI/src
    python AmebaPro2_Whisper_LLM_server.py
    
 2. To run client on AMB82-mini:   
    upload this code to AMB82-mini, and hit reset to start the client on AMB82-mini,
    press button for 2 seconds to speak to AMB82-mini
    AMB82-mini will record voice to MP4 file on SDcard, 
    then send to AmebaPro2_Whisper_LLM_server

*/

#include "string.h"
#include "StreamIO.h"
#include "AudioStream.h"
#include "AudioEncoder.h"
#include "MP4Recording.h"
#include "WiFi.h"
#include "AmebaFatFS.h"
#include "Base64.h"
#include "ArduinoJson.h"
#include "SPI.h"
#include "AmebaILI9341.h"
#include "NNAudioClassification.h"
#include "AudioClassList.h"

// NN audio classification requires 16KHz
AudioSetting configA(16000, 1, USE_AUDIO_AMIC);    // Sample rate, Channel count, Mic type
Audio audio;
NNAudioClassification audioNN;
StreamIO audioStreamerNN(1, 1);    // 1 Input Audio -> 1 Output Audio Classification

int max_id = 0;
int max_prob = 0;

#define TFT_RESET 5
#define TFT_DC    4
#define TFT_CS    SPI_SS

AmebaILI9341 tft = AmebaILI9341(TFT_CS, TFT_DC, TFT_RESET);

#define ILI9341_SPI_FREQUENCY 20000000

#define FILENAME "TestRecordingAudioOnly.mp4"

char ssid[] = "Your_SSID";              // your network SSID (Home WiFi or Smartphone Hotspot)
char pass[] = "Your_Password";        // your network password
int status = WL_IDLE_STATUS;

char server[] = "123.195.32.57";   // the server IP running HTTP server on PC
#define PORT 5000

AmebaFatFS fs;
WiFiClient wifiClient;

char buf[512];
char *p;
String filepath;
File file;

// Default audio preset configurations:
// 0 :  8kHz Mono Analog Mic
// 1 : 16kHz Mono Analog Mic
// 2 :  8kHz Mono Digital PDM Mic
// 3 : 16kHz Mono Digital PDM Mic
AAC aac;
MP4Recording mp4;
StreamIO audioStreamer1(1, 1);    // 1 Input Audio -> 1 Output AAC
StreamIO audioStreamer2(1, 1);    // 1 Input AAC -> 1 Output MP4

const int buttonPin = 1;          // the number of the pushbutton pin
int buttonState;                          // variable for reading the pushbutton status
unsigned long buttonPressTime = 0;        // variable to store the time when button was pressed
bool buttonPressedFor2Seconds = false;    // flag to indicate if button is pressed for at least 2 seconds
int recordingstate = -1;
int previousRecordingState = -1;
bool blinkstate = false;

// Receiving Buffer
#define OFFSET 94              // skip HTTP response headers
#define PAGE_CHAR_LENGTH 26*15 // Font 2 = 26 characters per line, total 14 lines
char textbuffer[26*15*3];      // 3 pages buffer 
int  textcount = 0;
int  skipcount = 0;
int  displaycount =0;
//int  pos=0; // for finding "LLM:"

void setup()
{
    Serial.begin(115200);

    // Connection to internet
    while (status != WL_CONNECTED) {
        Serial.print("Attempting to connect to WPA SSID: ");
        Serial.println(ssid);
        status = WiFi.begin(ssid, pass);
        delay(2000);
    }

    SPI.setDefaultFrequency(ILI9341_SPI_FREQUENCY);
    tft.begin();
    tft.clr();
    tft.setCursor(0, 0);
    tft.setForeground(ILI9341_WHITE);
    tft.setFontSize(2);
    tft.setRotation(3);
    tft.println("Portable LLM : Llama3-TAIDE");

    // list files under root directory
    fs.begin();

    // initialize the pushbutton pin as an input:
    pinMode(buttonPin, INPUT);
    pinMode(LED_BUILTIN, OUTPUT);
    pinMode(LED_G, OUTPUT);

    // Configure audio peripheral for audio data format
    audio.configAudio(configA);
    audio.begin();
    // Configure AAC audio encoder
    aac.configAudio(configA);
    aac.begin();    

    audioNN.configAudio(configA);
    audioNN.setResultCallback(ACPostProcess);
    audioNN.modelSelect(AUDIO_CLASSIFICATION, NA_MODEL, NA_MODEL, NA_MODEL, DEFAULT_YAMNET);
    audioNN.begin();

    // Configure StreamIO object to stream data from audio to audio classification
    audioStreamerNN.registerInput(audio);
    audioStreamerNN.registerOutput(audioNN);
    if (audioStreamerNN.begin() != 0) {
        Serial.println("StreamIO link start failed");
    }
    // Configure MP4 recording settings
    mp4.configAudio(configA, CODEC_AAC);
    mp4.setRecordingDuration(5);
    mp4.setRecordingFileCount(1);
    mp4.setRecordingFileName("TestRecordingAudioOnly");
    mp4.setRecordingDataType(STORAGE_AUDIO);    // Set MP4 to record audio only

    // Configure StreamIO object to stream data from audio channel to AAC encoder
    audioStreamer1.registerInput(audio);
    audioStreamer1.registerOutput(aac);
    if (audioStreamer1.begin() != 0) {
        Serial.println("StreamIO link start failed");
    }

    // Configure StreamIO object to stream data from AAC encoder to MP4
    audioStreamer2.registerInput(aac);
    audioStreamer2.registerOutput(mp4);
    if (audioStreamer2.begin() != 0) {
        Serial.println("StreamIO link start failed");
    }    
}

void loop()
{  
    // Button state
    int newButtonState = digitalRead(buttonPin);
    if (newButtonState != buttonState) {
        buttonPressTime = millis();
    }
    // update button state
    buttonState = newButtonState;

    // update recording state
    recordingstate = (int)(mp4.getRecordingState());
/*
    // check if the button has been held for at least 2 seconds
    if (buttonState == HIGH && millis() - buttonPressTime >= 2000) {
        // button has been pressed for at least 2 seconds
        buttonPressedFor2Seconds = true;
    } else if (voiceActivated){
        // Speech detected
        buttonPressedFor2Seconds = true;
        voiceActivated = false;
    } else {
        // button was released before 2 seconds
        buttonPressedFor2Seconds = false;
    }

    // if button has been pressed for at least 2 seconds
    if (buttonPressedFor2Seconds) {
        if (recordingstate == 1) {
            digitalWrite(LED_BUILTIN, HIGH);
        } else {
            mp4.begin();
            Serial.println("Recording");
            tft.clr();
            tft.setCursor(0,0);
        }
    }
*/    
    if (recordingstate == 1 && previousRecordingState == 0) {
        // Change from 0 to 1
        digitalWrite(LED_BUILTIN, HIGH);
    } else if (recordingstate == 0 && previousRecordingState == 1) {
        encodeMP4andsendHttpPostRequest();
        // Change from 1 to 0
        digitalWrite(LED_BUILTIN, LOW);  
    }
    // Check if there are incoming bytes available from the server
    textcount =0;    
    skipcount =0;
    while (wifiClient.available()) {
        char c = wifiClient.read();
        textbuffer[textcount] = c;
        if (textcount==0){
          tft.clr();
          tft.setCursor(0,0);
        }
        textcount++;
        skipcount++;
        Serial.write(c);
        if (skipcount>OFFSET) tft.print(c);
    }
// finding indexOf LLM:     
    // if (pos<=0) {
    //     String s = String(textbuffer);
    //     pos = s.indexOf("LLM:");
    //     Serial.print("LLM indexOf = ");
    //     erial.println(pos);
    //  }
    previousRecordingState = recordingstate;
    
}

// User callback function
void ACPostProcess(std::vector<AudioClassificationResult> results)
{
    printf("No of Audio Detected = %d\r\n", audioNN.getResultCount());

    if (audioNN.getResultCount() > 0) {
        max_id =0;
        max_prob =0;
        for (int i = 0; i < audioNN.getResultCount(); i++) {
            AudioClassificationResult audio_item = results[i];
            int class_id = (int)audio_item.classID();
            if (audioNames[class_id].filter) {
                int prob = audio_item.score();
                printf("%d class %d, score: %d, audio name: %s\r\n", i, class_id, prob, audioNames[class_id].audioName);
                if (prob > max_prob) {
                  max_id   = class_id;
                  max_prob = prob;
                }
            }
        }
        printf("MAX class %d, prob: %d, class_name: %s\r\n", max_id, max_prob, audioNames[max_id].audioName);
        
        if (max_id==0 && max_prob>80 && !recordingstate) {
          digitalWrite(LED_BUILTIN, HIGH);
          mp4.begin();
          Serial.println("Recording Audio...............");        
        }    
    }
}

void encodeMP4andsendHttpPostRequest()
{
    memset(buf, 0, sizeof(buf));
    fs.readDir(fs.getRootPath(), buf, sizeof(buf));
    filepath = String(fs.getRootPath()) + String(FILENAME);
    p = buf;
    while (strlen(p) > 0) {
        /* list out file name image will be saved as "TestRecordingAudioOnly.mp4"*/
        if (strstr(p, FILENAME) != NULL) {
            Serial.println("[INFO] Found 'TestRecordingAudioOnly.mp4' in the string.");
            Serial.println("[INFO] Processing file...");
        } else {
            // Serial.println("Substring 'image.jpg' not found in the
            // string.");
        }
        p += strlen(p) + 1;
    }
    uint8_t *fileinput;
    file = fs.open(filepath);
    unsigned int fileSize = file.size();
    fileinput = (uint8_t *)malloc(fileSize + 1);
    file.read(fileinput, fileSize);
    fileinput[fileSize] = '\0';
    file.close();

    // Encode the file data as Base64
    int encodedLen = base64_enc_len(fileSize);
    char *encodedData = (char *)malloc(encodedLen);
    base64_encode(encodedData, (char *)fileinput, fileSize);

    JsonDocument doc;

    //Change "base64_string" to the key that you set in your server.
    doc["base64_string"] = encodedData;
    String jsonString;
    serializeJson(doc,jsonString);

    if (wifiClient.connect(server, PORT)) {
        wifiClient.println("POST /audio HTTP/1.1");
        wifiClient.println("Host: " + String(server));
        wifiClient.println("Content-Type: application/json");    // Use appropriate content type
        wifiClient.println("Content-Length: " + String(jsonString.length()));              // Specify the length of the content
        wifiClient.println("Connection: keep-alive");
        wifiClient.println();             // Empty line indicates the end of headers
        wifiClient.print(jsonString);    // Send the Base64 encoded audio data directly
        
        Serial.println("Binary sent");
        tft.println("Voice sent to LLM server !");
        tft.println("wait a moment for LLM.....");
    }
}
```

Sever: [https://github.com/pp2457/portable_ChatGPT/blob/88df36f57f1b0887c4aa3be76dfd9119792797f6/server.py](https://github.com/pp2457/portable_ChatGPT/blob/88df36f57f1b0887c4aa3be76dfd9119792797f6/server.py)
```
## To run server: python AmebaPro2_whisper_llm_server.py
## To run client: RecordMP4_HTTP_Post_Audio.ino

# pip install git+https://github.com/openai/whisper.git
# pip install fastapi uvicorn
# pip install nest-asyncio
# pip install accelerate

from fastapi import FastAPI, HTTPException
from fastapi.responses import Response
from pydantic import BaseModel
import uvicorn
import base64

import whisper
ASR = whisper.load_model("base").to("cpu")

import torch
import transformers
from transformers import AutoModelForCausalLM , AutoTokenizer

### https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard

#model_name = "Q-bert/Mamba-130M"
#model_name = "Q-bert/Mamba-370M"
#model_name = "Q-bert/Mamba-790M"
#model_name = "Q-bert/Mamba-1B"
#model_name = "Q-bert/Mamba-3B"
#model_name = "Q-bert/Mamba-3B-slimpj"
#model_name = "mtgv/MobileLLaMA-1.4B-Chat"
#model_name = "TinyLlama/TinyLlama-1.1B-Chat-v1.0"
#model_name = "microsoft/phi-2"
#model_name = "microsoft/Phi-3-mini-4k-instruct"
#model_name = "microsoft/Phi-3-mini-128k-instruct"
#model_name = "microsoft/Orca-2-7b"
#model_name = "google/gemma-1.1-2b-it"
#model_name = "google/gemma-1.1-7b-it"
#model_name = "mistralai/Mistral-7B-Instruct-v0.2"
#model_name = "kaist-ai/mistral-orpo-beta" # fine-tuned mistral-7B-v0.1
#model_name = "openlm-research/open_llama_3b_v2"
#model_name = "openlm-research/open_llama_7b_v2"
#model_name = "lmsys/vicuna-7b-v1.5"
#model_name = "lmsys/vicuna-7b-v1.5-16k"
#model_name = "Nexusflow/Starling-LM-7B-beta"
#model_name = "meta-llama/Llama-2-7b-hf"
#model_name = "meta-llama/Llama-2-7b-chat-hf"
#model_name = "meta-llama/Meta-Llama-3-8B-Instruct"

#model_name = "ckip-joint/bloom-3b-zh" 
#model_name = "Qwen/Qwen1.5-7B-Chat" # 通义千问
#model_name = "01-ai/Yi-6B-Chat" # 零一万物
#model_name = "openbmb/MiniCPM-2B-128k" # 面壁智能 
#model_name = "yentinglin/Taiwan-LLM-7B-v2.0.1-chat" # 台大
#model_name = "MediaTek-Research/Breeze-7B-Instruct-v1_0" # 達哥
#model_name = "MediaTek-Research/Breeze-7B-32k-Instruct-v1_0" # 達哥
#model_name = "INX-TEXT/Bailong-instruct-7B" # 白龍
#model_name = "taide/TAIDE-LX-7B" # TAIDE
#model_name = "taide/TAIDE-LX-7B-Chat" # TAIDE
model_name = "taide/Llama3-TAIDE-LX-8B-Chat-Alpha1" # TIADE
print(model_name)

#LLM = AutoModelForCausalLM.from_pretrained(model_name, trust_remote_code=True, torch_dtype="auto", device_map="cuda")
LLM = AutoModelForCausalLM.from_pretrained(model_name, trust_remote_code=True, torch_dtype=torch.bfloat16, device_map="cuda")
tokenizer = AutoTokenizer.from_pretrained(model_name)

import nest_asyncio
nest_asyncio.apply()

app = FastAPI()

class Base64Data(BaseModel):
    base64_string: str

@app.get("/")
def home():
    return Response("hello")

@app.post("/audio")
async def post_audio(data: Base64Data):
    try:
        #Decode the base64 string
        decoded_data = base64.b64decode(data.base64_string)
        
        # print(decoded_data)
        #Save the decoded data to an MP4 file
        with open("output.mp4", "wb") as f:
            f.write(decoded_data)
      
        # Whisper transcribe
        result = ASR.transcribe("output.mp4",fp16=False)
        header1 = "ASR: "
        print(header1+result["text"])

        # LLM generate
        prompt = result["text"]
        input_ids = tokenizer.encode(prompt, return_tensors="pt").to("cuda")
        output = LLM.generate(input_ids, max_length=128, num_beams=5, no_repeat_ngram_size=2, pad_token_id=tokenizer.eos_token_id, do_sample=True)
        generated_text = tokenizer.decode(output[0], skip_special_tokens=True)
        #header2="LLM: "
        header2="TAIDE: "
        print(header2+generated_text) 
        return Response(header2+generated_text)
    except Exception as e:
        raise HTTPException(status_code=500, detail=str(e))


if __name__ == "__main__":
    uvicorn.run(app, host="0.0.0.0", port=5000, log_level="info")
```

---
## Demo Video
[![](https://img.youtube.com/vi/9A391s-49-o/0.jpg)](https://www.youtube.com/shorts/9A391s-49-o)



---


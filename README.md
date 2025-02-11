# AI-Generated-Text-Detection

This is most relavant project in the current era and the future, as this project aims to solve one of the most critical problems we face today...

It's 2024 and we can no longer trust the content we see on the internet. With the rise of AI-generated content, it's hard to distinguish between real and fake content. This project aims to solve this problem by detecting AI-generated text/content using a custom AI model trained on a large dataset.

This is an AI text/content detection program that makes use of a custom model trained using GPT-4, DebertaModel, DebertaModelv3, SlimPajama and other models, dataset & techiniques, to detect & score contents provided as input. It is fine-tuned on a large dataset to produce most accurate results.

[Snitch-GPT](https://snitch-gpt.vercel.app) ([Repo](https://github.com/jesvijonathan/Snitch-GPT-Frontend))

## Demo

![Youtube Video](https://img.youtube.com/vi/1Q1Q1Q1Q1Q1/maxresdefault.jpg)

## Prerequisites -

- CUDA-enabled GPU
- Python 3.10.6

## Installation Steps -

### 1. Check CUDA Information

Check and note down the CUDA information:

```bash
nvcc --version # or
nvidia-smi
```

### 2. Install CUDA Driver Toolkit

Download and install [CUDA driver toolkit](https://developer.nvidia.com/cuda-toolkit) if not installed already.
(This Project also works with CPU, but it's recommended to use a CUDA-enabled GPU for better performance)

### 3. Install Python 3.10.6

Download and install [Python 3.10.6](https://www.python.org/downloads/release/python-3106) if not installed already.
(I recommend using this version for compatibility with the torch dependencies)

### 4. Clone Main Repository

Clone the main repository & move into the directory:

```bash
git clone https://github.com/jesvijonathan/AI-Generated-Text-Detection
cd AI-Generated-Text-Detection
```

### 5. Download Weights

Download the model [Weights](https://www.mediafire.com/file/7n4b2e1geeuzu69/weights.zip/file) (~9GB) from [here](https://www.mediafire.com/file/7n4b2e1geeuzu69/weights.zip/file) & extract them to the weights directory:

```bash
# wget https://www.mediafire.com/file/7n4b2e1geeuzu69/weights.zip/file -O weights.zip
unzip weights.zip -d ./weights
```

### 6. Create and Activate Virtual Environment

Create and activate the virtual environment:

```bash
python -m venv env
source env/bin/activate
```

### 7. Install Python Torch Dependencies

Install CUDA/GPU version of [Python torch](https://pytorch.org/get-started/locally/) dependencies (check & replace link-version below with your CUDA version, e.g: v12.1 = 121):

```bash
python -m pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```

### 8. Install Requirements

Install project requirements:

```bash
pip install -r packages.txt
```

### 9. Run the Application

Run the app.py file,
(make sure to adjust the params in the config.py file):

```bash
python app.py
```

### 10. Clone Frontend Repository

clone the frontend repository & move into the directory:

```bash
cd ../
git clone https://github.com/jesvijonathan/Snitch-GPT-Frontend
cd Snitch-GPT-Frontend
```

### 11. Install NPM Dependencies and Build App

Install npm project dependencies and build the app:

```bash
npm install
npm run build
```

### 12. Run Frontend Application

Run the frontend application:

```bash
npm run dev
```

### 13. Open Application

Open the application in your web browser:

```bash
http://localhost:5173 # for App
http://localhost:5000 # for Legacy App
http://localhost:5000/api # for API
```

## Notes

- Use the application via API or web interface.
- Refer to the [frontend repository](https://github.com/jesvijonathan/Snitch-GPT-Frontend) for more details.
- Both the frontend and backend applications should be running simultaneously.
- Configure the parameters in the `config.py` file for better results.
- Ensure you have the recommended hardware and software requirements:
  - **GPU Mode** (recommended, significantly better performance),
    - CUDA enabled GPU,
    - 4GB+ VRAM (with all 6 models loaded, 12GB+ recommended),
  - **CPU Mode** (not recommended, although you can use it in MIX mode alongside GPU),
    - 4+ Core CPU (8+ Core CPU recommended),
    - 2.5GHz+ Clock Speed,
    - 16GB RAM (32GB+ recommended)
  - Min 40GB Storage (SSD recommended, faster swap & loading time),
  - Python 3.10.6
- Lack of memory or VRAM may cause poor performance or might crash during execution.
- Lack of storage may cause the program to crash due insufficient space for model weights or swap memory.
- Switch to sequential mode & disable models to reduce memory usage if you face memory issues.
  <br>
- This project works best with text with more than 250 characters & is trained on lengthy texts & using bert/DebertaModel along with 3M GPT-4 Data.
- Use this project along with the frontend interface intended to use with this project, which has visualization & more | [Snitch-GPT](https://snitch-gpt.vercel.app)
- Adjust the params in the config.py file best, as per need (You will have to modify the default params).
- The model is trained on a large custom dataset for the most accurate results. Results may not always be inaccurate, use at own risk.
- I know most of it is speghetti code rn, but it works. Will refactor soon. 0_0

## Features

- Detect AI-generated text/content.
- Score the content based on multiple parameters & the probability of being AI-generated.
- Model trained on a broader/large dataset for the most accurate results.
- Use of new multiple models & techniques to improve the accuracy of the model.
- Interactive Web app interface to interact with the application.
- API availability to integrate the application with other services.
- Minimal & easy to use, can save research time.
- Customizable parameters to adjust the model for better results.
- Maximum efficiency by using max hardware resources for significant performance boosts & faster results.
- Supports one shot detection & other checks.
- ~300ms execution time for optimal cases.
- many more...

## Endpoints

- <b>Legacy App Endpoint:</b>

  - http://localhost:5000/ - Home Page

- <b>WebSocket Endpoints:</b>

  - ws://localhost:5000/socket.io/ - Connect to the WebSocket
  - ws://localhost:5000/socket.io/ - Disconnect from the WebSocket
  - ws://localhost:5000/socket.io/ - Get the values from the WebSocket

- <b>Http (API) Endpoints:</b>
  - http://localhost:5000/api/ - API Home Page
  - http://localhost:5000/api/token - Get the token from the API
  - http://localhost:5000/api/remove - Remove the token from the API
  - http://localhost:5000/api/job - Get/Post Job requests
    - GET: http://localhost:5000/api/job?user_id=ef933904&text=hello%20world%20jesvi
    - POST: http://localhost:5000/api/job {"user_id": "ef933904", "text": "hello world jesvi"}
- <b>Sntich GPT App Endpoints:</b>
  - Please refer Snitch-GPT [Docs](<[www.google.com](https://github.com/jesvijonathan/Snitch-GPT-Frontend)>)

## License

- [MIT](https://choosealicense.com/licenses/mit/)

## Contributors

- [Jesvi Jonathan](jesvi22j@gmail.com)

<!--
- []()

## Acknowledgements

- [Hugging Face](https://huggingface.co/)
- [PyTorch](https://pytorch.org/)
- [DebertaModel]()
- [DebertaModelv3]()
- [SlimPajama]()
- [AI GPT-4]()
- [Kaggle]()
- [Collab]()

## Support

- [PayPal](https://www.paypal.com/paypalme/jesvijonathan)
  -->

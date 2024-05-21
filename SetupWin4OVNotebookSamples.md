## What's this?
- Instructions how to setup OpenVINO(TM) enviornment on Windows PC (Intel(r) Core Ultra)
- Goal is to run [OpenVINO(TM) Notebooks](https://github.com/openvinotoolkit/openvino_notebooks/tree/latest) sample scripts with CPU/GPU/NPU on your PC

## First to do when you get PC
- please update GPU and CPU driver
- https://www.intel.co.jp/content/www/jp/ja/products/details/processors/core-ultra/downloads.html
  - インテル® Arc™ & Iris® Xe Graphics - Windows*
  - インテル® NPU ドライバー - Windows*
- Install GIT command for Windows
  - Download and install for Win-64bit 
  - https://git-scm.com/download/win
- Also run Windows Update
  - 設定　-> アップデート＆セキュリティ -> Windows Update から更新
 
## Setup

1. Install Python
   access to Python 3.11.8. Download [Windwos 64 installer](https://www.python.org/ftp/python/3.11.8/python-3.11.8-amd64.exe) and click to open.
   Check "Add Python.exe to Path" and "Install Now"
   
   ![](python_installer.png)

2. Setup Virtual Environment
   
   Open comandline prompt (cmd.exe). You can confirm python 3.11.8 is installed with typing "python". (exit() for finshing python prompt)
   
   ```
   cd %USERPROFILE%
   python -m venv ov_env
   ov_env\Scripts\activate
   ```
   
   check your see (ov_env) on top of your command prompt line, meaning you're in ov_env virtual environment.
   to finish virtual env, type 'deactivate'

   
   ![](venv.png)

4. Download openvino_notebooks with GIT command

   ```
   cd ov_env
   git clone https://github.com/openvinotoolkit/openvino_notebooks.git
   cd openvino_notebooks
   ```

5. install required python libraries on your virtual environment.
   
   ```
   pip install -r requirements.txt
   ```

6. go to first folders and run jupyter.
   
   ```
   cd notebooks
   jupyter lab
   ```

7. Once open Jupyter Lab on your browser, move to "OpenVINO™ Runtime API Tutorial"
   click "openvino-api" folder and open "openvino-api.ipynb" on left plain.

   ![](images/notebooks1.png)
   ![](images/notebooks2.png)
   

8. Read instruction and run each cell one by one (click run button or Ctrl-Enter on each cell)
    
   ![](images/notebooks3.png)

9. Once finished, please try other tutrials, also try other samples you are interested in.
   First steps:
    - [OpenVINO™ Runtime API Tutorial](https://github.com/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/openvino-api/openvino-api.ipynb)
    - [Hello Image Classification](https://github.com/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/hello-world/hello-world.ipynb)
    - [Hello Image Segmentation](https://github.com/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/hello-segmentation/hello-segmentation.ipynb)
    - [Hello Object Detection](https://github.com/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/hello-detection/hello-detection.ipynb)

   Here are some recommendataions you'll have fun with. 
    - [Stable Diffusion](https://github.com/openvinotoolkit/openvino_notebooks/tree/latest/notebooks/stable-diffusion-v2)
    -    ![](https://github.com/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/stable-diffusion-v2/stable-diffusion-v2-infinite-zoom.gif)
    - [Riffusion (txt to music)](https://github.com/openvinotoolkit/openvino_notebooks/tree/latest/notebooks/riffusion-text-to-music)
    -    ![](https://github.com/openvinotoolkit/openvino_notebooks/blob/latest/notebooks/riffusion-text-to-music/riffusion-text-to-music.png)
    - [YoLov8](https://github.com/openvinotoolkit/openvino_notebooks/tree/latest/notebooks/yolov8-optimization)
    -    <img src="yolo_example.png" width="50%">
    - [LLM RAG](https://github.com/openvinotoolkit/openvino_notebooks/tree/latest/notebooks/llm-rag-langchain)
    -    <img src="llmrag_example.png" width="50%">


How to uninstall？
  - Just remove folders.
  - Uninstall python and git from Windows settings if necessary 

## Reference
- https://github.com/openvinotoolkit/openvino_notebooks/tree/latest

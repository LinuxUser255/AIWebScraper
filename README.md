# AI Assited Web Scraper

### Built with [Streamlit](https://streamlit.io/)  & Powered by [Ollama](https://ollama.com/)

<img width="452" alt="Screenshot 2025-01-13 at 5 18 23 PM" src="https://github.com/user-attachments/assets/9509b333-d71f-4e77-b222-c7b3297f5b55" />


![streamlit-mail-logo](https://github.com/user-attachments/assets/2bb87c8e-11e8-4236-bf85-162b099e7189)





ABOUT:

This webscraper uses the Ollama LLM to assist in web scraping.
It prompts the user to supply a URL, and a description of they want scraped from the specified website.
These instructions are then read by the LLM and parsed by the python code, and the results are returned to the user.

## First:

## You will need to download the Chrome Driver 
## and palce it in the same directory as the python files/scripts
## --> https://googlechromelabs.github.io/chrome-for-testing/#stable

<br>


## Installation and use:
**Clone the repository & Install the requirments**
```shell
pip3 install -r requirements.txt
```

**Then, in the command line, in the `/AIWebScraper` directory run:**
```shell
streamlit run main.py
```

<br>

## Quickstart

### To run and chat with [Llama 3.1](https://ollama.com/library/llama3.1):


**To pull a model do:**
```shell
ollama pull llama3.1
```

**Then run it interactively on the command line.**
```shell
ollama run llama3.1
```

**You can also use this shell script to automate selecting and pulling Ollama Models**
```shell
chmod +x install_ollama.sh
./install_ollama.sh
```


### _Before pulling a model number, keep in mind the memory constraints and limitations of your machine. Check the table below_


<br>

**_The following information is from [Ollama's GitHub](https://github.com/ollama/ollama) and is relevant to it's use in this web scraper_**

## Model library

Ollama supports a list of models available on [ollama.com/library](https://ollama.com/library 'ollama model library')

Here are some example models that can be downloaded:

| Model              | Parameters | Size  | Download                       |
| ------------------ | ---------- | ----- | ------------------------------ |
| Llama 3.1          | 8B         | 4.7GB | `ollama run llama3.1`          |
| Llama 3.1          | 70B        | 40GB  | `ollama run llama3.1:70b`      |
| Llama 3.1          | 405B       | 231GB | `ollama run llama3.1:405b`     |
| Phi 3 Mini         | 3.8B       | 2.3GB | `ollama run phi3`              |
| Phi 3 Medium       | 14B        | 7.9GB | `ollama run phi3:medium`       |
| Gemma 2            | 2B         | 1.6GB | `ollama run gemma2:2b`         |
| Gemma 2            | 9B         | 5.5GB | `ollama run gemma2`            |
| Gemma 2            | 27B        | 16GB  | `ollama run gemma2:27b`        |
| Mistral            | 7B         | 4.1GB | `ollama run mistral`           |
| Moondream 2        | 1.4B       | 829MB | `ollama run moondream`         |
| Neural Chat        | 7B         | 4.1GB | `ollama run neural-chat`       |
| Starling           | 7B         | 4.1GB | `ollama run starling-lm`       |
| Code Llama         | 7B         | 3.8GB | `ollama run codellama`         |
| Llama 2 Uncensored | 7B         | 3.8GB | `ollama run llama2-uncensored` |
| LLaVA              | 7B         | 4.5GB | `ollama run llava`             |
| Solar              | 10.7B      | 6.1GB | `ollama run solar`             |

> [!NOTE]
> You should have at least 8 GB of RAM available to run the 7B models, 16 GB to run the 13B models, and 32 GB to run the 33B models.

## Customize a model

### Import from GGUF

Ollama supports importing GGUF models in the Modelfile:

1. Create a file named `Modelfile`, with a `FROM` instruction with the local filepath to the model you want to import.

   ```
   FROM ./vicuna-33b.Q4_0.gguf
   ```

2. Create the model in Ollama

   ```
   ollama create example -f Modelfile
   ```

3. Run the model

   ```
   ollama run example
   ```

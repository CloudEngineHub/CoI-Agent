<p align="center">
    <img src="assets/logo.jpg" width="16%" height="25%">
    <img src="assets/title.png" width="55%" height="55%">
</p>

<h3 align="center">
CoI Agent: Revolutionizing Research in Novel Idea Development with LLM Agents
</h3>

<font size=3><div align='center' > [[📖 arXiv Paper](https://arxiv.org/pdf/2410.13185)] [[📊 Online Demo](https://huggingface.co/spaces/DAMO-NLP-SG/CoI_Agent)] </div></font>


<p align="center">
<a href="https://opensource.org/license/apache-2-0"><img src="https://img.shields.io/badge/Code%20License-Apache_2.0-green.svg"></a>
<a href="https://github.com/DAMO-NLP-SG"><img src="https://img.shields.io/badge/Institution-DAMO-red"></a>
<a><img src="https://img.shields.io/badge/PRs-Welcome-red"></a>
</p>


## 🔥 News
* **[2024.10.12]**  The first version of CoI Agent!


## 🛠️ Requirements and Installation
**Step 1**:
```bash
git clone https://github.com/DAMO-NLP-SG/CoI-Agent.git
cd CoI-Agent
pip install -r requirements.txt
```

**Step 2**:
Install [SciPDF Parser](https://github.com/titipata/scipdf_parser) for PDF parsing.

**Step 3**:
set config.yaml to use the LLM APIs.
```yaml
# Sementic scholor api, it should be filled
SEMENTIC_SEARCH_API_KEY: ""

AZURE_OPENAI_ENDPOINT : ""
AZURE_OPENAI_KEY : ""
AZURE_OPENAI_API_VERSION : ""

OPENAI_API_KEY: ""
OPENAI_BASE_URL: ""

# if not set it will be set to the same as main llm
EMBEDDING_API_KEY: ""
EMBEDDING_API_ENDPOINT: ""
EMBEDDING_MODEL: ""

MAIN_LLM_MODEL: "" # "gpt-4o" or ...

CHEAP_LLM_MODEL: "" # "gpt-4o" or ...
```

## 🚀 Quick Start
**Step 1**:
**Run grobid**
If you git clone https://github.com/titipata/scipdf_parser.git
```bash
cd scipdf_parser
bash serve_grobid.sh
```

elif you download the grobid
```bash
cd grobid
./gradlew run
```

**Step 2**:
```python
python main.py --topic {your research topic}
```


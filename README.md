# Ask my PDF



Thank you for your interest in my application. Please be aware that this is only a **Proof of Concept system** and may contain bugs or unfinished features.



### Ask my PDF - Question answering system built on top of GPT3



🎲 The primary use case for this app is to assist users in answering  questions about board game rules based on the instruction manual. While  the app can be used for other tasks, helping users with board game rules is particularly meaningful to me since I'm an avid fan of board games  myself. Additionally, this use case is relatively harmless, even in  cases where the model may experience hallucinations.



📄 The app implements the following academic papers:

- [In-Context Retrieval-Augmented Language Models](https://arxiv.org/abs/2302.00083) aka **RALM**

- [Precise Zero-Shot Dense Retrieval without Relevance Labels](https://arxiv.org/abs/2212.10496) aka **HyDE** (Hypothetical Document Embeddings)



### Installation



1. Clone the repo:

   `git clone https://github.com/catlover75926/pdf-ask-system`

2. Install dependencies:

   `pip install -r ask-my-pdf/requirements.txt`

3. Run the app:

   `cd ask-my-pdf/src`
   
   `run.sh` or `run.bat`



### High-level documentation



#### RALM + HyDE

![RALM + HyDE](docs/ralm_hyde.jpg)



#### RALM + HyDE + context

![RALM + HyDE + context](docs/ralm_hyde_wc.jpg)



### Environment variables used for configuration



##### General configuration:

- **STORAGE_SALT** - cryptograpic salt used when deriving user/folder name and encryption key from API key, hexadecimal notation, 2-16 characters

- **STORAGE_MODE** - index storage mode:  S3, LOCAL, DICT (default)

- **STATS_MODE** - usage stats storage mode: REDIS, DICT (default)

- **FEEDBACK_MODE** - user feedback storage mode: REDIS, NONE (default)

- **CACHE_MODE** - embeddings cache mode: S3, DISK, NONE (default)

  

##### Local filesystem configuration (storage / cache):

- **STORAGE_PATH** - directory path for index storage

- **CACHE_PATH** - directory path for embeddings cache

  

##### S3 configuration (storage / cache):

- **S3_REGION** - region code

- **S3_BUCKET** - bucket name (storage)

- **S3_SECRET** - secret key

- **S3_KEY** - access key

- **S3_URL** - URL

- **S3_PREFIX** - object name prefix

- **S3_CACHE_BUCKET** - bucket name (cache)

- **S3_CACHE_PREFIX** - object name prefix (cache)

  

##### Community version related options:

- **OPENAI_KEY** - API key used for the default user
- **COMMUNITY_DAILY_USD** - default user's daily budget
- **COMMUNITY_USER** - default user's code

### Contact US
If there are some problems associated with this project, please contact us: titanrtx0714@gmail.com

# assistant-streamlit-starter

This is a template repository for creating a [Streamlit](https://streamlit.io/) app to interact with PDF and text files with natural language. Content is processed and queried against with [Pinecone Assistant](https://www.pinecone.io/blog/pinecone-assistant/).

## Configuration

### Install packages

1. For best results, create a [Python virtual environment](https://realpython.com/python-virtual-environments-a-primer/) with 3.10 or 3.11 and reuse it when running any file in this repo.
2. Run

```shell
pip install -r requirements.txt
```

### Environment Variables

Copy `.env.template` to `.env` and `.streamlit/secrets.toml.template` to `.streamlit/secrets.toml`. Fill in your [Pinecone API key](https://app.pinecone.io/organizations/-/projects/-/keys) and the name you want to call your Assistant. The `.env` file will be used by the Jupyter notebook for processing the data and upserting it to Pinecone, whereas `secrets.toml` will be used by Streamlit when running locally.

## Setup Assistant

1. In the [console](https://app.pinecone.io/organizations/-/projects/-/assistant), accept the Terms of Service for Pinecone Assistant.

2. Run all cells in the "assistant-starter" Jupyter notebook to create an assistant and upload files to it.
   > [!Note] If you prefer to create an assistant and upload your files via the UI, skip the notebook and continue to the next section.

## Test the app locally

### [OPTIONAL] Configure the app

In the `streamlit_app.py` file:

- Set your preferred title on [line 18](https://github.com/pinecone-field/assistant-streamlit-starter/blob/f5091cbe5a9bb0fc31f327cda47830824d7a168b/streamlit_app.py#L18)
- Set your preferred prompt on [line 21](https://github.com/pinecone-field/assistant-streamlit-starter/blob/f5091cbe5a9bb0fc31f327cda47830824d7a168b/streamlit_app.py#L21)
- Set your preferred button label on [line 24](https://github.com/pinecone-field/assistant-streamlit-starter/blob/f5091cbe5a9bb0fc31f327cda47830824d7a168b/streamlit_app.py#L24)
- Set your preferred success message on [line 49](https://github.com/pinecone-field/assistant-streamlit-starter/blob/f5091cbe5a9bb0fc31f327cda47830824d7a168b/streamlit_app.py#L49)
- Set your preferred failure message on [line 53](https://github.com/pinecone-field/assistant-streamlit-starter/blob/f5091cbe5a9bb0fc31f327cda47830824d7a168b/streamlit_app.py#L53)
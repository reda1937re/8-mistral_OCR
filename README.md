# 8-mistral_OCR

"Legal Copilot" — app Streamlit d'OCR et Q&A sur des PDF juridiques. Le PDF uploadé est envoyé à l'OCR de Mistral (`mistral-ocr-latest`) pour en extraire le markdown ; l'app génère ensuite un résumé via le modèle de chat Mistral, ou répond à des questions libres via un pipeline RAG simple (découpage du texte, embeddings via `mistral-embed`, recherche FAISS, réponse via `mistral-large-latest`).

## Tech stack

streamlit, mistralai, faiss, numpy, chardet, python-dotenv

## Lancer le projet

```bash
pip install -r requirements.txt
```

Créer un `.env` avec `MISTRAL_API_KEY=...`

```bash
streamlit run app.py
```

# Car Review Analysis with Pre-trained LLMs  
As part of a pilot project for **Car-ing is Sharing**, I applied **pre-trained Large Language Models (LLMs)** to solve diverse NLP tasks over customer car reviews. The tasks spanned sentiment classification, machine translation, extractive QA, and summarization.

---

## Process & Findings

### 1. Sentiment Classification
- **Task**: Classify 5 car reviews into positive/negative sentiment.  
- **Model Used**: `distilbert-base-uncased-finetuned-sst-2-english`  
- **Predicted Labels**:  `["POSITIVE", "POSITIVE", "POSITIVE", "NEGATIVE", "POSITIVE"]`
- - **Binary Predictions**: `[1, 1, 1, 0, 1]`  
- **Results**:  
- Accuracy: **0.80**  
- F1 Score: **0.857**  

*Insight*: The model correctly captured most customer sentiments, though one misclassification impacted accuracy.

---

### 2. Translation (EN → ES)
- **Task**: Translate the first two sentences of the first review into Spanish.  
- **Model Used**: `Helsinki-NLP/opus-mt-en-es`  
- **Generated Translation**:  
> *"Estoy muy satisfecho con mi Nissan NV SL 2014. Uso esta camioneta para mis entregas de negocios y uso personal."*

- **Reference Translations** (from file):​:contentReference[oaicite:0]{index=0}  
- **BLEU Score**: **68.88**

*Insight*: The translation was fluent and aligned well with provided references, yielding a strong BLEU score.

---

### 3. Extractive Question Answering
- **Context**: Second review (customer described both positives and negatives).  
- **Question**: *“What did he like about the brand?”*  
- **Answer Extracted**:  
> **"ride quality, reliability"**

*Insight*: The QA model successfully pinpointed the brand aspects valued by the customer despite broader negative context.

---

### 4. Summarization
- **Task**: Summarize the last review into ~50–55 tokens.  
- **Model Used**: `sshleifer/distilbart-cnn-12-6`  
- **Summarized Text**:  
> *"Nissan Rogue provides the desired SUV experience without burdening me with an exorbitant payment. Handling and styling are great; I have hauled 12 bags of mulch in the back with the seats down and could have held more. The engine delivers strong performance, and the ride is really smooth."*

*Insight*: The summary is concise, preserving key details on affordability, performance, and comfort.

---

## Conclusion
Through the use of pre-trained LLMs, I demonstrated that **Car-ing is Sharing** can efficiently:  
- Automate **sentiment insights** from customer reviews,  
- Provide **multilingual support** with quality translations,  
- Enable **question answering** to assist agents,  
- Deliver **summaries** for quick review analysis.  

This pilot validates the potential of LLMs to enhance customer support and internal efficiency.

---

*Report by Nayab Irfan — AI Engineer*

# Repository Structure – GenderSte Survey Project
L'articolo in formato pdf, "Un dataset italiano per l'analisi degli stereotipi di genere nei testi mediante Large Language Model", contiene una spiegazione dettagliata di quanto svolto nell'analisi e il background teorico necessario per la compresione dell'analisi.

## Materiale per la creazione della survey
- **Zip `GenderSte_Survey`**  
  Contiene tutto il materiale utilizzato per la creazione della survey su PsyToolkit, tra cui:
  - file di testo delle sub-survey  
  - dataset di estratti testuali (.xlsx e .txt)  
  - script Python per la composizione automatica della survey  
  - output finale pronto per PsyToolkit  
---
## `AnalisiGenderSte_Persone`

- **Zip `PsyToolkitData_GenderSteSurvey_2026_02_11_08_55`**  
  Contiene i risultati del questionario svolto su PsyToolkit.
- **`Analisi-Gender_Ste-Survey`**
  Contiene un pdf con l'analisi dei dati raccolti nel questionario rivolto alle persone
---
## `AnalisiChatBot`

- **`gender_survey.pipeline.py`**
  Contiene lo script python utilizzato per interrogare i vari chatbot
- **`deepseek-chat`**  
  Contiene un pdf con l'analisi relativa ai dati raccolti nelle chiamate a deepseek e nella cartella 'data' i file delle varie run fatte con deepseek
- **`gemini-2.5-flash`**  
  Contiene un pdf con l'analisi relativa ai dati raccolti nelle chiamate a gemini e nella cartella 'data' i file delle varie run fatte con gemini
- **`gpt4.1-mini`**  
Contiene un pdf con l'analisi relativa ai dati raccolti nelle chiamate a gpt e nella cartella 'data' i file delle varie run fatte con gemini

---

## Analisi statistiche di confronto Umani vs Modelli

Le quattro zip seguenti contengono le analisi statistiche di confronto tra le valutazioni umane e quelle prodotte dai tre LLM (GPT-4.1-mini, Gemini-2.5-flash, DeepSeek-chat) sulle 111 sezioni testuali del dataset. Ogni cartella include lo script Quarto (`.qmd`), l'output compilato (`.pdf` e/o `.html` con relative figure) e i dataset CSV (`deepseek_wide_111.csv`, `gemini_wide_111.csv`, `gpt_wide_111.csv`, `human_wide_raw.csv`) usati come input.

- **Zip `Spearman`**
  Correlazione di Spearman tra i gender score assegnati dai valutatori umani e quelli prodotti dai tre modelli, scelta per la natura ordinale discreta della scala di valutazione (−2, −1, 0, +1, +2) e la robustezza rispetto a valori estremi. Include anche i file `risultati_spearman.csv` e `risultati_scores_unificati.csv` con i risultati numerici.

- **Zip `Paired_T-test_Bland-Altman`**
  Confronto tra i giudizi umani e quelli dei modelli AI tramite paired t-test e diagrammi di Bland–Altman, per valutare sia le differenze medie sia l'accordo/bias sistematico tra le valutazioni.

- **Zip `IRR`**
  Analisi dell'accordo inter-rater (IRR) tramite Alpha di Krippendorff (metodo ordinale), calcolata separatamente per i valutatori umani (accordo tra partecipanti) e per ciascun modello (stabilità tra le 5 run a diverse temperature: T=0, T=0.3×2, T=0.5×2), sia a livello globale che per categoria testuale (F, M, N).

- **Zip `Polarizzazione_ed_entropia`**
  Analisi della polarizzazione e dell'entropia dei giudizi (umani vs DeepSeek, Gemini, GPT) calcolate sui singoli rating (non sulle medie) lungo la scala a cinque categorie (−2, −1, 0, 1, 2).









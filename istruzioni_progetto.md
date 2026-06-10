## Obiettivo del Progetto
L'obiettivo del progetto consiste nel valutare la robustezza di modelli di Machine Learning a fronte di un decadimento della qualità dei dati. Il fulcro dell'analisi è identificare le feature più significative e osservare come la loro alterazione ("sporco") influenzi le prestazioni finali di classificazione.

## Fasi del Lavoro

### 1. Scelta del Dataset
* Selezionare un dataset adeguato al problema (non troppo piccolo e con un buon numero di feature).
* Il dataset dovrebbe contenere un mix di variabili numeriche e categoriche per un'analisi più ricca.

### 2. Esplorazione dei Dati (EDA)
Eseguire un'analisi esplorativa completa per comprendere:
* La distribuzione delle feature.
* La presenza di valori mancanti.
* La correlazione tra le variabili.
* Identificazione preliminare delle feature potenzialmente più importanti.

### 3. Preparazione dei Dati e Feature Extraction
Preparare il dataset per l'addestramento:
* Gestione dei valori mancanti.
* Codifica delle variabili categoriche (Encoding).
* Normalizzazione o standardizzazione delle feature.
* **Feature Extraction:** identificare le feature più importanti. Questo passaggio è fondamentale per decidere, in seguito, quali colonne "sporcare" per testare il modello.

### 4. Scelta e Addestramento del Modello (Baseline)
* **Modelli:** Selezionare almeno **2 modelli** di machine learning adatti al problema (es. Random Forest, Logistic Regression, SVM, ecc.).
* **Baseline Model:** Addestrare i modelli sul dataset originale "pulito". I risultati ottenuti fungeranno da riferimento (baseline) per le valutazioni successive.

### 5. Degradazione del Dataset (Data Dirtying)
Applicare diverse tecniche per "sporcare" il dataset in modo controllato:
* Aggiunta di rumore ai dati.
* Rimozione casuale di feature.
* Sostituzione di valori con dati casuali.
* Duplicazione dei dati o introduzione di outlier.
* *Nota:* È possibile utilizzare librerie specifiche o funzioni custom per sporcare i dati con errori diversi e percentuali crescenti.
* **Logica di analisi:** Decidere quali feature sporcare (priorità a quelle importanti) in base ai risultati della fase 3.

### 6. Valutazione delle Prestazioni
Valutare i modelli sul dataset "sporco" misurando le metriche rilevanti:
* Accuracy
* Precision
* Recall
* F1-score

### 7. Confronto e Interpretazione dei Risultati
* **Confronto:** Analizzare le differenze di performance tra il Baseline Model e i modelli testati sui dati corrotti.
* **Interpretazione:** Spiegare il comportamento dei modelli. Quali feature hanno avuto il maggior impatto quando alterate? Quale modello si è dimostrato più robusto?

### 8. Riflessioni e Conclusioni
* Discutere l'efficacia delle tecniche di "sporco" nell'evidenziare l'importanza delle feature.
* Fornire suggerimenti per eventuali passi futuri o miglioramenti del processo di gestione della Data Quality.
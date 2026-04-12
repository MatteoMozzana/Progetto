# F1 Tyre Degradation Predictor 

## Descrizione
Progetto per il laboratorio di Python che analizza i dati telemetrici del Gran Premio d'Italia 2024 (Monza) per studiare il degrado degli pneumatici in Formula 1 attraverso tecniche di Machine Learning.

## Obiettivo
Costruire un modello predittivo capace di classificare i giri in base al livello di degrado degli pneumatici, analizzando variabili come l'età della gomma, il numero del giro e lo stint.

## Dataset
Dati estratti tramite la libreria **FastF1** — API ufficiale che fornisce telemetria, tempi sul giro e dati sugli pneumatici direttamente dalle sessioni di Formula 1.
- **Gran Premio:** Italia 2024 — Monza
- **Sessione:** Gara
- **Piloti analizzati:** Leclerc, Sainz, Verstappen

## Fasi del progetto
### 1. EDA (Exploratory Data Analysis)
- Esplorazione del dataset: 1008 giri, 31 variabili
- Analisi dell'andamento dei tempi sul giro per pilota e per stint
- Confronto delle mescole tramite boxplot
- Analisi della correlazione tra variabili

### 2. Addestramento del modello
- Definizione del target: degrado alto (1) o basso (0) rispetto alla mediana dello stint
- Feature utilizzate: TyreLife, LapNumber, Stint
- Modello: Decision Tree Classifier (max_depth=4)
- Accuracy ottenuta: 61%

## Risultati
Il modello raggiunge una accuracy del 61% con sole 3 feature. L'analisi ha evidenziato come il degrado degli pneumatici non possa essere studiato sull'intera gara, ma debba essere analizzato stint per stint per isolare l'effetto del consumo di carburante.

## Librerie utilizzate
- `fastf1` — accesso ai dati telemetrici F1
- `pandas` — manipolazione dei dati
- `numpy` — calcoli numerici
- `matplotlib` / `seaborn` — visualizzazione
- `scikit-learn` — Machine Learning

## Autore
Matteo Mozzana
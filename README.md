# Historical Parapsychology Data Parser
### Automated Semantic Data Extraction on Legacy Literature

A self-directed Python pipeline designed to ingest unstructured, 19th-century textual accounts of anomalous phenomena and normalize them into structured database matrices for statistical analysis. This project serves as a proof-of-concept for automating archive digitization workflows within parapsychological and historical text corpora.

## Project Architecture
*   **Ingestion & Memory Layer:** Processes raw text file transcriptions parsed out of legacy literature (tested using *Phantasms of the Living*, 1886).
*   **Rule-Based Regex Engine:** Implements a deterministic local rule processing sequence via Python's built-in `re` module to cleanly extract structural variables case-insensitively without API walls, external dependencies, or cost constraints.
*   **Tabular Normalization:** Compiles multi-line qualitative narratives into quantitative columns via `pandas` DataFrames, converting prose into queryable analytical assets.

## Extracted Data Matrix Fields
Every isolated narrative report is automatically audited and mapped across the following structural variables:
*   `case_number`: The specific historical identifier or letter index found in the text structure.
*   `year_of_event`: 4-digit chronological anchor extraction mapping when the phenomenon occurred.
*   `phenomenon_category`: Categorical grouping tracking the nature of the claim (e.g., Apparitions, Physical/Environmental Anomalies).
*   `witness_state_of_consciousness`: Behavioral conditions of the subject at the time of the event (e.g., Awake, Asleep/Bed, Unknown).
*   `environmental_triggers_reported`: Array lists capturing ambient metadata triggers reported during the sequence (e.g., Cold spots, extreme weather anomalies, nighttime).
*   `veridical_coincidence`: A boolean evaluating chronological alignment with real-world external logs (e.g., corresponding deaths or accidents).
*   `skeptical_or_rational_counter_notes`: Tracks explicit witness exclusions regarding typical physiological explanations like sleep paralysis or intoxication.

## Repository Contents
*   `anomalous_data_parser.ipynb`: The complete executable Jupyter data science workbook containing environment setup, ingestion scripts, tokenization filters, and tabular formatting loops.
*   `final_manually_parsed_archive.csv`: The clean target dataset generated dynamically from 43 isolated historical text files extracted from the corpus.

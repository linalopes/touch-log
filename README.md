# Touch Log: Self-Tracking Human Touch, Care, and Hugs

This touch log is a small autoethnographic data collection experiment created as a warm-up for the broader research on hugs, affective touch, and machine-readable intimacy. The goal is to observe how touch appears in everyday life: not only as explicit hugs, but also as care, holding, functional contact, social greetings, playful gestures, and moments that are difficult to classify.

The data is collected through two Google Forms. **Form A** is a quick event-based log designed to be filled on the phone immediately after, or shortly after, a touch event. It records timestamp, delay, person/category, type of contact, intention, duration, optional note, and location. **Form B** is a daily reflection form, used to capture what was memorable, missed, ambiguous, or difficult to log in the moment.

Data spreadsheet: [Touch Log — Google Sheets](https://docs.google.com/spreadsheets/d/1SH7GUCg6qTbpDvbtOAxIxynKs4mnKyKOZjeSKJsWaBk/edit?gid=714232102#gid=714232102)

The spreadsheet currently contains three layers:

- **Form A / Touch Log**
  - Raw logged events, mostly captured close to the moment they happened.
  - Useful for quantitative patterns such as frequency, contact type, duration, person/category, and location.

- **Form B / Daily Touch Reflection**
  - Qualitative reflection written after the day.
  - Useful for recovering social events, missed touches, affective memories, and moments that did not fit neatly into the form.

- **Inferred Touch Events**
  - Reconstructed touch events inferred from Form B.
  - These entries keep the same core fields as Form A, but include metadata such as `data_source`, `confidence`, `source_reflection_date`, `inferred_person_name`, and `methodological_note`.
  - This allows inferred events to be visualized together with the raw log, while still preserving their reconstructed status.

Early observations:

- Touch with **Uma** appears mostly through care, holding, calming, and long-duration bodily presence. This suggests that touch with a baby is less an isolated event and more a sustained bodily condition.

- Touch with a **partner** appears across affection, play, goodbye gestures, sex, massage, holding hands, and domestic intimacy. This category shows a wide range of duration and intention.

- **Social events** are difficult to log in real time. Many greetings and goodbyes are only recovered later through reflection, which suggests that social touch often appears as a cluster rather than as a single memorable event.

- Some touches are not easily captured as “hug” or “touch.” Examples include functional touch while making or fixing something, touch as part of the Maze Circuit workshop, and residual forms of touch such as perfume left on Uma’s head after being held by someone else.

- The act of logging touch also changes the social situation. Once others become aware of the dataset, they may start joking with it, performing for it, or “messing with the data.” This makes the dataset itself part of the touch ecology.

This experiment is not only a dataset of touch events. It is also a record of what can be logged, what is forgotten, what is reconstructed, and what escapes classification. It may become useful for thinking about the limits of a future “Human Touch Archive”: a machine may detect duration, category, frequency, and gesture, but the meaning of touch often appears in memory, context, ambiguity, and afterthought.

Published CSV (used by the notebook):

https://docs.google.com/spreadsheets/d/e/2PACX-1vSJ2_L5hKxn8GjWzoNhpr0y2Dw14yRye52tePIUut46C44L0HTFvHHKk2xgDeAyqly_cfpyqe3jrCmu/pub?gid=714232102&single=true&output=csv

---

## Repository contents

| File | Description |
|------|-------------|
| `touch_log_EDA.ipynb` | Exploratory data analysis notebook |
| `eda_01_distributions.png` | Distributions of contact type, person, duration, and location |
| `eda_02_intentions.png` | Intention breakdown by person |
| `eda_03_daily_timeline.png` | Daily event timeline |
| `eda_04_circadian.png` | Circadian rhythm of touch events |
| `eda_05_person_x_type.png` | Person × contact type heatmap |
| `eda_06_crosstabs.png` | Cross-tabulation panels |
| `eda_07_formA_vs_inferred.png` | Form A vs inferred events comparison |

---

## How to run the analysis

### 1. Clone the repository

```bash
git clone https://github.com/linalopes/touch-log.git
cd touch-log
```

### 2. Create a virtual environment (recommended)

```bash
python3 -m venv .venv
source .venv/bin/activate   # macOS / Linux
# .venv\Scripts\activate    # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch the notebook

```bash
jupyter notebook touch_log_EDA.ipynb
```

Or open `touch_log_EDA.ipynb` directly in VS Code, Cursor, or JupyterLab.

### 5. Run all cells

The notebook reads data live from the published Google Sheets CSV — no local data files are required. Running all cells will:

1. Load and clean Form A and inferred events
2. Print summary statistics
3. Regenerate the seven chart PNGs in the repository root

Internet access is required on the first data-loading step.

---

## Notebook structure

1. Setup & data loading
2. Data cleaning & feature engineering
3. Overview stats
4. Distribution analyses
5. Timeline & circadian rhythm
6. Cross-tabulations
7. Form A vs inferred events
8. Highlights & observations

---

*Human Touch Archive · School of Tomorrow's AI · Autoethnographic dataset · May 21 – Jun 2, 2026*

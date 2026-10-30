# Artifact for Paper I (anonymised)

Regenerate every result, number and figure of the paper:

```bash
pip install -r requirements.txt
bash paperI/experiments/run_all.sh          # writes paperI/results/*.csv and manuscript/numbers.tex
cd paperI/manuscript && latexmk -pdf main.tex
```

E1 and E5 need the public corpus (`python3 data/fetch_kaggle.py --copy`); without it they print
SKIPPED and the literature fallbacks recorded in `paperI/results/provenance_paperI.csv` are used.
Every CSV carries a `provenance` column (measured, derived, assumption).

# Final Corpus — Results

> Auto-generated. Re-run `final_results.ipynb` to refresh.

## raw-corpus

### Prompt V5

```
Clasifica cada tweet como POSITIVE o NEGATIVE aplicando esta jerarquía de reglas:

1. Si el autor afirma explícitamente que consume, ha consumido o desea consumir drogas ilícitas, y lo expresa de manera neutral o positiva → POSITIVE.
2. Si el autor menciona consumo propio pero con desaprobación, crítica o rechazo → NEGATIVE.
3. Si describe consumo de otra persona, real o ficticia → NEGATIVE.
4. Si es ambiguo y puede interpretarse de forma no problemática → NEGATIVE.
5. Si menciona drogas ilícitas en contextos humorísticos, ficticios, metafóricos o musicales, sin expresar deseo o nostalgia propia → NEGATIVE.
6. Si menciona "tomar una línea" en contexto de transporte público → NEGATIVE.

Definiciones:
- "Neutral o positiva" significa que el autor no expresa desaprobación o condena.
- "Nostalgia" implica recordar consumo pasado con añoranza o valoración positiva.
```

| Model | Confusion Matrix | Classification Report | Wrong / Total |
|-------|-----------------|----------------------|--------------|
| gpt-5.4-mini | <table><tr><th></th><th>Pred NEG</th><th>Pred POS</th></tr><tr><th>True NEG</th><td>199</td><td>26</td></tr><tr><th>True POS</th><td>95</td><td>130</td></tr></table> | <table><tr><th>Label</th><th>Prec</th><th>Recall</th><th>F1</th></tr><tr><td>POSITIVE</td><td>0.83</td><td>0.58</td><td>0.68</td></tr><tr><td>NEGATIVE</td><td>0.68</td><td>0.88</td><td>0.77</td></tr><tr><td><b>Accuracy</b></td><td colspan='3'>0.73</td></tr></table> | 121 / 450 [CSV](/data/processed/final-corpus/raw-corpus/wct_gpt-5.4-mini-v5.csv) |

### Summary

<img src="media/results/final-corpus/classification-report-raw-corpus.png" alt="Classification report — raw-corpus" />

<img src="media/results/final-corpus/error-counts-raw-corpus.png" alt="Error counts — raw-corpus" />

---

## pre-filtered-corpus

### Prompt V5

```
Clasifica cada tweet como POSITIVE o NEGATIVE aplicando esta jerarquía de reglas:

1. Si el autor afirma explícitamente que consume, ha consumido o desea consumir drogas ilícitas, y lo expresa de manera neutral o positiva → POSITIVE.
2. Si el autor menciona consumo propio pero con desaprobación, crítica o rechazo → NEGATIVE.
3. Si describe consumo de otra persona, real o ficticia → NEGATIVE.
4. Si es ambiguo y puede interpretarse de forma no problemática → NEGATIVE.
5. Si menciona drogas ilícitas en contextos humorísticos, ficticios, metafóricos o musicales, sin expresar deseo o nostalgia propia → NEGATIVE.
6. Si menciona "tomar una línea" en contexto de transporte público → NEGATIVE.

Definiciones:
- "Neutral o positiva" significa que el autor no expresa desaprobación o condena.
- "Nostalgia" implica recordar consumo pasado con añoranza o valoración positiva.
```

| Model | Confusion Matrix | Classification Report | Wrong / Total |
|-------|-----------------|----------------------|--------------|
| gpt-5.4-mini | <table><tr><th></th><th>Pred NEG</th><th>Pred POS</th></tr><tr><th>True NEG</th><td>196</td><td>29</td></tr><tr><th>True POS</th><td>75</td><td>150</td></tr></table> | <table><tr><th>Label</th><th>Prec</th><th>Recall</th><th>F1</th></tr><tr><td>POSITIVE</td><td>0.84</td><td>0.67</td><td>0.74</td></tr><tr><td>NEGATIVE</td><td>0.72</td><td>0.87</td><td>0.79</td></tr><tr><td><b>Accuracy</b></td><td colspan='3'>0.77</td></tr></table> | 104 / 450 [CSV](/data/processed/final-corpus/pre-filtered-corpus/wct_gpt-5.4-mini-v5.csv) |

### Summary

<img src="media/results/final-corpus/classification-report-pre-filtered-corpus.png" alt="Classification report — pre-filtered-corpus" />

<img src="media/results/final-corpus/error-counts-pre-filtered-corpus.png" alt="Error counts — pre-filtered-corpus" />

---


# Final Corpus — Results

> Auto-generated. Re-run `final_results.ipynb` to refresh.

## raw-corpus

### Prompt V1

```
Clasifica cada tweet como POSITIVE o NEGATIVE según estos criterios:

POSITIVE: cumple con uno o más de los siguientes:
- El usuario del tweet habla de cómo o qué tipo de droga ilícita está consumiendo.
- El usuario del tweet expresa la necesidad de consumir drogas ilícitas, ya sea por abstinencia o por gusto.
- El usuario añora consumir drogas ilícitas.

NEGATIVE: no cumple con ningún criterio POSITIVE, por ejemplo:
- Habla sobre noticias o información general sobre drogas ilícitas.
- Menciona drogas ilícitas sin relación con consumo problemático o necesidad.
- Expresa ironía o sarcasmo relacionado con drogas ilícitas.
```

| Model | Confusion Matrix | Classification Report | Wrong / Total |
|-------|-----------------|----------------------|--------------|
| gpt-5.4-mini | <table><tr><th></th><th>Pred NEG</th><th>Pred POS</th></tr><tr><th>True NEG</th><td>156</td><td>69</td></tr><tr><th>True POS</th><td>25</td><td>200</td></tr></table> | <table><tr><th>Label</th><th>Prec</th><th>Recall</th><th>F1</th></tr><tr><td>POSITIVE</td><td>0.74</td><td>0.89</td><td>0.81</td></tr><tr><td>NEGATIVE</td><td>0.86</td><td>0.69</td><td>0.77</td></tr><tr><td><b>Accuracy</b></td><td colspan='3'>0.79</td></tr></table> | 94 / 450 [CSV](/data/processed/final-corpus/raw-corpus/wct_gpt-5.4-mini-v1.csv) |

### Prompt V2

```
Clasifica cada tweet como POSITIVE o NEGATIVE según estos criterios:

POSITIVE: cumple con uno o más de los siguientes:
- El usuario del tweet habla de cómo o qué tipo de droga ilícita está consumiendo.
- El usuario del tweet expresa la necesidad de consumir drogas ilícitas, ya sea por abstinencia o por gusto.
- El usuario añora consumir drogas ilícitas.

NEGATIVE: no cumple con ningún criterio POSITIVE, por ejemplo:
- Habla sobre noticias o información general sobre drogas ilícitas.
- Menciona drogas ilícitas sin relación con consumo problemático o necesidad.
- Expresa ironía o sarcasmo relacionado con drogas ilícitas.

Tener en cuenta los siguientes aspectos:
- En el tweet puede estar presente la ironía o sarcasmo.
- El análisis se centra en el autor del tweet.
- Algunos tweets mencionan tomar una línea de colectivo, subte o tren, pero solamente esto no es condición suficiente para interpretarlo como una referencia al consumo de drogas ilícitas.
```

| Model | Confusion Matrix | Classification Report | Wrong / Total |
|-------|-----------------|----------------------|--------------|
| gpt-5.4-mini | <table><tr><th></th><th>Pred NEG</th><th>Pred POS</th></tr><tr><th>True NEG</th><td>183</td><td>42</td></tr><tr><th>True POS</th><td>31</td><td>194</td></tr></table> | <table><tr><th>Label</th><th>Prec</th><th>Recall</th><th>F1</th></tr><tr><td>POSITIVE</td><td>0.82</td><td>0.86</td><td>0.84</td></tr><tr><td>NEGATIVE</td><td>0.86</td><td>0.81</td><td>0.83</td></tr><tr><td><b>Accuracy</b></td><td colspan='3'>0.84</td></tr></table> | 73 / 450 [CSV](/data/processed/final-corpus/raw-corpus/wct_gpt-5.4-mini-v2.csv) |

### Prompt V3

```
Clasifica cada tweet como POSITIVE o NEGATIVE según estos criterios:

POSITIVE: cumple con uno o más de los siguientes:
- El autor describe que está consumiendo o ha consumido drogas ilícitas, y lo presenta de forma neutral o positiva.
- El autor expresa deseo, necesidad o anhelo de consumir drogas ilícitas.
- El autor manifiesta nostalgia por experiencias pasadas de consumo de drogas ilícitas.

NEGATIVE: no cumple con ningún criterio POSITIVE, por ejemplo:
- El autor menciona consumo propio pero lo critica o desaprueba.
- Describe consumo de otra persona (real o ficticia).
- Usa humor, ironía o sarcasmo sin implicar deseo o nostalgia real de consumo propio.
- Menciona drogas ilícitas en contextos informativos, ficticios o metafóricos.
- Habla de transporte público (colectivo, subte, tren) sin relación clara con drogas ilícitas.

Consideraciones:
- El foco está en consumo problemático del autor, no solo en cualquier mención de consumo.
- Ante ambigüedad, clasificar como NEGATIVE.
```

| Model | Confusion Matrix | Classification Report | Wrong / Total |
|-------|-----------------|----------------------|--------------|
| gpt-5.4-mini | <table><tr><th></th><th>Pred NEG</th><th>Pred POS</th></tr><tr><th>True NEG</th><td>194</td><td>31</td></tr><tr><th>True POS</th><td>57</td><td>168</td></tr></table> | <table><tr><th>Label</th><th>Prec</th><th>Recall</th><th>F1</th></tr><tr><td>POSITIVE</td><td>0.84</td><td>0.75</td><td>0.79</td></tr><tr><td>NEGATIVE</td><td>0.77</td><td>0.86</td><td>0.82</td></tr><tr><td><b>Accuracy</b></td><td colspan='3'>0.80</td></tr></table> | 88 / 450 [CSV](/data/processed/final-corpus/raw-corpus/wct_gpt-5.4-mini-v3.csv) |

### Prompt V4

```
Clasifica cada tweet como POSITIVE o NEGATIVE según estos criterios:

POSITIVE: cumple con uno o más de los siguientes:
- El autor indica explícitamente que consume o ha consumido drogas ilícitas y lo describe de forma neutral o positiva.
- El autor expresa deseo, necesidad o anhelo de consumir drogas ilícitas.
- El autor manifiesta nostalgia por consumo pasado, sin desaprobarlo.

NEGATIVE: no cumple con ningún criterio POSITIVE, por ejemplo:
- El autor menciona consumo propio pero lo desaprueba, lo critica o lo presenta como algo negativo.
- Contiene citas o menciones de consumo atribuibles a otra persona.
- Usa ironía, sarcasmo o lenguaje figurado sin implicar deseo o nostalgia real de consumo propio.
- Habla de drogas ilícitas en canciones, chistes, noticias o ficción.
- Usa expresiones como "tomar una línea" para referirse a transporte público, sin evidencia clara de drogas ilícitas.

Consideraciones:
- Si hay mezcla de experiencias propias y ajenas, clasificar como POSITIVE solo si el consumo problemático propio es explícito.
- Ante ambigüedad, clasificar como NEGATIVE.
```

| Model | Confusion Matrix | Classification Report | Wrong / Total |
|-------|-----------------|----------------------|--------------|
| gpt-5.4-mini | <table><tr><th></th><th>Pred NEG</th><th>Pred POS</th></tr><tr><th>True NEG</th><td>196</td><td>29</td></tr><tr><th>True POS</th><td>47</td><td>178</td></tr></table> | <table><tr><th>Label</th><th>Prec</th><th>Recall</th><th>F1</th></tr><tr><td>POSITIVE</td><td>0.86</td><td>0.79</td><td>0.82</td></tr><tr><td>NEGATIVE</td><td>0.81</td><td>0.87</td><td>0.84</td></tr><tr><td><b>Accuracy</b></td><td colspan='3'>0.83</td></tr></table> | 76 / 450 [CSV](/data/processed/final-corpus/raw-corpus/wct_gpt-5.4-mini-v4.csv) |

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

### Prompt V1

```
Clasifica cada tweet como POSITIVE o NEGATIVE según estos criterios:

POSITIVE: cumple con uno o más de los siguientes:
- El usuario del tweet habla de cómo o qué tipo de droga ilícita está consumiendo.
- El usuario del tweet expresa la necesidad de consumir drogas ilícitas, ya sea por abstinencia o por gusto.
- El usuario añora consumir drogas ilícitas.

NEGATIVE: no cumple con ningún criterio POSITIVE, por ejemplo:
- Habla sobre noticias o información general sobre drogas ilícitas.
- Menciona drogas ilícitas sin relación con consumo problemático o necesidad.
- Expresa ironía o sarcasmo relacionado con drogas ilícitas.
```

| Model | Confusion Matrix | Classification Report | Wrong / Total |
|-------|-----------------|----------------------|--------------|
| gpt-5.4-mini | <table><tr><th></th><th>Pred NEG</th><th>Pred POS</th></tr><tr><th>True NEG</th><td>161</td><td>64</td></tr><tr><th>True POS</th><td>18</td><td>207</td></tr></table> | <table><tr><th>Label</th><th>Prec</th><th>Recall</th><th>F1</th></tr><tr><td>POSITIVE</td><td>0.76</td><td>0.92</td><td>0.83</td></tr><tr><td>NEGATIVE</td><td>0.90</td><td>0.72</td><td>0.80</td></tr><tr><td><b>Accuracy</b></td><td colspan='3'>0.82</td></tr></table> | 82 / 450 [CSV](/data/processed/final-corpus/pre-filtered-corpus/wct_gpt-5.4-mini-v1.csv) |

### Prompt V2

```
Clasifica cada tweet como POSITIVE o NEGATIVE según estos criterios:

POSITIVE: cumple con uno o más de los siguientes:
- El usuario del tweet habla de cómo o qué tipo de droga ilícita está consumiendo.
- El usuario del tweet expresa la necesidad de consumir drogas ilícitas, ya sea por abstinencia o por gusto.
- El usuario añora consumir drogas ilícitas.

NEGATIVE: no cumple con ningún criterio POSITIVE, por ejemplo:
- Habla sobre noticias o información general sobre drogas ilícitas.
- Menciona drogas ilícitas sin relación con consumo problemático o necesidad.
- Expresa ironía o sarcasmo relacionado con drogas ilícitas.

Tener en cuenta los siguientes aspectos:
- En el tweet puede estar presente la ironía o sarcasmo.
- El análisis se centra en el autor del tweet.
- Algunos tweets mencionan tomar una línea de colectivo, subte o tren, pero solamente esto no es condición suficiente para interpretarlo como una referencia al consumo de drogas ilícitas.
```

| Model | Confusion Matrix | Classification Report | Wrong / Total |
|-------|-----------------|----------------------|--------------|
| gpt-5.4-mini | <table><tr><th></th><th>Pred NEG</th><th>Pred POS</th></tr><tr><th>True NEG</th><td>175</td><td>50</td></tr><tr><th>True POS</th><td>22</td><td>203</td></tr></table> | <table><tr><th>Label</th><th>Prec</th><th>Recall</th><th>F1</th></tr><tr><td>POSITIVE</td><td>0.80</td><td>0.90</td><td>0.85</td></tr><tr><td>NEGATIVE</td><td>0.89</td><td>0.78</td><td>0.83</td></tr><tr><td><b>Accuracy</b></td><td colspan='3'>0.84</td></tr></table> | 72 / 450 [CSV](/data/processed/final-corpus/pre-filtered-corpus/wct_gpt-5.4-mini-v2.csv) |

### Prompt V3

```
Clasifica cada tweet como POSITIVE o NEGATIVE según estos criterios:

POSITIVE: cumple con uno o más de los siguientes:
- El autor describe que está consumiendo o ha consumido drogas ilícitas, y lo presenta de forma neutral o positiva.
- El autor expresa deseo, necesidad o anhelo de consumir drogas ilícitas.
- El autor manifiesta nostalgia por experiencias pasadas de consumo de drogas ilícitas.

NEGATIVE: no cumple con ningún criterio POSITIVE, por ejemplo:
- El autor menciona consumo propio pero lo critica o desaprueba.
- Describe consumo de otra persona (real o ficticia).
- Usa humor, ironía o sarcasmo sin implicar deseo o nostalgia real de consumo propio.
- Menciona drogas ilícitas en contextos informativos, ficticios o metafóricos.
- Habla de transporte público (colectivo, subte, tren) sin relación clara con drogas ilícitas.

Consideraciones:
- El foco está en consumo problemático del autor, no solo en cualquier mención de consumo.
- Ante ambigüedad, clasificar como NEGATIVE.
```

| Model | Confusion Matrix | Classification Report | Wrong / Total |
|-------|-----------------|----------------------|--------------|
| gpt-5.4-mini | <table><tr><th></th><th>Pred NEG</th><th>Pred POS</th></tr><tr><th>True NEG</th><td>210</td><td>15</td></tr><tr><th>True POS</th><td>116</td><td>109</td></tr></table> | <table><tr><th>Label</th><th>Prec</th><th>Recall</th><th>F1</th></tr><tr><td>POSITIVE</td><td>0.88</td><td>0.48</td><td>0.62</td></tr><tr><td>NEGATIVE</td><td>0.64</td><td>0.93</td><td>0.76</td></tr><tr><td><b>Accuracy</b></td><td colspan='3'>0.71</td></tr></table> | 131 / 450 [CSV](/data/processed/final-corpus/pre-filtered-corpus/wct_gpt-5.4-mini-v3.csv) |

### Prompt V4

```
Clasifica cada tweet como POSITIVE o NEGATIVE según estos criterios:

POSITIVE: cumple con uno o más de los siguientes:
- El autor indica explícitamente que consume o ha consumido drogas ilícitas y lo describe de forma neutral o positiva.
- El autor expresa deseo, necesidad o anhelo de consumir drogas ilícitas.
- El autor manifiesta nostalgia por consumo pasado, sin desaprobarlo.

NEGATIVE: no cumple con ningún criterio POSITIVE, por ejemplo:
- El autor menciona consumo propio pero lo desaprueba, lo critica o lo presenta como algo negativo.
- Contiene citas o menciones de consumo atribuibles a otra persona.
- Usa ironía, sarcasmo o lenguaje figurado sin implicar deseo o nostalgia real de consumo propio.
- Habla de drogas ilícitas en canciones, chistes, noticias o ficción.
- Usa expresiones como "tomar una línea" para referirse a transporte público, sin evidencia clara de drogas ilícitas.

Consideraciones:
- Si hay mezcla de experiencias propias y ajenas, clasificar como POSITIVE solo si el consumo problemático propio es explícito.
- Ante ambigüedad, clasificar como NEGATIVE.
```

| Model | Confusion Matrix | Classification Report | Wrong / Total |
|-------|-----------------|----------------------|--------------|
| gpt-5.4-mini | <table><tr><th></th><th>Pred NEG</th><th>Pred POS</th></tr><tr><th>True NEG</th><td>193</td><td>32</td></tr><tr><th>True POS</th><td>50</td><td>175</td></tr></table> | <table><tr><th>Label</th><th>Prec</th><th>Recall</th><th>F1</th></tr><tr><td>POSITIVE</td><td>0.85</td><td>0.78</td><td>0.81</td></tr><tr><td>NEGATIVE</td><td>0.79</td><td>0.86</td><td>0.82</td></tr><tr><td><b>Accuracy</b></td><td colspan='3'>0.82</td></tr></table> | 82 / 450 [CSV](/data/processed/final-corpus/pre-filtered-corpus/wct_gpt-5.4-mini-v4.csv) |

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


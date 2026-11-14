# Dos d’âne carbone

Calculateur web simple pour estimer le **coût énergétique et carbone** d’un dos d’âne, dû à la réaccélération des véhicules.

## Utilisation

Ouvrir [`index.html`](index.html) dans un navigateur, ou servir le dossier en local :

```bash
python3 -m http.server 8000
```

Puis ouvrir [http://127.0.0.1:8000](http://127.0.0.1:8000).

## Saisies

| Champ | Défaut |
|--------|--------|
| Vitesse avant (ralentissement) | 30 km/h |
| Vitesse après (réaccélération) | 50 km/h |
| Véhicules / jour | 2000 |
| Masse moyenne (avancé) | 1450 kg |
| Rendement moteur (avancé) | 28 % |

## Modèle

1. Énergie cinétique supplémentaire : \( \frac12 m (v_2^2 - v_1^2) \) (vitesses en m/s)
2. Énergie carburant = énergie cinétique / rendement moteur
3. Litres = énergie carburant / 9,7 kWh/L
4. CO₂ ≈ 2,4 kg/L (moyenne pondérée parc français essence/diesel)

Les totaux jour et an (× 365) sont affichés en litres et kg (ou t) de CO₂.

**Estimation** basée sur le parc automobile français moyen — outil pédagogique, pas un bilan ACV.

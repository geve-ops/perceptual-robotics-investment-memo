# Perceptual Robotics: VC Investment Memo

An investment memo and startup screening model on **Perceptual Robotics**, a Bristol and Athens company that builds autonomous drones and AI software for wind turbine blade inspection.

**Recommendation: Track.** The technology and the Greek ecosystem link are attractive. But the company discloses no revenue, valuation or named customers, and better-funded rivals such as SkySpecs and Aerones already sell a similar product.

## What's inside

| File | What it is |
|---|---|
| `Perceptual_Robotics_Investment_Memo_GeraldVelas.pptx` | 13-slide memo: problem, product, market size (TAM, SAM, SOM), traction, go-to-market, competition, team, risks, screening model and decision |
| `Perceptual_Robotics_Screening_Model.ipynb` | Startup screening model, already run, with all outputs |
| `startup_data.csv` | Public dataset of 923 US startups used to train the model |
| `model_results.json` | Model metrics and Perceptual Robotics scores exported by the notebook |
| `figures/` | Charts produced by the notebook |

## The screening model

Logistic regression and random forest classifiers estimate whether a startup ends in an **acquisition** rather than a **shutdown**, using funding rounds, total funding, age at last funding, investor types and sector.

| Model | CV accuracy | CV AUC |
|---|---|---|
| Logistic regression | 71% | 0.70 |
| Random forest | 69% | 0.70 |
| Always guessing "acquired" | 65% | 0.50 |

Perceptual Robotics scores about **49%** in the base case, below the 65% dataset average. The score moves from 42% to 69% across the input scenarios, and the sector label alone moves it 20 points. So the model is a screening aid, not a verdict.

**Limits:** US-only training data, a narrow acquired-or-closed label, hindsight in the funding features, and no view of revenue, team quality or market size.

## Run it

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
jupyter notebook Perceptual_Robotics_Screening_Model.ipynb
```

## Sources

Funding, team and product facts come from public sources: the company website, University of Bristol news, DroneLife, Fortune, Greek business press and CB Insights. Market sizes are third-party estimates (NextMSC, Technavio, 360iResearch) with different definitions. Founder photos and the logo belong to Perceptual Robotics.

This is an independent student analysis, not affiliated with Perceptual Robotics or any investor. It is not investment advice.

## Author

Gerald Velas · MIS student · [LinkedIn](https://www.linkedin.com/in/geraldvelas)

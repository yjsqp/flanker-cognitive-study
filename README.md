# Cognitive Effects of Rapidly Changing Stimuli on Executive Control
### Flanker Task Research Platform

This project is a **web‑based cognitive psychology experiment system** built for science fair research.

It measures how **rapid visual stimulus exposure (video streams)** affects **executive control and attention**, using a **Flanker task** before and after exposure.

Everything runs **in the browser** — no installation or server required.

---

# 📦 Files

## collect.html
Runs the experiment and collects participant data.

Use this to test participants.

Features:
- configurable trial counts per block
- congruent % control
- demographics collection
- practice block with feedback
- pause + timers
- rapid stimulus exposure (YouTube playlist or video)
- automatic CSV export:
  - trials_PID.csv
  - summary_PID.csv

---

## analyzer.html
Offline analysis + merging tool.

Use this AFTER collecting data.

Features:
- upload multiple CSVs
- auto-merge participants
- master files:
  - master_trials.csv
  - master_summary.csv
- automatic statistics
- charts and summaries
- exports stats_report.csv

---

# 🚀 How to Run (GitHub Pages recommended)

## Option 1 — GitHub Pages (best)
1. Upload files to repo
2. Enable GitHub Pages
3. Open:

```
https://yourusername.github.io/repo/collect.html
https://yourusername.github.io/repo/analyzer.html
```

This avoids local CORS issues and allows YouTube playback.

---

## Option 2 — Local server
If running locally:

```
python -m http.server 8000
```

Then open:
```
http://localhost:8000/collect.html
```

Do NOT open with file:// (YouTube may fail to load).

---

# 🧪 Experimental Protocol

Flow:

Consent  
→ Instructions  
→ Practice  
→ Baseline Flanker  
→ Rapid Stimulus Exposure  
→ Post Flanker  
→ Rest  
→ Recovery Flanker  
→ Summary + Export  

---

# 📊 Data Structure

## trials_PID.csv (long format)
One row per trial

```
pid, block, trial, congruency, correct, rt
```

## summary_PID.csv (wide format)
One row per participant

Includes:
- demographics
- setup parameters
- interference cost metrics
- RT/accuracy by block

## Analyzer outputs
```
master_trials.csv
master_summary.csv
stats_report.csv
```

---

# 📈 Metrics Calculated

Per participant:
- mean RT
- accuracy
- interference cost (incongruent − congruent)
- post/baseline change
- recovery change

Group level:
- mean
- standard deviation
- paired t-test
- Cohen’s d

---

# 🧠 Research Notes

Why split files?
- smaller datasets
- easier Excel/R/Python analysis
- matches real cognitive science labs
- avoids repeated demographics

---

# 🔒 Privacy

- runs fully client-side
- no data uploaded anywhere
- files stay on participant’s computer

---

# 🛠 Tech

- HTML
- CSS
- Vanilla JavaScript
- Canvas charts
- No external libraries

---

# 👩‍🔬 Science Fair Tips

For judging:
- use GitHub Pages or local server
- preload videos locally if internet is unreliable
- export master files for analysis
- show analyzer charts live

---

# Authors
Student research project – Cognitive Psychology / Executive Control

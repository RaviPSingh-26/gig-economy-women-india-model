# Women, Work and the Gig Economy in India: Model

Machine-learning pipeline behind the "Door or Trap" analysis of women's work and
gig-economy participation in India (PLFS-based survey data). This repository holds
the **model code only**; the survey data and the written report are not included.

## Pipeline (run notebooks in order)
| Step | Notebook | Purpose |
|---|---|---|
| 01 | `01_data_preparation` | Load `.sav`, clean, build features and targets |
| 02 | `02_eda` | Exploratory analysis |
| 03 | `03_stage1_models` | Stage 1: who participates in the labour force |
| 04 | `04_stage2_models` | Stage 2: gig-proxy vs traditional work |
| 05 | `05_latent_gig_eligible` | Score non-participants for latent gig eligibility |
| 06 | `06_state_residual_map` | State-level residual gaps |
| 07 | `07_door_or_trap` | Earnings, security and contract scorecards |
| 08 | `08_fairness_and_export` | Subgroup fairness checks and export |

## Setup
```bash
pip install -r requirements.txt
```
Set `DATA_PATH` in `01_data_preparation` to your local `.sav` file. Steps write
intermediate files to `outputs/` (git-ignored), which later steps read.

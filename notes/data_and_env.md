
# Data Sources and Environments

---

## Robot Manipulation — Offline Datasets

Real robot demonstration data. `robotdataset` (local pkg) loads OXE, Table30v2, Agibot-World natively; OXE datasets discovered from `gs://gresearch/robotics`.

| Name | Links | `robotdataset` | Notes |
|------|-------|:--------------:|-------|
| Open-X-Embodiment | [site](https://robotics-transformer-x.github.io/) · [code](https://github.com/google-deepmind/open_x_embodiment) · [paper](https://arxiv.org/abs/2310.08864) | ✓ `OXEDataset` | 1M+ trajectories, 22 embodiments, 60+ datasets in RLDS format |
| DROID | [site](https://droid-dataset.github.io/) · [code](https://github.com/droid-dataset/droid) · [paper](https://arxiv.org/abs/2403.12945) | ✓ `OXEDataset` | 76k demos, 350 h, 564 scenes, in-the-wild; on `gs://gresearch/robotics/droid` |
| Agibot-World | [site](https://agibot-world.com/) · [code](https://github.com/OpenDriveLab/AgiBot-World) | ✓ `AgiBotWorldBetaDataset` | 1M+ demos, 100 robots, real-world scenes (home / restaurant / industrial) |
| Table30v2 | [data](https://huggingface.co/datasets/RoboChallenge/Table30v2) | ✓ `Table30v2Dataset` | 30 tabletop tasks, 4 embodiments; part of RoboChallenge |
| LIBERO | [site](https://libero-project.github.io/) · [code](https://github.com/Lifelong-Robot-Learning/LIBERO) · [paper](https://arxiv.org/abs/2306.03310) | — | Lifelong / knowledge-transfer benchmark; HDF5 format, not in OXE bucket |
| LIBERO-Plus | [paper](https://arxiv.org/abs/2510.13626) | — | LIBERO extension with 7-dimension perturbations for VLA robustness analysis |

---

## Robot Manipulation — Simulation Environments

| Name | Links | Notes |
|------|-------|-------|
| ManiSkill | [site](https://www.maniskill.ai/) · [code](https://github.com/haosulab/ManiSkill) · [docs](https://maniskill.readthedocs.io/) | GPU-parallelised; fast physics via SAPIEN |
| RoboCasa365 | [site](https://robocasa.ai/) · [code](https://github.com/robocasa/robocasa) · [paper](https://arxiv.org/abs/2603.04356) | 365 kitchen tasks, 2500 scene variants; also ships a human-demo dataset |
| RoboTwin | [site](https://robotwin-platform.github.io/) · [code](https://github.com/RoboTwin-Platform/RoboTwin) · [docs](https://robotwin-platform.github.io/doc/) · [paper](https://arxiv.org/abs/2506.18088) | 50-task bimanual sim + expert data generator; 100k+ trajectories on HF (LeRobot format) |
| MetaWorld | [docs](https://metaworld.farama.org/) · [code](https://github.com/Farama-Foundation/Metaworld) | 50 tasks, Sawyer arm, MuJoCo; multi-task and meta-RL benchmark |
| gymnasium/robotics | [docs](https://robotics.farama.org/) · [code](https://github.com/Farama-Foundation/Gymnasium-Robotics) | Fetch / Shadow Hand / Ant Maze envs; Farama Foundation |
| MimicGen | [site](https://mimicgen.github.io/) · [code](https://github.com/NVlabs/mimicgen) · [data](https://huggingface.co/datasets/amandlek/mimicgen_datasets) · [paper](https://arxiv.org/abs/2310.17596) | Data generator: scales human demos to 48k+ synthetic trajectories across 12 tasks |
| PushT | [code](https://github.com/real-stanford/diffusion_policy) · [data](https://diffusion-policy.cs.columbia.edu/data/training/) · [paper](https://arxiv.org/abs/2303.04137) | 2D T-block pushing env from Diffusion Policy; ~200 expert demos; simple but widely used for policy benchmarking |

---

## Robot Manipulation — Real-World Evaluation

| Name | Links | Notes |
|------|-------|-------|
| RoboArena | [site](https://robo-arena.github.io/) · [code](https://github.com/robo-arena/roboarena) · [paper](https://arxiv.org/abs/2506.18123) | Distributed pairwise eval of generalist policies on DROID hardware; live through Dec 2026 |

---

## Autonomous Driving & Navigation

| Name | Links | Notes |
|------|-------|-------|
| highway-env | [docs](https://highway-env.farama.org/) · [code](https://github.com/Farama-Foundation/HighwayEnv) | Highway, merge, roundabout, parking envs for decision-making research |

---

## Reasoning / General RL

| Name | Links | Notes |
|------|-------|-------|
| ARC-AGI-2 | [site](https://arcprize.org/) · [code](https://github.com/arcprize/ARC-AGI-2) | Abstract visual pattern completion; benchmark, not a standard RL env |
| MiniGrid | [docs](https://minigrid.farama.org/) · [code](https://github.com/Farama-Foundation/MiniGrid) | Lightweight partially-observable grid-world envs for RL research |

# Reward Ensembles

This repository accompanies  the pre-print
> Eisenstein, J. et al. [Helping or Herding? Reward Model Ensembles Mitigate but do not Eliminate Reward Hacking](https://arxiv.org/abs/2312.09244). (2023)

The repository contains links to pretrained checkpoints used in the
above manuscript. Specifically, we pre-train encoder-decoder models, following
precisely the procedure that was used to generate the checkpoints [in the original T5 paper (Raffel et al.)](https://github.com/google-research/text-to-text-transfer-transformer?tab=readme-ov-file#released-model-checkpoints). Importantly, we pre-train five
times, changing only the random seed, which controls the initialization of
parameters and sample of data from C4 used for pretraining.

These checkpoints can be useful for creating ensembles (as we did in the above manuscript), analyzing differences between different pretrain checkpoints that were trained using the same procedure, estimating uncertainty, etc.


We release 15 checkpoints, five for T5-base models, five for T5-large models, and five for T5-XL models.

## Checkpoints

Download the checkpoints from here. Each GCS path contains five directories each corresponding to a different pretrained model.

| Model | GCS Path |
|---|---|
| T5-base | gs://reward_ensembles/base |
| T5-large | gs:/reward_ensembles/large |
| T5-XL | gs://reward_ensembles/xl |

## Citing this work

If you use the checkpoints, please cite:

```bibtex
@article{eisenstein2023helping,
  author = {Jacob Eisenstein and Chirag Nagpal and Alekh Agarwal and Ahmad Beirami and Alex D'Amour and DJ Dvijotham and Adam Fisch and Katherine Heller and Stephen Pfohl and Deepak Ramachandran and Peter Shaw and Jonathan Berant},
  journal = {arXiv preprint arXiv:2312.09244},
  title = {Helping or Herding? Reward Model Ensembles Mitigate but do not Eliminate Reward Hacking},
  year = {2023},
}
```
## License and disclaimer

Copyright 2024 DeepMind Technologies Limited

All software is licensed under the Apache License, Version 2.0 (Apache 2.0);
you may not use this file except in compliance with the Apache 2.0 license.
You may obtain a copy of the Apache 2.0 license at:
https://www.apache.org/licenses/LICENSE-2.0

All other materials are licensed under the Creative Commons Attribution 4.0
International License (CC-BY). You may obtain a copy of the CC-BY license at:
https://creativecommons.org/licenses/by/4.0/legalcode

Unless required by applicable law or agreed to in writing, all software and
materials distributed here under the Apache 2.0 or CC-BY licenses are
distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,
either express or implied. See the licenses for the specific language governing
permissions and limitations under those licenses.

This is not an official Google product.

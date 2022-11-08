## Efficient Tuning

Vanilla methods try to make a pre-train model carry out downstream tasks by tuning the model parameters in a completed tuning manner or tuning the task-specific head for more flexibility and fixing the backbone for maintaining the learned feature extraction. The first manner obtains better performance but leads to expensive computation, while the second is limited in inference accuracy. 

To tradeoff the two aspects, VPT incorporates visual prompts for efficient tuning. The visual prompt is prepended directly to the input sequence as of the shallow architecture or to input sequences for each computation operator as of the deep one. In the tuning phase, weights only update at the prompt parameters and the prediction head. Firstly,  VPT can obtain a bonus in performance with few active parameters. Secondly, as for the flexibility, it only needs to update the active param as transferring to the downstream task.

- Visual prompt tuning. ECCV 2022.
  - arXiv: 2203.12119
  - code: KMnP/vpt


# adversarial_inspection

## Goal

1. Determine the frequency at which many popular adversarial attack algorithms produce **invalid** data (i.e. the "true" semantics no longer align with the label). 
2. Determine criteria for which valid data is measured. 

Candidates observed in existing work:
  - __Classification__: related to model performance on the generated adversaries.
  - __Annotation__: the degree to which humans agree with the adversarial examples, plus the agreement among themselves as a function of the text quality. NOTE: many papers used inter-annotator agreement (IAA) to validate human performance, but this category only counts papers which used IAA as a direct measure of text quality (essentially a proxy for clarity). 
  - __Similarity__: how similar are the generated adversaries vs. the source texts?
  - __Diversity__: how linguistically diverse are the generated adversaries vs. the source texts?
  - __Fluency__: how grammatical / natural are the generated adversaries?
  - __Efficiency__: how efficient are the algorithms that produce the adversaries? NOTE: efficiency is not a property of the text and is thus excluded from RQ1 consideration, but it was just collected for completeness. 
  
Possible additional criteria:
  - __Toxicity__? Rationale: models failing to identify toxic text is more urgent than failing on generic topics. Example: if a human preference model (e.g. RLHF) rates “You’re a disgusting pig” as acceptable, that’s more important than it rating “You’re a lovely person” as unacceptable. In the first case, we’re greenlighting toxic abuse, in the second we are encouraging the model to not give compliments. 
  - __Factuality__? Rationale: models failing to identify fake information is less important than if they fail on content that is actually true. Example: if we detect bias against a fictional race of aliens, that’s not as important as bias against minorities that actually exist. 

## Update

It appears that the intention of this project has already been realized in [AdvGLUE](https://adversarialglue.github.io/). Putting this on the backburner for now. 

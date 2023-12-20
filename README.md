<img width="1259" alt="FANER" src="https://github.com/nehalelkaref/Flat-Arabic-NER/assets/16616024/bc2636e5-0329-44e3-bce5-92c425a23df6">

# Flat Arbaic NER
Classifying Flat Arabic entities using an esemble of two models built using _StagedNER_ and supplementary POS tags ranking 🥈 2nd place in [NER Shared tasks](https://dlnlp.ai/st/wojood/results)

Data: [Wojood corpus](https://aclanthology.org/2022.lrec-1.387.pdf)
  - consists of 21 entity types
  - Majority of data comes in MSA while the rest is in the Levant dialects (Palestinian and Lebanese)

Method: 
  - Staged NER trains two instances of the same transformer
  - One transformer is trained on classifying BIO spans in the first stage and the second transformer is trained on classifying entity types in the second stage
  - We strengthen the first stage by supplementry MSA and LEV pos tags from [CaMeL tools](https://github.com/CAMeL-Lab/camel_tools)
  - The demoed model is an ensemble of two AraBERTv2 transformers one trained using MSA POS tags and another using LEV POS tags
  - to reproduce StagedNER checkout our paper [here](https://aclanthology.org/2023.arabicnlp-1.91/)

Check our demo here: [Flat-ANER Demo](https://huggingface.co/spaces/nehalelkaref/flat-arabic-entity-classification?logs=build)


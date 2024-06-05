# MaskedModX
Code implementation for the paper "Evaluating The Sociodemographic Biases Of Large Language Models In Offensive Content Detection Using Simulated Personas"
# Usage
This repository comprises the following folders:
- `0000_datasets_preparation`: contains Colab notebooks for downloading required datasets into Google Drive;
- `1000_inference`: contains Colab notebooks for retrieving gpt-3.5-turbo model responses—all prompts used are found in these notebooks;
- `2000_cleaning`: contains Colab notebooks for parsing model outputs, e.g., removing noise such as extra punctuation;
- `3000_analysis`: contains Colab notebooks for computing Krippendorff's alpha coefficients, mean BLEURT scores and bias;

For running 3003_IHC_NLE_analysis.ipynb, you will require around 8.7GB of GPU RAM. Paid versions of Colab will give you access to faster GPUs. Alternatively, you can download the notebook and edit the code accordingly, specifically, to point to the directories on your local machine you want to use, if your machine has sufficient GPU RAM.

Run the notebooks sequentially by folder name, i.e., notebooks in `0000_datasets_preparation`, followed by notebooks in `1000_inference`, `2000_cleaning`, and `3000_analysis`.

Run the notebooks sequentially by notebook name, e.g., 0001_COVID-HATE_preparation.ipynb, followed by 0002_IHC_preparation.ipynb and so on.

Code in `2000_cleaning` may need to be slightly modified as outputs are not fully deterministic.

# Datasets
We use the following datasets:

COVID-HATE [1]

Implicit Hate Corpus (IHC) [2]

Social Bias Inference Corpus (SBIC) [3]

Annotators with Attitudes (AWA) [4]

POPQUORN [5]

# Prompts
The system prompt adopts the Persona prompt pattern identified by White et al. [6].

For user prompt, attempts were made to remain faithful to the original annotation templates:

Implicit Hate Corpus (IHC) [2]

Social Bias Inference Corpus (SBIC) [3, 7]

Annotators with Attitudes (AWA) [4, 8]

POPQUORN [5, 9]

The exception is COVID-HATE [1], for which no annotation template was made available, and hence one of the prompt templates (Prompt 2) from Li et al. [10] was used in combination with definitions from the COVID-HATE study [1]. For all tasks except for the generation of NLEs for IHC [2], we included in the user prompt constraints on the possible answer options, emulating Ziems et al. [11]. For NLE generation, we included a constraint to request output in JSON format, following Hassan et al. [12]. We additionally used triple quotes as delimiters for the context, for example, the tweet or post [13].

# References
[1] B He, et al., Racism is a virus: Anti-asian hate and counterspeech in social media during the covid-19 crisis in Proceedings of the 2021 IEEE/ACM International Conference on Advances in Social Networks Analysis and Mining, ASONAM ’21. (Association for Computing Machinery, New York, NY, USA), p. 90–94 (2022).

[2] M ElSherief, et al., Latent hatred: A benchmark for understanding implicit hate speech in Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing. (Association for Computational Linguistics, Online and Punta Cana, Dominican Republic), pp. 345–363 (2021).

[3] M Sap, et al., Social bias frames: Reasoning about social and power implications of language in Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics. (Association for Computational Linguistics, Online), pp. 5477–5490 (2020).

[4] M Sap, et al., Annotators with attitudes: How annotator beliefs and identities bias toxic language detection in Proceedings of the 2022 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies. (Association for Computational Linguistics, Seattle, United States, pp. 5884-5906 (2022).

[5] J Pei, D Jurgens, When do annotator demographics matter? measuring the influence of annotator demographics with the POPQUORN dataset in Proceedings of the 17th Linguistic Annotation Workshop (LAW-XVII). (Association for Computational Linguistics, Toronto, Canada), pp. 252–265 (2023).

[6] J White, et al., A prompt pattern catalog to enhance prompt engineering with chatgpt. CoRR abs/2302.11382 (2023).

[7] M Sap, et al., Full instructions (https://maartensap.com/social-bias-frames/annotationTask.html) (2022) Accessed: 2024-04-17.

[8] M Sap, et al., Full instructions (https://maartensap.com/racial-bias-hatespeech/annWithAttitudes-LargeScale.html) (2022) Accessed: 2024-04-17.

[9] J Pei, D Jurgens, Using the annotation interfaces (https://github.com/Jiaxin-Pei/Potato-Prolific-Dataset) (2023) Accessed: 2024-04-17.

[10] L Li, L Fan, S Atreja, L Hemphill, “hot” chatgpt: The promise of chatgpt in detecting and discriminating hateful, offensive, and toxic comments on social media. ACM Trans. Web 18 (2024).

[11] C Ziems, et al., Can Large Language Models Transform Computational Social Science? Comput. Linguist. pp. 1–55 (2024).

[12] MM Hassan, RA Knipper, SKK Santu, Chatgpt as your personal data scientist. CoRR abs/2305.13657 (2023).

[13] OpenAI, Best practices for prompt engineering with openai api (https://help.openai.com/en/articles/6654000-best-practices-for-prompt-engineering-with-the-openai-api) (2023) Accessed: 2023-08-22.

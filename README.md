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
We use datasets presented in the following papers:
- He, B., Ziems, C., Soni, S., Ramakrishnan, N., Yang, D., Kumar, S.: Racism is a
virus: Anti-asian hate and counterspeech in social media during the covid-19 crisis.
In: Proceedings of the 2021 IEEE/ACM International Conference on Advances
in Social Networks Analysis and Mining. ASONAM ’21, pp. 90–94. Association
for Computing Machinery, New York, NY, USA (2022). https://doi.org/10.1145/3487351.3488324
- ElSherief, M., Ziems, C., Muchlinski, D., Anupindi, V., Seybolt, J., De Choudhury, M., Yang, D.: Latent hatred: A benchmark for understanding implicit hate
speech. In: Proceedings of the 2021 Conference on Empirical Methods in Natural
Language Processing, pp. 345–363. Association for Computational Linguistics,
Online and Punta Cana, Dominican Republic (2021). https://doi.org/10.18653/v1/2021.emnlp-main.29 . https://aclanthology.org/2021.emnlp-main.29
- Sap, M., Gabriel, S., Qin, L., Jurafsky, D., Smith, N.A., Choi, Y.: Social bias
frames: Reasoning about social and power implications of language. In: Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics,
pp. 5477–5490. Association for Computational Linguistics, Online (2020). https://doi.org/10.18653/v1/2020.acl-main.486 . https://aclanthology.org/2020.acl-main.486
- Sap, M., Swayamdipta, S., Vianna, L., Zhou, X., Choi, Y., Smith, N.A.: Annotators with attitudes: How annotator beliefs and identities bias toxic language
detection. In: Proceedings of the 2022 Conference of the North American
Chapter of the Association for Computational Linguistics: Human Language
Technologies, pp. 5884–5906. Association for Computational Linguistics, Seattle, United States (2022). https://doi.org/10.18653/v1/2022.naacl-main.431 .
https://aclanthology.org/2022.naacl-main.431
- Pei, J., Jurgens, D.: When do annotator demographics matter? measuring the
influence of annotator demographics with the POPQUORN dataset. In: Proceedings of the 17th Linguistic Annotation Workshop (LAW-XVII), pp. 252–265.
Association for Computational Linguistics, Toronto, Canada (2023). https://doi.org/10.18653/v1/2023.law-1.25 . https://aclanthology.org/2023.law-1.25

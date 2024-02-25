# CantCounter

Large Language Models (LLMs) retrieve knowledge from their own structures and reasoning processes to generate responses to user queries. Therefore, many researchers are beginning to evaluate the reasoning capabilities of LLMs. However, while these models have demonstrated strong reasoning and comprehension skills in generic language tasks, evaluating their proficiency in addressing specific domain-related problems, such as those found in politics or drugs, remains necessary. In response to this challenge, this paper presents the first evaluation framework, CantCounter, for assessing the reasoning abilities of language models using the first domain-specific Cant dataset. Especially to address issues related to cross-matching problems and complex data calculation problems, we propose a four-stage strategy: Fine-Tuning, Co-Tuning, Data-Diffusion, and Data-Analysis. Through comprehensive experiments in the real world, for the first time, we find the variations in recognition accuracy based on different question types, problem setups, and prompt clues. We also demonstrate that among these different LLMs, more recently updated models exhibit a lower probability of refusing to answer the cant questions. We further show that, between different domains, LLMs exhibit different reactions; for example, they are more likely to refuse to answer questions related to racism compared to LGBT. Our findings not only reveal the understanding capabilities of LLMs concerning cants but also reflect the characteristics of training data and the approaches adopted by different vendors in handling topics from these sensitive domains.

# After the Review Period we update our work, dataset and codes.
Please see batch for code.

First, make sure you have Python 3.8 installed on your machine
$ python --version
Python 3.8
Next, create a virtual environment and install the project's dependencies within the virtual environment
# Pull warehouse
$ https://github.com/cistineup/CantCounter.git

# Go to directory
$ cd CantCounter

# Install all dependencies
$ pip install -r requirements.txt

# Enter fine-tuning
$ cd cantcounter_finetuned-gpt2-convai-main
$python generate_drug_news.py # Take the field of drugs
Because the fine-tuning is done separately in different domains, you need to set the domains manually

# Enter the overall test
$ cd cantcounter_gpt_test
$ cd drugs
In the case of drugs_zero_shot.py, you need to set the desired cant in the corresponding cant file and set the fine-tuned text in the scene. Put them in drugs_zero_shot.py at the same time and then run.

# Run test
$ python drugs_zero_shot.py

The final test results will be summarized and sorted in the test data.

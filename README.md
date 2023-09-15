
<h1 align="center">TAL-SCQ5K</h1>


## Dataset Description

### Dataset Summary

TAL-SCQ5K-EN/TAL-SCQ5K-CN are high quality mathematical competition datasets in English and Chinese language created by TAL Education Group, each consisting of 5K questions(3K training and 2K testing). The questions are in the form of multiple-choice and cover mathematical topics at the primary,junior high and high school levels. In addition, detailed solution steps are provided to facilitate CoT training and all the mathematical expressions in the questions have been presented as standard text-mode Latex.

### Supported Tasks and Leaderboards

[More Information Needed]

### Languages

The text in TAL-SCQ5K-EN is in English and TAL-SCQ5K-CN  is in Chinese.

## Dataset Structure

### Data Instances

```
{
	"dataset_name": "prime_math_competition_en_single_choice_8K_dev",
	"dataset_version": "2023-07-07",
	"qid": "244",
	"queId": "8afc802a8c304199b1040f11ffa2e92a",
	"competition_source_list": [],
	"difficulty": "2",
	"qtype": "single_choice",
	"problem": "A $14$-digit. number $666666 XY 444444$ is a multiple of $26$. If $X$ and $Y$ are both positive, what is the smallest vaue of $X+ Y$? ",
	"answer_option_list": [
		[{
			"aoVal": "A",
			"content": "$$3$$ "
		}],
		[{
			"aoVal": "B",
			"content": "$$4$$ "
		}],
		[{
			"aoVal": "C",
			"content": "$$9$$ "
		}],
		[{
			"aoVal": "D",
			"content": "$$14$$ "
		}],
		[{
			"aoVal": "E",
			"content": "None of the above "
		}]
	],
	"knowledge_point_routes": ["Overseas Competition->Knowledge Point->Number Theory Modules->Division without Remainders->Divisibility Rules"],
	"answer_analysis": ["Since $1001$ is a multiple of $13$, $111111 = 111 \\times 1001$ is also a multiple of $13$.  It follows that both $666666$ and $444444$ are both multiples of $26$.  $666666XY 444444 = 66666600000000 + XY 000000 + 444444$  $\\Rightarrow XY$ must be divisible by $13$.  Smallest $X+Y=1+3=4$. "],
	"answer_value": "B"
}
```

### Data Fields

* "dataset_name": identification of the source dataset name from which TAL-SCQ5K-EN/TAL-SCQ5K-CN has been created, use only for inner of TAL education group, please ignore.
* "dataset_version": identification of the source dataset version from which TAL-SCQ5K-EN/TAL-SCQ5K-CN has been created, use only for inner of TAL education group, please ignore.
* "qid": identification of local id of the question in the source dataset from which TAL-SCQ5K-EN/TAL-SCQ5K-CN has been created, use only for inner of TAL education group, please ignore.
* "queId": identification of global id of the question, use only for inner of TAL education group, please ignore.
* "competition_source_list": identification of math competitions in which the questions appeared, if have been logged.
* "difficulty": difficulty level of the questions, value ranged from 0 to 4
* "qtype": question type, valued as "single_choice" for all the questions in this dataset indicates that all the questions are multiple-choice questions with unique ground-truth answer.
* "problem": the question string to a math competition question.
* "answer_option_list": answer choices to be selected
* "knowledge_point_routes": knowledge point route from coarse-grained to fine-grained.
* "answer_analysis": step-by-step answer analysis of the questions, which helps CoT training
* "answer_value": value of the ground-truth answer choice


### Data Splits


| name|train|test |
|:---:|:----:|:----:|
|TAL-SCQ5K-EN|3K  |2K  |
|TAL-SCQ5K-CN|3K  |2K  |

## Usage

Each of the above datasets is located in a separate sub-directory. To load an individual subset, use the data_dir argument of the load_dataset() function as follows:

```python
from datasets import load_dataset

# Load all subsets (share the same schema)
dataset = load_dataset("math-eval/TAL-SCQ5K")

# Load TAL-SCQ5K-EN
dataset = load_dataset("math-eval/TAL-SCQ5K", data_dir="TAL-SCQ5K-EN")

# Load TAL-SCQ5K-CN
dataset = load_dataset("math-eval/TAL-SCQ5K", data_dir="TAL-SCQ5K-CN")

```


## Additional Information

### Dataset Curators

[More Information Needed]

### Licensing Information

The TAL-SCQ5K dataset is licensed under the [MIT License](https://opensource.org/license/mit/)

### Citation Information

[More Information Needed]

### Contact

The original authors host this dataset on GitHub here: https://github.com/math-eval/TAL-SCQ5K You can submit inquiries to: matheval.ai@gmail.com

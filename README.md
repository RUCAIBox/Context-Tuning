# Context-Tuning
This is the repository for COLING 2022 paper "Context-Tuning: Learning Contextualized Prompts for Natural Language Generation". The implementation is completely based on our text generation library **[TextBox 2.0](https://github.com/RUCAIBox/TextBox)**.

## Installation
You should clone the TextBox repository and follow its [instructions](https://github.com/RUCAIBox/TextBox#installation).
```bash
git clone https://github.com/RUCAIBox/TextBox.git && cd TextBox
bash install.sh
```

## Dataset
The datasets ROCStories (roc), WritingPrompts (wp), WikiPlots (wikip), and ChangeMyView (cmv) can be downloaded at the link [https://huggingface.co/datasets/RUCAIBox/Story-Generation](https://huggingface.co/datasets/RUCAIBox/Story-Generation).

## Running Context-Tuning based on TextBox
For example, you can conduct Context-Tuning on roc dataset using this command:
```bash
python run_textbox.py --model=Context_Tuning --dataset=roc
```
You can use `--dataset=xxx` to specify the dataset name, such as `roc`, `wp`, `wikip`, and `cmv`.

Other hyperparameters can be changed in the [yaml](https://github.com/RUCAIBox/TextBox/blob/2.0.0/textbox/properties/model/context_tuning.yaml). The `prompt_generator` can be set to `bert` or `roberta`. The `semantic_mapping` can be set to `True` or `False`. The `prompt_length` of `efficient_kwargs` can also be changed at your will. 


## Reference
```bibtex
@inproceedings{tang-etal-2022-context,
    title = "Context-Tuning: Learning Contextualized Prompts for Natural Language Generation",
    author = "Tang, Tianyi  and
      Li, Junyi  and
      Zhao, Wayne Xin  and
      Wen, Ji-Rong",
    booktitle = "Proceedings of the 29th International Conference on Computational Linguistics",
    month = oct,
    year = "2022",
    address = "Gyeongju, Republic of Korea",
    publisher = "International Committee on Computational Linguistics",
    url = "https://aclanthology.org/2022.coling-1.552",
    pages = "6340--6354",
}
```

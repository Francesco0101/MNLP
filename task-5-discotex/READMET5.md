# TASK 22 - DisCoTEX
- Homepage: https://sites.google.com/view/discotex/task?authuser=0
- Data: https://sites.google.com/view/discotex/data

## Data
- **Task 1 - Last sentence classification**: binary classification task; given a short paragraph (originally called prompt) and an individual sentence (target), classify whether the target follows or not, thus joining it to the prompt gives out a coherent or incoherent text.

- **Task 2 - Human score prediction**: regression task; predict the average coherence score assigned by human raters to short paragraphs which were evaluated both in their original and artificially modified version. Judgments will be collected through crowdsourcing and on an ordinal scale (i.e. 5-point Likert Scale), on the assumption that coherence is a gradual notion.

**NOTE**: for task 2, you are required to: a) _cast the scores as integers_ (you choose how and motivate why), and then b) _verbalise the scores_ using the common Likert-scale verbalisation (e.g., "Eccellente" in place of "5"). 
Furthermore, the actual data may have scores ranging over the previously mentioned Likert-scale; what you can do is simply to use the new range.

The dataset is already splitted into training and test data.
For further details on the data, please refer to the website. 

## Expected output

The expected output is two (2) datasets per tasks + one (1) prompt file per tasks.

### Task 1 - Last sentence classification
Files to submit: 
- `discotex-task1-train-data.jsonl`
- `discotex-task1-test-data.jsonl`
- `discotex-task1-prompt.jsonl`

Each line in the data files should be a JSON object following this format:
```JSON
{
    "id":           int,
    "text":         str,
    "target":       str,
    "choices":      list[str],
    "label":        int
}
```

In the prompt file you have to report the prompts you designed for the task.
Each line in the prompt files should be a JSON object following this format (max 5 lines):
```JSON
{
    "prompt": str
}
```

### Task 2 - Human score prediction
Files to submit: 
- `discotex-task2-train-data.jsonl`
- `discotex-task2-test-data.jsonl`
- `discotex-task2-prompt.jsonl`

Each line in the data files should be a JSON object following this format:
```JSON
{
    "id":           int,
    "text":         str,
    "choices":      list[str],
    "label":        int
}
```

In the prompt file you have to report the prompts you designed for the task.
Each line in the prompt files should be a JSON object following this format (max 5 lines):
```JSON
{
    "prompt": str
}
```

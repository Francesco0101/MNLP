# DisCoTex

Datasets for all the sub-tasks are released as tab-separated text files. 

For the first sub-task (Last sentence classification) we kept separated data from the two sources (i.e. Wikipedia and TED). Both versions present the following structure:

    ID: a simple identifier for the entry;

    PROMPT: a small snippet of text (3 sentences on average);

    TARGET: the sentence for which participants are asked to assess if it is coherent with the PROMPT (i.e. it is the next sentence after the PROMPT);

    CLASS: the class to be predicted. 1 stands for the positive class (i.e. the TARGET follows the PROMPT), 0 for the negative one (i.e. the TARGET does not follow the PROMPT).

For the second sub-task (Human score prediction) we mixed data from the two sources and we release a single dataset with the followng structure:

    ID: a simple identifier for the entry;

    TEXT: a small snippet of text (4 sentences on average), to be evaluated;

    MEAN: the coherence score of the TEXT to be predicted, based on the mean of the human judgements collected;

    STDEV: standard deviation of the coherence score.


Data for the official test will be provided in the same format, with the exception of the CLASS column for Sub-task 1, and the MEAN and the STDEV columns for Sub-task 2.

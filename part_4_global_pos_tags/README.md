# PART 4: POS Tagging on a non-English language

The goal of this part of the tutorial is that you use the skills acquired in the previous parts, and apply them to your own problem. 
Therefore, you have to find a dataset that you want to work with, write labeling functions, and train a model.

## Dataset

First, you need to download all necessary files and then, choose a dataset.

### Downloading the files

Download the zipped file using [this link](https://lindat.mff.cuni.cz/repository/xmlui/bitstream/handle/11234/1-3105/ud-treebanks-v2.5.tgz) 
and move it to the `part_4_global_pos_tags` folder.

Run the following command to extract and setup the files:

```bash
# First navigate into the part_4_global_pos_tags folder with your terminal, and run
./extract_files.sh
```

If you use Windows, create a folder `assets/` in the `part_4_global_pos_tags` folder, and extract the files into it.

### Extracting the files

Now you need to choose a dataset. Ideally, it is a treebank of a language you speak. 
You can find a list of all available languages in the `assets/` folder.

Make sure there exists a train file, and a test file for the language you want to work with, or create the split yourself.
For all data science projects, also weak supervision projects, it is always important to test your model on unseen data, so make sure you have a test set.

For example, if you want to work with a German treebank, you need to first open the file `create_data.sh` and change the following line:

```bash
# Change this line to the language you want to work with, e.g. German
vars_ud_treebank="UD_German-GSD"
```

With your Python environment for this tutorial activated, you need to run the following command:

```bash
./create_data.sh
```

and the data will be available in the `corpus/` folder, exactly as in part 3 of the tutorial.

## Project specifications

Use the knowledge from today's tutorial to solve the POS tagging task in the language of your choice.
You can use the code from part 3 as a starting point, but you will need to make some changes.
Your solution should contain the following steps:

1. Load the data
2. Write labeling functions
3. Evaluate the labeling functions
4. Train a model
5. Evaluate the model

Ideas 4 having fun:
- Could multiple languages be useful?
- How to use Spacy's transformer models, if you have a GPU?
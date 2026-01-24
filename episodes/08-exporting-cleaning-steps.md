---
title: Exporting Data Cleaning Steps
teaching: 10
exercises: 5
---

::::::::::::::::::::::::::::::::::::::: objectives

- Describe how OpenRefine generates JSON code.
- Demonstrate ability to export JSON code from OpenRefine.
- Save JSON code from an analysis.
- Apply saved JSON code to an analysis.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- How can we document the data-cleaning steps we've applied to our data?
- How can we apply these steps to additional data sets?

::::::::::::::::::::::::::::::::::::::::::::::::::

## Export the steps to clean up and enhance the dataset

As you conduct your data cleaning and preliminary analysis, OpenRefine saves every change you make to the dataset. These
changes are saved in a format known as JSON (JavaScript Object Notation). You can export this JSON script and apply it to other data files. If you had 20 files to clean, and they all had the same type of errors (e.g. species name misspellings, leading white spaces), and all
files had the same column names, you could save the JSON script, open a new file to clean in OpenRefine, paste in the script and run it. This gives you a quick way to clean all of your related data.

1. In the `Undo / Redo` section, click `Extract...`, and select the steps that you want to apply to other datasets by clicking the check boxes.
2. Copy the code from the right hand panel and paste it into a text editor (like NotePad on Windows or TextEdit on Mac). Make sure it saves as a plain text file. In TextEdit, do this by selecting `Format` > `Make plain text` and save the file as a `txt` file.

Let's practice running these steps on a new dataset. We'll test this on an uncleaned version of the dataset we've been working with.

:::::::::::::::::::::::::::::::::::::::  challenge

## Exercise

1. Download an uncleaned version of the dataset from the [Setup](../learners/setup.md) page or use the version of the raw dataset you saved to your computer.
2. Start a new project in OpenRefine with this file and name it something different from your existing project.
3. Click the `Undo / Redo` tab > `Apply` and paste in the contents of `txt` file with the JSON code.
4. Click `Perform operations`. The dataset should now be the same as your other cleaned dataset.

For convenience, we used the same dataset. In reality you could use this process to clean related datasets. For example, data that you had collected over different fieldwork periods or data that was collected by different researchers (provided everyone uses the same column headings).


::::::::::::::::::::::::::::::::::::::::::::::::::

## Reproducible science

Now, that you know how scripts work, you may wonder how to use them in your own scientific research. For inspiration, you can read more about the succesful application of the reproducible science principles in archaeology or marine ecology:

1. Marwick et al. (2017) [Computational Reproducibility in Archaeological Research: Basic Principles and a Case Study of Their Implementation](https://link.springer.com/article/10.1007/s10816-015-9272-9)
2. Stewart Lowndes et al. (2017) [Our path to better science in less time using open data science tools](https://www.nature.com/articles/s41559-017-0160)

:::::::::::::::::::::::::::::::::::::::  challenge

## Exercise (optional): Use an LLM to draft a Methods-style description of your cleaning steps

OpenRefine records the transformations you apply to your data in the **Undo / Redo** history. These steps can be exported as JSON, which is useful for reproducibility and sharing.

If you want, you can try using a large language model (LLM) (outside of the OpenRefine environment, one that is accessible to you online and free to use) to turn the exported JSON into a human-readable description that could be used as the basis for a *Methods* section in a paper.

1. Open **Undo / Redo** in OpenRefine.
2. Click **Extract...** and copy the exported JSON (or copy a subset of the most relevant steps).
3. Paste the JSON into an LLM interface of your choice.
4. Ask the LLM to draft a concise methods description. For example: 

> Below is an OpenRefine Undo/Redo JSON export describing data cleaning steps.
> Please draft a short Methods section paragraph that describes what was done.
> Use clear scientific language.
> Keep it reproducible: describe the operations, but do not invent steps that are not present.
> If something is unclear from the JSON alone, explicitly say so rather than guessing.


5. Read the output and revise it:
- Does it accurately describe what you did?
- Did it add steps or intentions that are not present in the JSON?
- Is it too vague to be reproducible?

Note: LLMs can be helpful for rewriting and summarising, but you should always verify the output for accuracy and completeness.

:::::::::::::::::::::::::  solution

## Discussion

A strong summary usually:
- Groups many small operations into a few clear actions (for example: “standardised country names”, “split scientific names”, “reconciled locations against Wikidata”)
- Uses readable language that could be shared with collaborators

Common issues to watch for:
- The LLM invents motivations or steps that are not in the JSON
- Important details are omitted (for example: which column was transformed)
- The wording becomes too vague to support reproducibility

A practical workflow is to treat the LLM output as a *first draft* and then edit it yourself.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: keypoints

- All changes are being tracked in OpenRefine, and this information can be used for scripts for future analyses or reproducing an analysis.
- Scripts can (and should) be published together with the dataset as part of the digital appendix of the research output.

::::::::::::::::::::::::::::::::::::::::::::::::::



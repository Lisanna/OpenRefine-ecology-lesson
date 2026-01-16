---
title: Introduction
teaching: 10
exercises: 0
---

::::::::::::::::::::::::::::::::::::::: objectives

- Describe OpenRefine’s uses and applications.
- Differentiate data cleaning from data organization.
- Experiment with OpenRefine’s user interface.
- Locate helpful resources to learn more about OpenRefine.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- How is OpenRefine useful?

::::::::::::::::::::::::::::::::::::::::::::::::::

## Lesson

## Motivations for the OpenRefine Lesson

- Data is often very messy, and this tool saves a lot of time on cleaning
  headaches.

- Data cleaning steps often need repeating with multiple files. It is important to know what you did to your data. This makes it possible for you to repeat these steps again with similarly structured data. OpenRefine is
  perfect for speeding up repetitive tasks by replaying previous actions on
  multiple datasets.

- Additionally, journals, granting agencies, and other institutions are requiring documentation of the
  steps you took when working with your data. With OpenRefine, you can capture
  all actions applied to your raw data and share them with your publication as
  supplemental material.

- Any operation that changes the data in OpenRefine can be reversed or
  undone.

- Some concepts such as clustering algorithms are quite complex, but with OpenRefine
  we can introduce them, use them, and show their power.
  
  > **Note:** You must export your modified dataset to a new file: OpenRefine does not save over the original source file. All changes are stored in the OpenRefine project.

## Before we get started

The following setup is necessary before we can get started (see the [instructions here](../learners/setup.md).)

## What is OpenRefine?

- OpenRefine is a Java program that runs on your machine (not in the cloud): it is a desktop application that uses your web browser as a graphical interface. No internet connection is needed, and none of the data or commands you enter in OpenRefine are sent to a remote server.
- OpenRefine does not modify your original dataset. All actions can be reversed in OpenRefine and you can capture all the actions applied to your data and share this documentation with your publication as supplemental material.
- OpenRefine saves as you go. You can return to the project at any time to pick up where you left off or export your data to a new file.
- OpenRefine can be used to standardise and clean data across your file.

### It can also help you

- Get an overview of a data set
- Resolve inconsistencies in a data set
- Help you split data up into more granular parts
- Match local data up to other data sets
- Enhance a data set with data from other sources
- Save a set of data cleaning steps to replay on multiple files

OpenRefine is a powerful, free, and open source tool with a large growing community of practice. More help can be found at [https://openrefine.org](https://openrefine.org).

### Features

- Open source ([source on GitHub](https://github.com/OpenRefine/OpenRefine)).
- A large growing community, from novice to expert, ready to help.

### More Information on OpenRefine

You can find out a lot more about OpenRefine at the official user manual [docs.openrefine.org](https://docs.openrefine.org/). There is a [user forum](https://forum.openrefine.org) that can answer a lot of beginner questions and problems. [Recipes](https://github.com/OpenRefine/OpenRefine/wiki/Recipes), scripts, projects, and extensions are available to add functionality to OpenRefine. These can be copied into your OpenRefine instance to run on your dataset.

## Optional: Using the AI extension with OpenRefine

Some parts of this lesson include optional activities using an experimental **AI extension for OpenRefine**.  
This extension allows you to use a large language model (LLM) to help generate new columns based on existing data (for example, extracting standardised values).

You do **not** need to use the AI extension to complete the core OpenRefine lesson.  
If you choose to use it, the following sections explain what it is and how to set it up.

### What is an LLM provider?

The AI extension does not contain an AI model itself. Instead, it connects to an external **LLM provider**.

An LLM (Large Language Model) is a type of software that can generate text based on patterns learned from data. Examples include models accessed through:

- Online services (e.g. commercial APIs)
- Locally running models (e.g. via tools such as Ollama or LM Studio)

An **LLM provider** is simply the configuration that tells OpenRefine:
- Which model to use
- Where the model is running (URL / endpoint)
- How to authenticate (API key, if required)

Different workshops may use different providers depending on availability, cost, or institutional policy. Your instructor will tell you which provider to use for your session.

### Installing the AI extension

To install the AI extension for OpenRefine:

1. In OpenRefine, go to **Extensions**.
2. Click **Open Extensions directory**. This opens a file explorer showing a folder called `extensions`.
3. Download **AI Extension for OpenRefine version 0.1.2.3**  (file name: `openrefine-llm-extension-0.1.2.zip`).
4. Extract the zip file into the `extensions` folder. After extraction, you should see a folder named: `llm-extension`.
5. Stop OpenRefine by **closing its window** (not just the browser tab).
6. Relaunch OpenRefine and wait for it to open in your browser.
7. Go to **Extensions** again. You should now see: `llm-extension` with **Bundled** set to `false`

If the extension does not appear, check that the folder name is exactly `llm-extension` and that it is directly inside the `extensions` directory.

### Installing Ollama (local LLM provider)

...

**Important:**  
- The AI extension sends your data to the configured provider.  
- You should only use providers that are appropriate for your data and comply with your institutional or project data policies.



:::::::::::::::::::::::::::::::::::::::: keypoints

- OpenRefine is a powerful, free and open source tool that can be used for data cleaning.
- OpenRefine will automatically track any steps you take in working with your data.

::::::::::::::::::::::::::::::::::::::::::::::::::



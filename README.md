# M3 Required Assignment: Exploratory Data Analysis

## Overview

This is the EDA assignment — one of the four required assignments in the course, and the one where you learn what exploratory data analysis is actually *for*.

Here's the framing, which we'll develop in class: **EDA is communication.** A good EDA notebook reads a newcomer into a dataset — a classmate, a stakeholder, or you in three months — without the newcomer having to open the data file or ask you anything. An AI can compute every plot in seconds. Deciding what's *salient for a reader*, and saying it clearly, is the part that's still entirely on you. That's the skill this assignment practices and the standard it's graded against.

You'll work with the Kaggle dataset you claimed at the end of Module 2. I don't know your dataset — that's deliberate. Your audience is real: your notebook has to do all the work of orienting me, because nothing else will.

This assignment spans two class weeks (Modules 3 and 4) and is designed to take about 4–6 hours total, including the in-class work time. If it's running much longer than that, let me know — that's useful information for me, not a failure on your part.

### What does successful work look like?

Your work should show that you can decide what a reader needs to know about a dataset and communicate it — in prose, tables, and plots that carry their own interpretation. Successful completion means a reader can answer every question in `eda-questions.md` using only your notebook. Your notebook runs top-to-bottom without errors, your analysis honestly says what the data can and cannot support, and your reflection shows real engagement with what you did and didn't understand. See **Evaluation Criteria** below for details.

## Learning Objectives

By the end of this assignment you should be able to:

- Orient a reader to an unfamiliar dataset: its provenance, structure, and scope — including what it *cannot* answer
- Choose and interpret the summaries, tables, and plots that make a dataset's important features visible, and describe distributions and relationships in words
- Assess data quality honestly: missingness, duplicates, suspicious encodings, and the difference between "verified complete" and "didn't check"
- Extend a general question set into a personal EDA guide tailored to a specific dataset

## Data

Your dataset is the Kaggle dataset you claimed in your section's claim thread at the end of Module 2. Download it from Kaggle and put it in this repository's directory.

Recall the eligibility rules from the claim assignment — your dataset must:

1. Have a Kaggle **usability score of 9.0 or higher** (this guarantees there's documented provenance to write about);
2. **Fail the AI-memorization test.** Ask your AI: *"Without looking anything up, can you tell me the columns of [dataset name] on Kaggle?"* If it answers from memory, the dataset is too famous — pick something else;
3. Be **unclaimed** by anyone else in your section (first post in the claim thread wins).

Anything loadable by name from `seaborn` or `sklearn` (titanic, iris, penguins, tips, diamonds, mpg, Boston/Ames housing) is banned regardless.

Beyond the hard rules, pick something with enough to write about: a mix of categorical and continuous variables, enough rows for distributions to have shape, and at least one honest wrinkle — skew, a weird encoding, suspicious duplicates. A perfectly clean, perfectly rectangular dataset makes for a boring EDA.

**Never commit data files to Git.** The `.gitignore` is set up to exclude them, but don't fight it — no data in the repo. Here is a [Reddit thread](https://www.reddit.com/r/mlops/comments/13s716f/give_me_one_good_reason_why_i_shouldnt_keep_my/) that describes some of the reasons not to commit your data. Since your data isn't in the repo, your notebook's prose and saved outputs have to do the communicating — which is the entire point.

## Tasks

Complete all work in the provided notebook (`eda.ipynb`). It gives you a loading scaffold and a section skeleton matching the question set — the structure is a starting point, not a cage. Reorganize if your dataset demands it.

### The question set is the shopping list

`eda-questions.md` holds the starter question set. A reader of your finished notebook should be able to answer **every question on that list** without opening the data file. That's the test your notebook has to pass — literally: in the Module 4 class, a classmate will try, using only what you wrote. Later, I will.

### Part 1: Provenance & structure

Who collected this data, how, and why? What does one row represent? What's the scope — and what tempting question can this data *not* answer? Then the honest quality audit: missingness (remember — "no missing values (verified)" is a claim you have to earn), duplicates, suspicious encodings, variables the author created or transformed.

### Part 2: Distributions & relationships

What does each key variable look like — shape, center, spread, outliers — *in words, not just plots*? What are the two or three most important relationships, shown and interpreted? What surprised you? Every table and plot gets a takeaway sentence; a figure without prose is homework you're assigning your reader.

### Part 3: Readiness & your personal question set

What would an analyst still have to do before running an analysis tomorrow? What analyses is this dataset ready to support? Finally: **extend the question set.** Add the dataset-specific questions a reader of *your* data would need answered — at least two, added to the end of your notebook and flagged as yours. This growing personal question set travels with you: you'll use it again in Module 6 and it becomes your EDA guide for the final project.

### How this gets evaluated: the reader test

In the Module 4 class, a randomly paired classmate reads your draft cold and reports what they could and couldn't answer. Their feedback is your revision roadmap. When you submit, I do the same thing with the final version. If your reader succeeds, your EDA works.

## Reflection

End your notebook with a short written reflection (a few paragraphs, Markdown). Address:

- What was confusing, and how did you resolve it?
- Where did AI help you most? Describe one suggestion you had to verify, correct, narrow, or reject, and how you checked it. If you did not use AI, explain how you found help and verified your work instead.
- What can you now explain or do without AI that you couldn't before starting?
- How long did it take? Any unresolved questions?

## Deliverables & Submission

When you have completed your work, **follow these steps carefully before submitting**. They're the same on every assignment.

### 1. Restart & Clear Outputs

In the notebook menu, select **Kernel → Restart & Clear Output**. This removes all generated output and resets the kernel.

### 2. Run everything top to bottom

Select **Run → Run All Cells**. Scroll through the notebook, looking for errors, checking that outputs appear as expected, and **reading your Markdown cells**. These cells should be polished and complete, just as you'd review an essay before submitting it. This step proves your notebook doesn't depend on out-of-order execution and that I'll see the same results you do.

### 3. Commit and push to GitHub

You can commit and push using the GUI tools in VS Code or at the command line. Your clone starts on the `work` branch — just commit and push as normal.

```bash
git add eda.ipynb
git commit -m "Ready for review"
git push
```

After your first successful push, use GitHub's **Compare & pull request** button to open one pull request from `work` into `main`. Then request **`37chandler`** as a reviewer using the **Reviewers** gear on the pull-request page; otherwise I will not be notified that your work is ready. Every later push updates that same pull request automatically, so pushing is how you submit. My feedback arrives as review comments there: **"Request changes"** means Needs Revision (push your fixes to `work` and the PR updates again); **approved and merged** means Complete. Do not open another pull request for revisions.

**Final checklist:**

- [ ] Kernel restarted and all outputs cleared
- [ ] All cells run successfully from top to bottom
- [ ] Every question in `eda-questions.md` answerable from the notebook alone
- [ ] Your dataset-specific questions added and answered
- [ ] Reflection written
- [ ] Changes committed and pushed — one `work` → `main` pull request is open and shows your latest commit
- [ ] `37chandler` requested as a reviewer on that pull request

## Working with AI

AI coding tools are allowed and expected in this course, from day one. You are not graded on hand-writing pandas; you are graded on asking the right statistical questions, verifying that the code does what you think it does, and interpreting results honestly.

Two rules of the road:

1. **You own every claim in your notebook.** "The AI wrote it" is not a defense of a wrong number, a mislabeled axis, or an overstated conclusion.
2. **Point your AI at `AGENTS.md`** in this repository. Agentic tools (Copilot agent mode, Cursor, Claude Code) will read it automatically; if you're using a chat tool, paste it in at the start. It tells your AI how to work with you so you actually learn something — small steps, checkpoints, no one-shot solutions.

For each substantial step, use a simple loop: **predict** what you expect to find, **run** one focused piece of code, **check** the result against the data or another calculation, and **explain** what it means for a reader. The reflection asks where AI helped and where a suggestion required verification or revision. Honest, specific answers there are part of the work.

## Evaluation Criteria

This rubric describes levels of understanding and skill demonstration. Use it for self-assessment and to understand feedback. Your work is evaluated holistically — this shows what I'm looking for at each facet.

### Code Functionality

**Exemplary**: The notebook executes flawlessly top to bottom. All required tasks are completed correctly, and the notebook shows evidence that you *verified* the code does what you claim — sanity checks, spot checks against raw data, or commentary that demonstrates you know what each step accomplished.

**Proficient**: Executes with only minor issues that don't prevent completion of major tasks. Most tasks correct; errors are minor and don't indicate fundamental misunderstanding.

**Developing**: Some execution errors or incomplete tasks. Core functionality present but unverified — code appears pasted-and-hoped rather than checked.

**Beginning**: Does not run or has major errors. Multiple required tasks missing or fundamentally incorrect.

### Analysis & Interpretation

**Exemplary**: Every analytical question is answered correctly with a clear, plain-English explanation supported by the data. Claims are disciplined — they say what the data support, no more. Uncertainty is acknowledged where it exists. Visualizations directly support conclusions.

**Proficient**: Most questions answered correctly; minor calculation or interpretation errors, but claims stay tethered to evidence. Visualizations present but less clearly tied to the analysis.

**Developing**: Some answers incorrect or incomplete; some claims overreach what the data support. Visualizations rudimentary or absent.

**Beginning**: Many questions unanswered or incorrect. Conclusions disconnected from output. Limited evidence of analytical thinking.

### Finished Product

**Exemplary**: The notebook reads like a document, not a scratchpad. Markdown cells organize the workflow and carry commentary; variable names are meaningful; formatting is clean; a reader can follow the analysis without you in the room.

**Proficient**: Generally clean and readable; minor inconsistencies that don't impede understanding.

**Developing**: Works, but readability suffers — unclear names, weak organization, sparse commentary.

**Beginning**: Difficult to read or follow. Minimal attention to presentation.

### Reflection

**Exemplary**: Specific and honest. Names actual points of confusion and how they were resolved; identifies concretely where AI helped and where a suggestion required verification, correction, narrowing, or rejection; articulates something learned. Reads like it could only have been written by someone who did *this* assignment.

**Proficient**: Addresses the prompts with some specificity; engagement is evident but some answers stay general.

**Developing**: Generic — could have been written before starting the assignment. Little evidence of engagement with the actual experience.

**Beginning**: Missing or perfunctory.

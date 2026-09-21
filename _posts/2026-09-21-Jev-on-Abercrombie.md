---
layout: post
title: Trying out TypeSafe's Jev on a legaltech benchmark
---

Last week (typesafe.ai) introduced Jev, a model designed to take textual prompts as input and produce structured output.
Jev is advertised as being faster and cheaper than other frontier models in this restricted environment.

A lot of my current responsibilities at my [day job](https://www.bloomberg.com/) involve evaluation and benchmarking of
[legal AI](https://pro.bloomberglaw.com/products/legal-research-and-software/legal-research/?trackingcode=BLAW22108720&utm_medium=referral&utm_source=mainblawlogin) systems. I thought I would give Jev a try on a published benchmark and see how it compares to a frontier model.

[LegalBench](https://hazyresearch.stanford.edu/legalbench/) is a collection of benchmarks designed to cover different
legal reasoning tasks. One of those tasks, [abercrombie](https://hazyresearch.stanford.edu/legalbench/tasks/abercrombie.html), requires classifying trademark names according to a schema outlined in the case *Abercrombie & Fitch Co. v. Hunting World, Inc.* (the following is a quote
from LegalBench's description of the benchmark):

* **Generic:** Generic terms are those which connote the basic nature of articles or services, rather than the more individualized characteristics of a product.
* **Descriptive:** Descriptive terms identify a characteristic or quality of an article or service, such as color, odor, function, dimensions, or ingredients.
* **Suggestive:** A suggestive term suggests, rather than describes, some particular characteristic of the goods or services to which it applies. It requires to consumer to exercise the imagination in order to draw a conclusion as to the nature of the goods and services.
* **Arbitrary:** Arbitrary terms are those that are real words, but arbitrary with respect to the product.
* **Fanciful:** Fanciful terms are those that are entirely made up, and not found in the English dictionary.

The associated dataset contains 99 examples of trademarks with correct classifications. For example, the correct label
for "The mark 'Pictures' for a photography service." is "generic".

I thought I would see how Jev does at this task, so I applied for (and pretty quickly received) a trial login, and set
up a Jupyter notebook to run the test cases through Jev and a couple of Claude models (Fable and Haiku 4.5, which a
Google search told me should be the fastest Anthropic model).  The results are in [this
repo](https://github.com/rkingan/typesafe-legaltech-spike); take a look at the Jupyter notebook
`abercrombie_benchmark.ipynb`.

## A few results and observations

* Jev was faster than the Anthropic models: Average latency was 0.20s for Jev, 0.73s for Haiku 4.5 and 3.05s for Fable.
* Jev was more accurate than Haiku but less than Fable: Haiku was 65.3%, Jev was 76.8%, Fable was 87.4%.
* Why didn't I try more frontier models? Laziness - I had my Anthropic key laying around.
* Are these speed comparisons conclusive? Maybe, maybe not. I did not use Anthropic's [fast
  mode](https://code.claude.com/docs/en/fast-mode). Also there's no accounting here for network speeds etc.
* What about cost? I didn't include any calculations, though the token counts should have been about the same.

Overall it looks like Jev is an interesting and potentially useful addition to the ML engineer's suite of tools.

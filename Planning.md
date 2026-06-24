## Community

I chose the Jujutsu Kaisen fan community because it contains a wide range of discussion styles including character analysis, power-scaling debates, emotional reactions, and meme-based agenda posting.

This makes it an ideal classification task because community members care about the distinction between evidence-based discussion and low-effort opinions. The discourse is active, varied, and highly opinionated, creating meaningful label boundaries.

Accuracy alone is insufficient because a model could achieve high accuracy by overpredicting the majority class.

I will evaluate:
- Accuracy
- Precision
- Recall
- F1-score for each label
- Confusion Matrix

F1-score is especially important because it balances precision and recall and shows whether the model truly learned each discourse category.

A successful classifier should achieve:

- 70%+ overall accuracy
- F1 score above 0.65 for most labels
- Comparable performance to a zero-shot Llama baseline while learning the discourse categories from a small labeled dataset

At this performance level the classifier would be useful as a moderation or discussion-quality analysis tool for the Jujutsu Kaisen community.

## AI Tool Plan

### Label Stress Testing
I will provide my label definitions to ChatGPT and ask it to generate borderline Jujutsu Kaisen posts that sit between labels.

### Annotation Assistance
I will use Claude to suggest labels for batches of comments, but I will manually review and correct every label before adding it to the dataset.

### Failure Analysis
After evaluation I will provide misclassified examples to ChatGPT and ask it to identify common error patterns. I will verify all suggested patterns myself before including them in the report.
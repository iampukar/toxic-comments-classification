## Description

    Discussing things you care about can be difficult. The threat of abuse and harassment online means that many people stop expressing themselves and give up on seeking different opinions. Platforms struggle to effectively facilitate conversations, leading many communities to limit or completely shut down user comments.

    The Conversation AI team, a research initiative founded by Jigsaw and Google (both a part of Alphabet) are working on tools to help improve online conversation. One area of focus is the study of negative online behaviors, like toxic comments (i.e. comments that are rude, disrespectful or otherwise likely to make someone leave a discussion). So far they’ve built a range of publicly available models served through the Perspective API, including toxicity. But the current models still make errors, and they don’t allow users to select which types of toxicity they’re interested in finding (e.g. some platforms may be fine with profanity, but not with other types of toxic content).

    In this competition, you’re challenged to build a multi-headed model that’s capable of detecting different types of of toxicity like threats, obscenity, insults, and identity-based hate better than Perspective’s current models. You’ll be using a dataset of comments from Wikipedia’s talk page edits. Improvements to the current model will hopefully help online discussion become more productive and respectful.

    Disclaimer: the dataset for this competition contains text that may be considered profane, vulgar, or offensive.


## Evaluation

    Update: Jan 30, 2018. Due to changes in the competition dataset, we have changed the evaluation metric of this competition.

    Submissions are now evaluated on the mean column-wise ROC AUC. In other words, the score is the average of the individual AUCs of each predicted column.

    Submission File
    For each id in the test set, you must predict a probability for each of the six possible types of comment toxicity (toxic, severe_toxic, obscene, threat, insult, identity_hate). The columns must be in the same order as shown below. The file should contain a header and have the following format:

    id,toxic,severe_toxic,obscene,threat,insult,identity_hate
    00001cee341fdb12,0.5,0.5,0.5,0.5,0.5,0.5
    0000247867823ef7,0.5,0.5,0.5,0.5,0.5,0.5
    etc.


## Leaderboard


    Public Leaderboard:
    Top: 0.9890
    My solution: 0.9817

    Private Leaderboard:
    Top: 0.9885
    My solution: 0.9801

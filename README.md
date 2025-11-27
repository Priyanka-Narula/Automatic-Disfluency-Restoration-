# Automatic-Disfluency-Restoration-
Challenge is to build a system that can predict the original, disfluent transcript from a clean text and its corresponding audio
🎧 Automatic Disfluency Restoration: Recreating the Nuance of Human Speech

This project addresses the challenging task of Automatic Disfluency Restoration, which sits at the intersection of Automatic Speech Recognition (ASR) and Natural Language Generation (NLG). The primary goal is to build a robust system that can predict the original, verbatim (disfluent) transcript from a given clean text and its corresponding audio recording.

This work requires models to understand not just what was said, but also how it was said, including the natural pauses, hesitations, and filler words that are an integral part of human communication.

The Core Technical Challenge

The underlying task is a multi-modal sequence-to-sequence prediction problem: taking the clean transcript and the audio signal as inputs to generate the full, disfluent transcript as output.

This emphasizes the following key areas:

Multi-modal Fusion: Developing an effective strategy to combine information from both the text (clean transcript) and the audio signal to make nuanced predictions.

Data Preprocessing as a Skill: The ability to programmatically create target training labels ("clean" transcripts) from raw, disfluent data using a provided list of common disfluencies. This skill is vital for success.

Model Selection and Fine-tuning: Choosing and fine-tuning appropriate models (e.g., ASR or sophisticated sequence-to-sequence architectures) capable of handling the complexities of spoken language, especially within limited computational resources.

Project Focus & Deliverables

This project is an exercise in practical deep learning skills, requiring participants to:

Design a robust data cleaning pipeline to map raw, disfluent transcripts to clean inputs, thus generating training labels.

Select and fine-tune appropriate models for this complex speech task.

Develop an end-to-end system that processes both audio and text to generate the final verbatim transcript.

🗃️ Dataset Description (Hindi Audio)

The dataset consists of audio clips in Hindi, their corresponding transcripts, and a list of common disfluencies. Your system must use the audio and a "clean" text input to predict the original, disfluent output.

Data Files Provided

train.csv: Contains labeled examples. The transcript column holds the disfluent ground truth. Note: You must create the "clean" training labels yourself.

test.csv: Contains the input for your predictions. The transcript column holds the clean text, with all disfluencies already removed.

unique_disfluencies.csv: A helper file containing a list of all unique disfluent words/phrases (e.g., "अं", "हम्म"). Use this to clean the training data.

downloaded_audios/: A directory containing all audio files in .wav format, named after the sample ID. This is the required multi-modal input.

Submission Format

You must submit a CSV file with exactly two columns: id and transcript. The transcript column should contain your model's predicted verbatim transcript (with disfluencies).

Evaluation Metric

The system is evaluated using the Word Error Rate (WER), the standard metric for assessing Automatic Speech Recognition systems.

Goal: To minimize the WER.

Lower is better (a score of 0.0 means a perfect prediction).

Scoring Formula:

$$\text{WER} = \frac{\text{Substitutions} + \text{Deletions} + \text{Insertions}}{\text{Number of Words in Reference}}$$

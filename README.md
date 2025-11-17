## Apache Beam Word Count Pipeline

This project implements a complete Apache Beam pipeline that reads a text dataset, extracts words, counts the frequency of each word using an alternative counting logic (`Count.PerElement()`), sorts the results, and stores them in an output file.

---

Project Overview

The objective of this project is to build a Word Count pipeline with **different logic** from the classic `(word, 1)` → `CombinePerKey(sum)` approach.  
This pipeline demonstrates:

- Reading a dataset using Apache Beam  
- Extracting words using regex  
- Counting words using `Count.PerElement()`  
- Sorting output inside Beam  
- Saving results to a `.txt` file  
- Maintaining the output format:


---

## Dataset

**File:** `world_events_dataset.txt`  
This dataset contains real-world global event summaries including:

- Climate news (COP30)
- Protests and political developments
- Conflict updates
- Economic and human rights reports
- Environmental issues

Each line represents one news item.

---

## Installation & Environment Setup

Install Apache Beam:

pip install apache-beam 

## Project Structure:

├── world_events_dataset.txt       # Input dataset
├── outputs-00000-of-00001.txt     # Auto-generated output file
├── README.md                      # Documentation file
└── notebook.ipynb                 # Apache Beam code implementation


## Key Apache Beam Concepts Used

1. Pipeline: Defines the workflow

2. PCollection: Distributed dataset

3. ReadFromText: Input source

4. FlatMap: Word extraction

5. Count.PerElement(): Alternative word counting logic

6. ToList: Combine results globally

7. WriteToText: Output sink

## How to Run

1. Run Cell 1 (Setup)

2. Run Cell 2 (Pipeline)

3. Check your working directory for:

   outputs-00000-of-00001.txt

## Conclusion

This project demonstrates a complete Apache Beam text-processing workflow using an alternative counting method. It processes real-world data, sorts and formats results, and exports them cleanly to a text file.

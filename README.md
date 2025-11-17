Apache Beam Word Count Pipeline

This project demonstrates how to build and run a Word Count data pipeline using Apache Beam (Python SDK).
The pipeline processes a text dataset containing current world events, counts word frequencies using a different logic (Count.PerElement()), sorts the results, and saves them to an output file.

* Project Overview

The pipeline performs the following steps:

1. Reads a text dataset (world_events_dataset.txt)

2. Extracts individual words using regex

3. Counts each unique word using Count.PerElement() (alternative logic to CombinePerKey)

4. Sorts words by their frequency in descending order

5. Saves the output into outputs.txt (Beam names it outputs-00000-of-00001.txt)

📁 Dataset

File: world_events_dataset.txt

Contains short news summaries about:

1. Climate events (COP30)

2. Conflicts and protests

3. Global politics

4. International relations

5. Environmental issues

6. Economic updates

7. Human rights reports

Each line represents one news item.

🛠️ Installation & Setup

1. Install Apache Beam:

pip install apache-beam


2. Optional (not required):

pip install "apache-beam[interactive]"

* Project Structure
├── world_events_dataset.txt       # Input data
├── outputs-00000-of-00001.txt     # Generated output file
├── README.md                      # Documentation
└── notebook.ipynb                 # Beam code (Jupyter Notebook)

* Key Apache Beam Concepts Used

1. Pipeline

2. PCollection

3. ReadFromText

4. FlatMap

5. Count.PerElement() (different logic)

6. ToList

7. Sorting inside Beam

8. WriteToText

* How to Run

1. Run Cell 1 to install Beam and set variables

2. Run Cell 2 to execute the pipeline

3. Check generated output file in your working directory

* Conclusion

This project demonstrates:

1. Building a complete Beam data processing pipeline

2. Using alternative logic (Count.PerElement) for word counting

3. Processing a real-world dataset

4. Sorting and formatting Beam output

5. Exporting results to a text file

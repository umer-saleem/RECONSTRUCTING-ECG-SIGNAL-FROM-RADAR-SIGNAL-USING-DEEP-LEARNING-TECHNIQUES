# Research Paper Relevance Finder
Overview

This project fetches recent publications from a Google Scholar author profile and identifies papers relevant to a given set of keywords using semantic similarity from a SentenceTransformer model.

The workflow:

Fetch recent publications using the author's Google Scholar ID.

Filter out papers without abstracts.

Compute similarity between keywords and paper abstracts/titles.

Return papers exceeding a given similarity threshold.

Save results into CSV files for further analysis.

Features

Fetches recent publications from Google Scholar.

Uses state-of-the-art semantic similarity to match papers to keywords.

Handles multiple keywords and provides per-paper matching scores.

Assigns unique IDs for papers per year for structured referencing.

Saves both full paper lists and filtered relevant papers as CSVs.

Requirements

You can install all dependencies by running:

pip install -r requirements.txt


Example requirements.txt:

pandas
tqdm
scholarly
sentence-transformers


Make sure you are using Python 3.8+ for compatibility.

Citation of the Transformer Model

This project uses the SentenceTransformer model:
Reimers, N., & Gurevych, I. (2019). Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks. Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing.
https://arxiv.org/abs/1908.10084

If you use this project or the underlying model in your work, please cite the above paper.

Project Structure
├── constants.py                  # Stores configuration values such as model name, author ID, keywords, etc.
├── main.py                        # Main script to fetch and process relevant papers
├── requirements.txt               # Python dependencies
├── research_papers_<AUTHOR>.csv   # All recent papers fetched (generated at runtime)
├── relevant_papers_<AUTHOR>.csv   # Relevant papers filtered by keyword similarity (generated at runtime)
└── README.txt                     # Documentation

Configuration

Edit the constants.py file to customize the behavior:
Example:

MODEL_NAME = "all-MiniLM-L6-v2"
AUTHOR_ID = "your_google_scholar_author_id"
YEARS_BACK = 5
KEYWORDS = ["remote sensing", "water quality", "machine learning"]
SIMILARITY_THRESHOLD = 0.5
START_YEAR = 2018
END_YEAR = 2024

Usage Instructions
1. Clone the Repository
git clone https://github.com/yourusername/research-paper-relevance-finder.git
cd research-paper-relevance-finder

2. Install Dependencies
pip install -r requirements.txt

3. Configure Parameters

Edit constants.py with:

MODEL_NAME: Name of the SentenceTransformer model.

AUTHOR_ID: The Google Scholar author ID (found in the profile URL).

YEARS_BACK: Number of years to go back for publications.

KEYWORDS: List of relevant keywords.

SIMILARITY_THRESHOLD: Value between 0 and 1 to control strictness.

Example Google Scholar author URL:

https://scholar.google.com/citations?user=abcd1234


Here, the AUTHOR_ID is abcd1234.

4. Run the Script
python main.py

Output

After running, two CSV files will be generated:

research_papers_<AUTHOR_ID>.csv – All fetched papers with metadata.

relevant_papers_<AUTHOR_ID>.csv – Filtered relevant papers based on similarity.

Each relevant paper entry includes:

title – Paper title.

abstract – Paper abstract.

year – Publication year.

similarity_score – Maximum similarity score among keywords.

keywords – Keywords matched.

url – Paper URL (if available).

title_id – Unique ID assigned for structured referencing.

Methods and Functionality
load_model(model_name)

Loads the SentenceTransformer model for encoding text.

find_relevant_papers(papers, keywords, similarity_threshold)

Finds papers with a similarity score above the threshold to any of the given keywords.

get_author_recent_papers_by_id(author_id, years_back)

Fetches recent publications for a given author from Google Scholar.

assign_unique_ids(df, years)

Assigns unique numeric IDs to papers per year based on occurrence frequency.

main()

Coordinates the entire workflow:

Fetch → Filter → Compute Similarities → Save Output.

Notes & Best Practices

Google Scholar scraping: The scholarly library fetches public data but can be rate-limited; use responsibly.

The similarity threshold controls filtering strictness:

Lower threshold → more results, possibly less relevant.

Higher threshold → fewer but more relevant results.

If you plan to work with large author profiles (hundreds of publications), expect longer runtime.

License

MIT License – Free to use and modify.

Do you want me to also make you a ready-to-use requirements.txt with exact package versions so users don’t face installation issues? That would make this repo completely plug-and-play.

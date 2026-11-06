# Financial Dataset Collection and Preparation Plan
**Project:** Multi-Agent Financial Research System (CSM-B12)
**Assigned Member:** Kusumuru Teja
**Project Guide:** Mr. M. Anil Kumar

## 1. Objective
To establish a verifiable dataset of financial documents and benchmark questions to evaluate our system's extraction accuracy and citation reliability.

## 2. Dataset Sources
* **Primary Benchmark:** FinanceBench (GitHub: `patronus-ai/financebench`). This provides over 10,000 question-answer pairs sourced directly from SEC filings.
* **Raw Documents:** 10-K and 8-K filings downloaded directly via the `sec-edgar-downloader` script to ensure we have the native text, not third-party summaries.

## 3. Dataset Validation & Structure
For every test case, we will record:
* **Question ID & Text:** (e.g., "What was the FY15 Net Income?")
* **Reference Answer & Source:** The exact ground-truth number and the specific PDF page number it came from.
* **Verification:** All benchmark answers will be manually verified against the original SEC PDF before testing our agents.

## 4. Evaluation Metrics (RAGAS)
We will use this dataset to measure the following metrics required for Review I:
* **Citation Faithfulness:** Does the generated answer match the retrieved text?
* **Extraction Accuracy:** Do the extracted financial numbers match the ground-truth dataset?
* **Context Precision:** Did the system retrieve the correct page?

## 5. Current Status & Next Steps
* **Status:** Dataset structure defined. No experimental results claimed yet.
* **Next Steps:** Clone the FinanceBench repository, extract 50 pilot questions, and download the corresponding SEC 10-K PDFs.
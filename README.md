# baymax_tc ✨
### An LLM application for summarization of Terms and Conditions agreements available on the internet. 

## Introduction 💡
Baymax_TC is an application designed to simplify complex Terms of Service agreements using the power of Large Language Models (LLMs). By leveraging RAG (Retrieval Augmented Generation), this application provides users with clear and concise explanations of legal jargon, making it easier to understand and comply with these often daunting documents.

## How it Works 🧲
- **Document Store:** The application maintains a repository of Terms of Service agreements from various platforms and services.
- **RAG:** When a user queries the application with a specific question or phrase related to a Terms of Service agreement, the RAG component searches the document store for relevant information.
- **LLM Processing**: The retrieved information is then processed by the LLM, which is trained to understand legal language and translate it into plain English.
- **Explanation Generation:** The LLM generates a comprehensive and easy-to-understand explanation of the query, addressing the user's specific concerns or questions.

## Key Features 📚
- **User-Friendly Interface:** A simple and intuitive interface allows users to easily input their queries and receive clear explanations.
- **Comprehensive Coverage:** The application covers a wide range of Terms of Service agreements, from popular social media platforms to online marketplaces.
- **Accurate and Reliable:** The LLM is trained on a vast dataset of legal documents, ensuring accurate and reliable explanations.
- **Customizable:** Users can customize the level of detail in the explanations to suit their needs and understanding.

## Getting Started 🔌
- **Installation:** Follow the installation instructions <Work In Progress>
- **Data Preparation:** Populate the document store with Terms of Service agreements in the desired format.
- **Usage:** Launch the application and start querying the Terms of Service agreements.

## Code Quality Tools🛠️

[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Imports: isort](https://img.shields.io/badge/%20imports-isort-%231674b1?style=flat&labelColor=ef8336)](https://pycqa.github.io/isort/)
[![Security: bandit](https://img.shields.io/badge/security-bandit-yellow.svg)](https://github.com/PyCQA/bandit)
[![Python 3.10.12](https://img.shields.io/badge/python-3.10.12-blue.svg)](https://www.python.org/downloads/release/python-31012/)

This project maintains high code quality standards through automated tools for formatting, style checking, and security analysis.

## Tools Overview 🔧

### Code Formatting and Style
- **[Black](https://black.readthedocs.io/)**: The uncompromising Python code formatter
  - Line length: 88 characters
  - Ensures consistent code style across the project
- **[isort](https://pycqa.github.io/isort/)**: Import statement organizer
  - Automatically formats and groups imports
  - Maintains consistent import ordering
- **[Bandit](https://bandit.readthedocs.io/)**: Security linter
  - Finds common security issues in Python code
  - Helps prevent security vulnerabilities

## Getting Started 🚀

### Installation

Install all development tools with pip:
```
  bash
  pip install black bandit isort pre-commit
  pre-commit install
```
### Usage
Check code without making changes:
```
  black --check .
  isort --check-only .
  bandit -r .
```
### Format Code
```
  black .
  isort .
```
### Pre-commit will run automatically on every commit, or manually:
```
  pre-commit run --all-files
```

### Configuration ⚙️ 
Tool settings are maintained in the following files:
| Tool | Configuration File | Use|
|------|-------------------|-----|
| Black & isort | `pyproject.toml` | Code formatting settings|
| Bandit | `.bandit` | Security check settings|
| Pre-commit | `.pre-commit-config.yaml` | Pre-commit hook settings|

### How to Run the Py Tests 🐍

1. **`q_a.json` file:** This file contains the question-answer pairs for evaluation.
2. **`evaluate_rag.py` script:** This script loads the data, generates answers using the language model, and then uses `deepeval` to calculate the three metrics.

* Correctness: How factually accurate are the answers?
* Faithfulness: How well do answers align with the information in the source document?
* Contextual Relevancy: How well do the answers address the specific question and its context within the source document?

### Python Version 🐍
- This project uses Python 3.10.12
- Dependencies listed in requirements.txt
  
### Troubleshooting 🔍
If any tool fails:
  - Run the tool manually (e.g., black . or isort .)
  - Stage changes: git add .
  - Try committing again

### A Simple Map For Organization

![alt text](<LLM Project (1).png>)
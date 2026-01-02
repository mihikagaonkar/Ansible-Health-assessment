# Markdown to Google Docs Converter

## Brief Description
This Python project is a specialized automation tool designed to convert raw Markdown formatted meeting notes into a polished, fully formatted Google Doc.

Built to run specifically within **Google Colab**, this script leverages the **Google Docs API** to programmatically generate documents. It goes beyond simple text insertion by mapping Markdown syntax to specific Google Docs structural elements and styles.

**Key Features:**
* **Header Mapping:** Converts Markdown headers (`#`, `##`, `###`) into Google Docs Heading styles (1, 2, 3).
* **Smart Lists:** Preserves nested bullet point hierarchies.
* **Interactive Elements:** Transforms Markdown checkboxes (`- [ ]`) into native Google Docs interactive checkboxes.
* **Styling:** Automatically highlights team member mentions (e.g., `@sarah`) in bold/color and formats footer metadata.

## Required Dependencies
The script relies on the official Google Client libraries for Python. These are installed dynamically within the notebook.

* `google-api-python-client`: To interact with the Docs API.
* `google-auth-httplib2`: For handling HTTP requests with authentication.
* `google-auth-oauthlib`: For handling OAuth 2.0 flows.
* `re` (Standard Library): For Regular Expression parsing of Markdown patterns.

## Setup Instructions

### Prerequisites
1.  A **Google Account**.
2.  Access to **Google Colab** (no local Python installation required).
3.  A destination Google Drive where the document will be created.

### Installation
No local installation is necessary. The script contains a cell to install the required packages within the Colab runtime environment:

```python
!pip install -q google-api-python-client google-auth-httplib2 google-auth-oauthlib

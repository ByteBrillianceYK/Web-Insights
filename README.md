# In-sights Chrome Extension

## Overview

In-sights is a Chrome extension designed to detect and highlight dark patterns on shopping websites. Dark patterns are design tricks used to influence the way users interact with software. While some dark patterns are harmless, like emphasizing signup buttons with color, others can be more malicious in problematic. In the context of online stores, dark patterns can be used to nudge buyers into buying items they might not need. For further information on dark patterns, check out this [website](https://www.darkpatterns.org/). Created by the man who coined the term ‘dark patterns,’ the site will teach you how to recognize the different kinds of dark patterns you may encounter.

## Features

- **Detection**: In-sights reads text on product pages and identifies potential dark patterns.
- **Highlighting**: Detected dark patterns are highlighted for easy identification.
- **Popup Explanation**: A popup provides information on the category of each detected dark pattern.

## Tech Stack

The Chrome Extension front-end that scrapes the active web page is written in Javascript. For the back-end, a Python server running Flask interfaces Bernoulli Naive Bayes models to classify tokens of text sent to it. To train these algorithms, datasets from Princeton University researchers along with manually annotated datasets were used.

## Installation

To begin installation, first clone this repository, or download and unzip it.

1. Install and run the Flask app backend by navigating to `api`, installing required libraries, and running `app.py` with Python.

2. Install the Chrome extension:
   - Navigate to `chrome://extensions`.
   - Enable "Developer mode" by toggling the switch at the top right of the page.
   - Click the "Load unpacked" button.
   - Navigate to the repository directory, and select the folder `app` for installation.
   - Ensure that the extension is enabled, and if so, the extension has been successfully installed!

## Acknowledgements

This project was inspired by the paper *Dark Patterns at Scale: Findings from a Crawl of 11K Shopping Websites* by Mathur et al. We are immensely grateful for their dataset of dark pattern strings, which was instrumental in training our classifier. Additionally, their page segmentation algorithm was crucial in breaking down webpages into meaningful blocks of text for analysis.

## Awards

We are proud to announce that In-sights won first prize at the NIRMAN HACKATHON. [Here](https://www.linkedin.com/feed/update/urn:li:activity:7033313964356771840/) is the link to the announcement post.

## Reference

Mathur, A., Acar, G., Friedman, M. J., Lucherini, E., Mayer, J., Chetty, M., & Narayanan, A. (2019). Dark Patterns at Scale: Findings from a Crawl of 11K Shopping Websites. Proceedings of the ACM on Human-Computer Interaction, 3(CSCW), 81.

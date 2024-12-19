# PLOS_ntds
### This dataset is collected from the [Journal Archive](https://journals.plos.org/plosntds/volume) section of [PLOS Neglected Tropical Disease](https://journals.plos.org/plosntds/). 

#### According to [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/), articles from PLOS are legally available for reuse, without permission or fees. Anyone may copy, distribute, or reuse these articles, as long as the author and original source are properly cited.

#### [See more on PLOS](https://journals.plos.org/plosntds/s/journal-information#loc-open-access)

---

The PLOS_ntds dataset exclusively comprises 10100 pieces of research articles from PLOS Neglected Tropical Diseases. It captures various components of each article, including the abstract, article content, author summary, acknowledgements, and other features. Below is a sample structure for one article:
```
- 10.1371
    - 2024
        - January
            - journal.pntd.0011369
            - journal.pntd.0011678
                - src
                - abstract.json
                - acknowledgments.txt
                - article_features.json
                - author_summary.txt
                - content.json
                - figure_table.json
```

Each article is identified by its DOI number, used as the `file name`. 

The `src` folder contains the original PDF file. Figures and tables, downloaded as TIFF files, are also stored in this folder. (disabled)

`figure_table.json` describes each figure and table downloaded into the `src` folder.

`article_features.json` provides basic details for each article, including the URL, publication date, subject areas, authors, and their affiliations.

`abstract.json` contains the abstract, organized with each subsection name as the dictionary key and the corresponding text as the value. If the abstract has no subsections, the key is labeled "Abstract".

`content.json` includes the main article content, with each section name as the dictionary key and the text as the value.

`acknowledgements.txt` and `author_summary.txt` contain the text data for each corresponding section.


---

`crawler.py` provides a python script for establishing this dataset. Crawling figures and pdfs is disabled due to the limitation of disk space.

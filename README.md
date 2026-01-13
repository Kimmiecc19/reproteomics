# The Crisis of Proteomics Reproducibility - A Bioinformatics Perspective

## Abstract

<p align="justify">
The lack of reproducibility in proteomics analyses, when viewed from a bioinformatics perspective, is a multifaceted issue stemming from several related challenges. A primary challenge is the inherent complexity and variability in proteomic datasets. Furthermore, the absence of standardized protocols and analysis pipelines across different laboratories and research groups compounds this problem, resulting in inconsistent practices and results. This review sets out to identify the primary obstacles and underlying causes contributing to the reproducibility crisis in proteomics analyses from a bioinformatics standpoint, while also exploring potential solutions. The review introduces a novel approach to assessing the reproducibility of proteomics data analysis tools. It involves evaluating key factors like documentation, version control, maintenance and community engagement employed by these tools and rating them on a scale of one to three, with three showing the greatest reproducibility. By scrutinizing these elements, developers can pinpoint areas requiring improvement and implement best practices to enhance reproducibility. Alternatively, users can select tools that are more likely to be reproducible for their analyses. This will hopefully facilitate the development of community-driven standards and guidelines for proteomics data analysis. Overall, we show that there is a reproducibility crisis in protein bioinformatics analyses, however, there are several solutions in play to improve this and the field will continue to develop. As it develops, it is essential to prioritize reproducibility and work towards establishing standardized protocols and guidelines for proteomics data analysis.
</p>

## Filtering Criteria for Proteomics Tools from Bio.tools Registry

<div align="center">
  <img src="https://github.com/omicscodeathon/reproteomics/blob/main/figures/reproproteo_filter_April2025.png" alt="Filtering results" width="600"/>
</div>

## How to Reproduce This Study

### Steps

<p align="justify">
1. Fetch the bio.tools metadata using keyword/s of interest using <code>fetch_biotools.py</code> (V1 or V2). If using multiple terms, separate each term by a comma (e.g., <code>protein,peptide,PPI</code>). The Python script saves the file in JSON format.
</p>

<p align="justify">
2. Convert the JSON file to a TSV file using <code>json2tsv.py</code> (V1 or V2).
</p>

<p align="justify">
3. Filter the TSV file using <code>filter_biotools.R</code> (V1 or V2). You can adjust any of the filtering steps for your specific use.
</p>

<p align="justify">
4. Manually go through your tools and score each one using the criteria (<code>reproteomics/output/scoring_criteria.pdf</code>). Use the exact descriptions given in the table to ensure that there are no issues with the scoring.
</p>

<p align="justify">
5. Score the filtered tool table using <code>scoring_tools.R</code>. These scores are based on the ten criteria associated with reproducibility.
</p>

## Differences Between Version 1 vs. Version 2 of Scripts

| Script | Version 1 | Version 2 |
|--------|-----------|----------|
| `fetch_biotools.py` | Does not extract citation information | Extracts citation information based on publications listed in bio.tools |
| `json2tsv.py` | Does not include citation information | Includes citation information |
| `filter_biotools.py` | Does not filter citations | Filters citations | 

## Team Members

**Coetzer, K.C<sup>(1)</sup>, Aidoo, A.S<sup>(2)</sup>, Adomako N.A<sup>(1,4)</sup>, Ajiboye, I.O<sup>(5,6)</sup>, Nortey H.<sup>(3)</sup>, Okello, O.I<sup>(7)</sup>, and Awe, O.I<sup>(8)</sup>**

<p align="justify">
1. Department of Biomedical Sciences, Division of Molecular Biology and Human Genetics, Stellenbosch University, Cape Town, South Africa
</p>

<p align="justify">
2. Department of Virology, Noguchi Memorial Institute for Medical Research, College of Health Sciences, University of Ghana, Legon, Accra, Ghana
</p>

<p align="justify">
3. Department of Clinical Pathology, Noguchi Memorial Institute for Medical Research, College of Health Sciences, University of Ghana, Legon, Accra, Ghana
</p>

<p align="justify">
4. Department of Molecular Medicine, School of Medicine and Dentistry, Kwame Nkrumah University of Science and Technology, Kumasi, Ghana
</p>

<p align="justify">
5. Covenant Applied Informatics and Communication Africa Centre of Excellence (CApIC-ACE), Covenant University, Ota, Nigeria
</p>

<p align="justify">
6. Department of Computer and Information Sciences, College of Science and Technology, Covenant University, Ota, Nigeria
</p>

<p align="justify">
7. Department of Immunology and Molecular Biology, College of Health Sciences, School of Biomedical Sciences, Makerere University, Kampala, Uganda
</p>

<p align="justify">
8. African Society for Bioinformatics and Computational Biology, Cape Town, South Africa
</p>

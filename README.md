MOVIE DATABASE: https://drive.google.com/file/d/1X2WAngDM85mX1tfxqh4Nv1wfyZbzfWfM/view?usp=sharing

# Exploring Rocchio Algorithm for Query Refinement in Movie Retrieval

## Overview

This project expands the scope of movie retrieval experiments by introducing Rocchio's algorithm for query refinement. The study evaluates its performance against baseline TF-IDF results using a dataset of over 10,000 movies, encompassing diverse genres. By incorporating human feedback and parameter tuning, the project aims to enhance precision for specific queries.

---

## Dataset Expansion

To reach a dataset size of 10,000+ movies, we added films across multiple genres released after 1900. Genres included:
- **Thriller**
- **Comedy**
- **Drama**
- **Science Fiction/Sci-Fi**
- **Adventure**
- **Western**
- **Biographic**
- **Crime**
- **Silent Sports**

These genres were chosen based on their consistent yearly releases and ability to cover subgenres (e.g., romantic comedies).

---

## Queries

The following queries were tested:
1. **Inspiring Pirate Adventure**
2. **Depressing Ghost Story**
3. **Romantic Comedy High School**

---

## Rocchio Algorithm

### Methodology
1. **Baseline Comparison:**
   - TF-IDF precision:
     - Pirate: 5/7
     - Ghost: 6/7
     - Rom-Com: 1/7
2. **Parameter Tuning:**
   - Hyperparameters: 
     - \( \beta \) (positive feedback): 0.1 to 1.
     - \( \gamma \) (negative feedback): 0.1 or lower.
   - Epochs: Multiple runs were conducted to identify trends.
3. **Performance:**
   - Best precision for Pirate and Ghost queries:
     - 2/3, 5/6, 6/7 over four trials (1, 6, 17, and 21).
   - Rom-Com query:
     - Precision improved in only one trial (trial 1).

### Observations
- Rocchio outperformed standalone TF-IDF by incorporating feedback, enabling query refinement.
- The Pirate and Ghost queries benefited significantly, while the Rom-Com query remained challenging.

---

## Query Alterations with Synonyms

### Approach
- Used **Wordhoard** to suggest synonyms for queries.
- New queries were fed into the model using the best hyperparameters.

### Results
- Synonym-based queries often reduced performance.
- Insights:
  - Synonyms can shift the focus of a query, affecting connotation and original intent.
  - Query specificity and context are critical for effective retrieval.

---

## Conclusions

- **Rocchio Algorithm:** Demonstrated superior performance over TF-IDF for integrating human feedback into the retrieval process.
- **Query Alterations:** Synonym-based modifications should be approached cautiously, as they can detract from query intent.
- **Future Work:** Further exploration of Rom-Com queries could involve broader dataset enhancements or specialized models for niche genres.

---

## Code and Results

Detailed implementations and results are available in the accompanying notebook `Rocchio.ipynb`.

---

## Questions?

Feel free to reach out for additional details or collaboration opportunities.

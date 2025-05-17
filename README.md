
# Annotation Error Detection in the LeNER-Br Dataset using Cleanlab

This repository contains a Jupyter notebook that applies *Confident Learning* techniques, via the [cleanlab](https://cleanlab.io/) library, to identify annotation errors in the [LeNER-Br](https://teodecampos.github.io/LeNER-Br/) dataset, a resource designed for Named Entity Recognition (NER) tasks in Brazilian Portuguese.

## 📘 About the Project

The goal of this project is to support data quality auditing and enhancement in manually annotated datasets for NER. By leveraging predicted probabilities from a pre-trained model, we automatically detect tokens that are likely to have been mislabeled during manual annotation.

The analysis successfully identified multiple annotation inconsistencies, such as legal expressions and case references mislabeled as geographic locations.

## 🧪 Technologies Used

- Python 3.10+
- [cleanlab](https://github.com/cleanlab/cleanlab)
- scikit-learn
- NumPy / Pandas
- Matplotlib
- Jupyter Notebook

## 📁 Project Structure

```
├── aed_lener_br_conclusao.ipynb     # Main notebook with annotation error analysis
├── data/
│   ├── train.conll                  # LeNER-Br training file
│   └── test.conll                   # LeNER-Br test file
├── README.md
```

## 📊 Workflow Overview

1. Convert `.conll` files into BIO tagging format.
2. Train a simple NER model.
3. Generate prediction probabilities for each token.
4. Use `cleanlab.find_label_issues` to identify potential labeling mistakes.
5. Visualize and analyze the top-ranked suspicious tokens.
6. Discuss false positives and improvement strategies.

## 📌 Conclusion

*Confident Learning* has proven to be an effective approach to detecting inconsistencies in the original LeNER-Br labels. The method enables more efficient dataset auditing by prioritizing cases with high error likelihood. As a next step, we recommend using automated or semi-automated *retagging* techniques to correct the identified labels, starting with the model’s high-confidence suggestions.

## 📄 License

This project is licensed under the MIT License.

## 👨‍💻 Author

**Eduardo P. Lima**  
MSc Student in Artificial Intelligence | Data Scientist

---

Feel free to contribute, suggest improvements, or report any issues.

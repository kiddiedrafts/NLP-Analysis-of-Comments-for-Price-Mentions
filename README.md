# Comment Mining using NLP

This project utilizes Natural Language Processing (NLP) to analyze user comments from the Digikala website, aiming to predict whether a comment mentions the price of a product. The implementation employs the Naive Bayes algorithm for classification, leveraging effective text preprocessing techniques.

## Dataset

The dataset comprises user comments collected from the Digikala website. Each comment is labeled based on whether it references product pricing. We have access to 40,000 labeled comments.

**Note:** The dataset is proprietary, and thus, its publication is not permitted.


| Column       | Description                                               |
|--------------|-----------------------------------------------------------|
| comment      | The text of the user comment                             |
| price_value  | Indicates whether the comment discusses price (1) or not (0) |

## Text Preprocessing
- **Removing Stop Words**: Certain frequently occurring words carry little meaning and can be removed to enhance model performance.
- **Removing Numbers and Extraneous Characters**: Numbers and extra characters that do not add value may also be excluded.
- **Normalization**: Ensuring consistency in text formatting, such as handling diacritics in Persian.
- **Stemming**: Reducing words to their base form to treat variations as the same word.

The project utilizes the `hazm` library for Persian text preprocessing, which provides tools for normalization, stemming, and retrieving a list of stop words.

## Model Training
The Naive Bayes algorithm, a probabilistic classifier based on Bayes' theorem, has been employed to build the model. This approach estimates the likelihood of a comment belonging to a specific class (mentioning price or not) by analyzing the frequencies of words in the training data. The model calculates prior probabilities and the conditional probabilities of the features, enabling it to predict the class of new comments effectively.

## Model Performance
The model achieved the following accuracy:
- **Training Set:** 0.8950
- **Test Set:** 0.8325

## Requirements
To run this project, you'll need the following Python libraries:
- `numpy`
- `pandas`
- `hazm`
- `re`
- `scikit-learn`

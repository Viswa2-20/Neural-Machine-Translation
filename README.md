# Neural Machine Translation with Attention

This project implements a Neural Machine Translation (NMT) model with an attention mechanism to translate dates from natural language format to a standardized machine-readable format (YYYY-MM-DD). The project is built using TensorFlow and Keras.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Model](#model)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview

Neural Machine Translation (NMT) is an approach to automate translation between languages using deep learning techniques. The project showcases the use of Seq2Seq models with an attention mechanism to translate various date formats. The model learns to convert dates like "5 April 09" or "Saturday May 9 2018" into the format "YYYY-MM-DD."

The attention mechanism allows the model to focus on specific words in the input sequence that are relevant to the current output word, improving the overall performance and accuracy.

## Dataset

The dataset consists of a set of dates in different textual formats paired with their corresponding machine-readable formats. These formats are converted into vocabulary sets for model training.

- **Input format examples:** "3 May 1979", "21th of August 2016"
- **Target format:** "YYYY-MM-DD"

## Model

The NMT model uses an encoder-decoder architecture with attention. 

- **Encoder:** Processes the input sequence (date in textual form) and converts it into a fixed-size context vector.
- **Attention Mechanism:** Helps the decoder to focus on different parts of the input sequence during the translation.
- **Decoder:** Generates the output sequence (the machine-readable date) based on the context vector and attention weights.

Key layers used:
- Bidirectional LSTM
- Attention layers
- Dense layers

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-repo/nmt-with-attention.git
    ```

2. Install the necessary packages:

    ```bash
    pip install -r requirements.txt
    ```

3. Download the pre-trained model weights if available or train the model from scratch using the notebook.

## Usage

1. **Training the model:**
   You can train the model using the provided dataset by running the notebook. Make sure to preprocess the data using the `preprocess_data` function.

2. **Running predictions:**
   Once the model is trained, you can provide a date in natural language format for translation:

   ```python
   EXAMPLES = ['3 May 1979', '5 April 09', '21th of August 2016']
   for example in EXAMPLES:
       predict(example)


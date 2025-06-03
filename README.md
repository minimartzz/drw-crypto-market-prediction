<div align="center">

  <img src="assets/header.png" alt="logo" width="300" height="auto" />
  <h1>Kaggle: DRW - Crypto Market Prediction</h1>
  
  <p>
    Build a model capable of predicting short-term crypto future price movements using our production feature data alongside publicly available market volume statistics
  </p>

</div>

<br />

<!-- Badges -->

## Tools

![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white)

---

<br />

<!-- Table of Contents -->

# :notebook_with_decorative_cover: Table of Contents

- [About the Project](#star2-about-the-project)
- [Details on Data](#bookmark_tabs-details-on-data)
- [Contact](#handshake-contact)
- [Acknowledgements](#gem-acknowledgements)

<!-- About the Project -->

## :star2: About the Project

Build a model capable of predicting short-term crypto future price movements using our production feature data alongside publicly available market volume statistics. The proprietary production features we provide are integral to our trading strategies, capturing subtle market signals that help us navigate and seize opportunities in real time. Moreover, these production features, combined with public data describing the broader market state, create a rich and challenging dataset for data mining and modeling. The task is to integrate these diverse sources of information into a single directional signal that effectively predicts crypto future price movements.

## :bookmark_tabs: Details on Data

The dataset comprises minute-level historical data for the crypto market. Goal is to predict future crypto market price movements.

### train.parquet

`timestamp`: The timestamp index representing the minute associated with each row.
`bid_qty`: The total quantity buyers are willing to purchase at the best (highest) bid price at the given timestamp.
`ask_qty`: The total quantity sellers are offering to sell at the best (lowest) ask price at the given timestamp.
`buy_qty`: The total trading quantity executed at the best ask price during the given minute.
`sell_qty`: The total trading quantity executed at the best bid price during the given minute.
volume: The total traded volume during the minute.
`X_{1,...,890}`: A set of anonymized market features derived from proprietary data sources.
`label`: The target variable representing the anonymized market price movement to be predicted.

### test.parquet

The test dataset has the same feature structure as train.parquet, with the following differences:

`timestamp`: To prevent future peeking, all timestamps are masked, shuffled, and replaced with a unique ID.
`label`: All labels in the test set are set to 0.

## :handshake: Contact

Author: Martin Ho

Project Link: []()

<!-- Acknowledgments -->

## :gem: Acknowledgements

- [Kaggle competition page](https://www.kaggle.com/competitions/drw-crypto-market-prediction/data)

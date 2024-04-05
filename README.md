# Dataset14_FinancialFraudDetection

## Introduction

This dataset presents a synthetic representation of mobile money transactions, meticulously crafted to mirror the complexities of real-world financial activities while integrating fraudulent behaviors for research purposes. Derived from a simulator named PaySim, which utilizes aggregated data from actual financial logs of a mobile money service in an African country, this dataset aims to fill the gap in publicly available financial datasets for fraud detection studies. It encompasses a variety of transaction types including CASH-IN, CASH-OUT, DEBIT, PAYMENT, and TRANSFER over a simulated period of 30 days, providing a comprehensive environment for evaluating fraud detection methodologies. By addressing the intrinsic privacy concerns associated with financial transactions, this dataset offers a unique resource for researchers and analysts in the field of financial security and fraud detection, scaled to 1/4 of the original dataset size for efficient use within the Kaggle platform. Please note that transactions marked as fraudulent have been nullified, emphasizing the importance of non-balance columns for fraud analysis. This dataset is a contribution to the field from the "Scalable resource-efficient systems for big data analytics" project, funded by the Knowledge Foundation in Sweden.

## Dataset Details

PaySim synthesizes mobile money transactions using data derived from a month's worth of financial logs from a mobile money service operating in an African country. These logs were provided by a multinational company that offers this financial service across more than 14 countries globally.

This synthetic dataset has been scaled to one-quarter the size of the original dataset and is specifically tailored for Kaggle.

**Important Note:** Transactions identified as fraudulent are annulled. Hence, for fraud detection analysis, the following columns should not be utilized: oldbalanceOrg, newbalanceOrig, oldbalanceDest, newbalanceDest.

## Dataset Structure

- `step`: Represents a unit of time in the real world, with 1 step equating to 1 hour. The total simulation spans 744 steps, equivalent to 30 days.
- `type`: Transaction types include CASH-IN, CASH-OUT, DEBIT, PAYMENT, and TRANSFER.
- `amount`: The transaction amount in the local currency.
- `nameOrig`: The customer initiating the transaction.
- `oldbalanceOrg`: The initial balance before the transaction.
- `newbalanceOrig`: The new balance after the transaction.
- `nameDest`: The transaction's recipient customer.
- `oldbalanceDest`: The initial recipient's balance before the transaction. Not applicable for customers identified by 'M' (Merchants).
- `newbalanceDest`: The new recipient's balance after the transaction. Not applicable for 'M' (Merchants).
- `isFraud`: Identifies transactions conducted by fraudulent agents aiming to deplete customer accounts through transfers and cash-outs.
- `isFlaggedFraud`: Flags large-scale, unauthorized transfers between accounts, with any single transaction exceeding 200,000 being considered illegal.

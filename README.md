
# AML Transaction Dataset

## Overview
This AML Transaction Dataset contains 5,000 unique transaction records, each labeled to indicate whether the transaction is suspected of money laundering. The dataset is intended for developing and benchmarking transaction monitoring and classification approaches in Anti-Money Laundering (AML) systems.

## Dataset Structure
The dataset is provided as a CSV file and includes the following columns:

| Column Name               | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| Date                      | Date of the transaction (YYYY-MM-DD)                                         |
| Time                      | Time of the transaction (HH:MM)                                              |
| Sender_account            | Unique identifier of the sender's account                                    |
| Receiver_account          | Unique identifier of the receiver's account                                  |
| Amount                    | Monetary amount of the transaction                                           |
| Payment_currency          | Currency code used by the sender                                             |
| Received_currency         | Currency code received by the receiver                                       |
| Sender_bank_location      | Geographic location of the sender's bank                                     |
| Receiver_bank_location    | Geographic location of the receiver's bank                                   |
| Payment_type              | Mode of payment (e.g., Credit Card, Cash, ACH Transfer, Cross-Border, etc.)  |
| Is_laundering             | Binary label indicating suspicion: 1 = suspicious, 0 = normal                |
| Laundering_type           | Transaction typology (e.g., Normal_Personal_Transfer, Suspicious_Structuring) |

## Usage
1. **Load the data**  
   ```python
   import pandas as pd
   df = pd.read_csv('aml_full_synthetic_dataset.csv')
   ```

2. **Explore the data**  
   ```python
   print(df.head())
   print(df['Is_laundering'].value_counts())
   ```

3. **Train a classifier**  
   - Perform preprocessing (e.g., encoding, scaling).  
   - Split into training and test sets.  
   - Fit models (e.g., SVM, Random Forest, LSTM, Transformer).  
   - Evaluate using metrics such as accuracy, precision, recall, AUC.

## Citation
If you use this dataset in your research, please cite the following work:
```
B. Öztas, D. Cetinkaya, F. Adedoyin, M. Budka, H. Dogan, and G. Aksu, 
"Enhancing Anti-Money Laundering: Development of a Synthetic Transaction Monitoring Dataset," 
2023 IEEE International Conference on e-Business Engineering (ICEBE), Sydney, Australia, 2023, 
pp. 47-54, doi:10.1109/ICEBE59045.2023.00028.
```

## License
Please check associated licensing terms provided by the dataset authors before distribution.

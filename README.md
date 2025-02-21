# Second AN2DL Challenge Report

## Description
This project focuses on developing a time series forecasting model capable of predicting several uncorrelated time series with strong generalization capabilities. The challenge is to build a model that predicts future values beyond specific time domains.

## Problem Statement
The task is to develop a forecasting model that can transcend specific time contexts. The model should predict 9 future values in the first phase and 18 future values in the second phase.

## Building the Sequences
- Transformed the dataset from a numpy array to a dataframe for better usability.
- Displayed time series by category.
- Created hopping time windows, which impacted model performance.
- The optimal window size was set to 200, excluding series shorter than this length.
- The best stride was determined to be 10.

## Model Design
### RNN (Recurrent Neural Network)
- Built a simple RNN with bidirectional GRU units (64 units).

### Transformer-Based Architecture
- Researched and adapted transformer-like architectures.
- Created a decoder network with positional embedding and transformer decoders.

### Hybrid Architecture: RNN + Attention Layer
- Combined RNN features with an Attention Layer.

### Autoregressive Prediction Model
- Used autoregression for the second phase to predict the next 9 values iteratively.

## Conclusion
- The transformer-based model performed better for predictions farther in time.
- Potential improvements include optimizing the time embedding procedure, experimenting with different sequence-building algorithms, and adjusting transformer parameters to reduce overfitting.

## Results
| Model             | First Phase MSE | Second Phase MSE |
|-------------------|-----------------|------------------|
| GRU (64 units)    | -               | 0.0056           |
| Transformers      | 0.0132          | 0.0067           |
| Hybrid Architecture | 0.0108         | -                |

## Contributions
- Francesco Ferrari: Transformer-based models
- Luca Bresciani: Dataset inspection and representation
- Francesco Pastori: Sequence building and GRU models
- Roberto Cialini: GRU and LSTM models

## References
- Notebook: “GRU dev.ipynb”
- Notebook: “Transformer dev.ipynb”
- Notebook: “Hybrid dev.ipynb”

## License
Information about the project's license.

## Acknowledgments
- Francesco Ferrari
- Roberto Cialini
- Luca Bresciani
- Francesco Pastori


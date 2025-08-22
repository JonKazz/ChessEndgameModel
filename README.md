# Chess Endgame Model - King+Rook vs King

A machine learning model that predicts the minimum number of moves required to achieve checkmate in King+Rook vs King chess endgames using LightGBM.

## Project Overview

This model analyzes chess endgame positions where one player has a King and Rook against an opponent with just a King. The goal is to predict the minimum number of moves required to achieve checkmate.

## Model Performance

The model achieves **97.65% accuracy** in predicting minimum moves to win, as measured by:
- **5-fold stratified cross-validation**
- **Macro F1-score average**

This evaluation method ensures the model's performance is consistent across different data splits and maintains high accuracy across all move count categories.

## Technical Details

- **Algorithm**: LightGBM (Light Gradient Boosting Machine)
- **Features**: Chess position characteristics and board state
- **Evaluation**: Stratified K-fold cross-validation to handle class imbalance
- **Metrics**: Classification accuracy and macro F1-score

## Files

- `krkhw2.ipynb` - Jupyter notebook containing the model implementation and analysis
- `king_rook_vs_king.csv` - Dataset of chess endgame positions
- `requirements.txt` - Python dependencies

## Usage

1. Install dependencies: `pip install -r requirements.txt`
2. Open `krkhw2.ipynb` in Jupyter
3. Run the notebook to train and evaluate the model

## Chess Endgame Context

The King+Rook vs King endgame is one of the fundamental checkmate patterns in chess. While it's theoretically a win for the side with the rook, the number of moves required can vary significantly based on the initial position. This model helps identify the most efficient path to victory.

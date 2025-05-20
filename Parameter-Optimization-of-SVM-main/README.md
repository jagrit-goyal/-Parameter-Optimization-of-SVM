# SVM Optimization Experiment

## Overview
This repository contains an implementation of a Support Vector Machine (SVM) optimization experiment for multi-class classification. The experiment uses a synthetic dataset to evaluate SVM performance across multiple samples with different parameters.

## Features
- Generation of synthetic multi-class dataset with 5000 samples and 10 features
- Automated SVM hyperparameter optimization
- Multiple sample evaluation (10 different train/test splits)
- Comprehensive visualization of results
- Detailed performance metrics and convergence analysis

## Dataset
The experiment uses a synthetic dataset with the following properties:
- 5000 samples
- 10 features (7 informative, 3 redundant)
- 5 classes with equal distribution
- Standardized preprocessing

## Methodology
1. A synthetic multi-class dataset is generated using scikit-learn's `make_classification`
2. Basic exploratory data analysis is performed (class distribution, feature statistics, correlations)
3. The dataset is split into 10 different train/test samples (70%/30% split)
4. For each sample, SVM optimization is performed with various kernel configurations:
   - Linear kernel with different C values (0.1, 1.0, 10.0)
   - RBF kernel with different C values and gamma parameters
5. Accuracy is tracked across iterations to generate convergence history
6. Results are compiled and visualized

## Results
The experiment identified optimal SVM parameters across 10 different samples:

| Sample | Best Accuracy | Best SVM Parameters  |
|--------|---------------|---------------------|
| S1     | 0.836         | rbf, 1.000, 0.100   |
| S2     | 0.844         | rbf, 1.000, 0.100   |
| S3     | 0.832         | rbf, 1.000, 0.100   |
| S4     | 0.845         | rbf, 1.000, 0.100   |
| S5     | 0.842         | rbf, 1.000, 0.100   |
| S6     | 0.851         | rbf, 1.000, 0.100   |
| S7     | 0.842         | rbf, 1.000, 0.100   |
| S8     | 0.839         | rbf, 1.000, 0.100   |
| S9     | 0.843         | rbf, 1.000, 0.100   |
| S10    | 0.849         | rbf, 1.000, 0.100   |

The best overall performance was achieved with Sample S6, reaching an accuracy of 85.1% using an RBF kernel with C=1.0 and gamma=0.1.

## Visualizations
The experiment generates several visualizations:
- Convergence graph for the best-performing SVM
- Class distribution visualization
- Feature correlation heatmap

## Dependencies
- Python 3.x
- NumPy
- pandas
- scikit-learn
- Matplotlib
- seaborn

## Usage
```python
# Clone the repository
git clone https://github.com/yourusername/svm-optimization-experiment.git
cd svm-optimization-experiment

# Install dependencies
pip install -r requirements.txt

# Run the experiment
python svm_experiment.py
```

## Output Files
- `svm_optimization_results.csv`: Complete results table
- `best_svm_convergence.png`: Convergence graph for the best SVM
- `class_distribution.png`: Visualization of class distribution
- `feature_correlation.png`: Heatmap of feature correlations

## License
[MIT License](LICENSE)

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

Collab link for this :- https://colab.research.google.com/drive/1k9nkubwlQZkNm5ysEUQHccR5eP-eqg6-?usp=sharing


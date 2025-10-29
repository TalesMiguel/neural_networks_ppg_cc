# Neural Networks Post-Grad Course - Project Instructions

## Project Overview
This is an academic project for a Neural Networks graduate course (Professor Dr. Marcos G. Quiles) focused on implementing and analyzing machine learning models for both classification and regression tasks.

## Project Structure
- `a1.ipynb` - first notebook containing MLP experiments with MNIST (classification) and California Housing (regression)
- `a2.ipynb` - second notebook (currently empty, likely for future assignments)


## Notebook Details
- the first cell of every file should contain the following information:
  - author name
  - date of creation
  - brief description of the notebook's purpose
- the second cell contains the instructions for this assignment

## Key Implementation Patterns

### Training Configuration
- **Optimizer variations**: Compare SGD, SGD+Momentum (0.9), SGD+L2 (0.001), SGD+Momentum+L2
- **Classification**: 50 epochs, batch_size=128, learning_rate=0.01, loss='sparse_categorical_crossentropy'
- **Regression**: 100 epochs, batch_size=32, learning_rate=0.01, loss='mse'
- Always set seeds: `np.random.seed(42)`, `tf.random.set_seed(42)`



### Academic Report Standards
- Document all experiments with markdown cells explaining methodology
- Include statistical comparisons between configurations
- Analyze impact of Momentum and L2 regularization with specific observations
- Provide interpretation sections after each major visualization
- Ensure reproducibility by documenting all hyperparameters

## Common Tasks

### Adding a New Topology
1. Add to `topologies` list with descriptive name and layer configuration
2. Ensure consistent naming format: `"N camadas, X-Y-Z"`
3. Rerun training loop on all topologies to update comparisons

### Modifying Training Parameters
- Epochs, batch size, and learning rate are hardcoded in training functions
- L2 penalty is fixed at 0.001 in model creation
- Momentum is fixed at 0.9 when enabled

### Creating Comparison Plots
Use the established 2x2 subplot pattern with:
- Top row: Validation and Training loss
- Bottom row: Validation and Training accuracy/MAE
- Always include legends, grid, and descriptive titles

## Notes
- This is a pedagogical project focusing on understanding ML fundamentals
- Avoid suggesting modern techniques (batch normalization, dropout, learning rate schedules) unless explicitly requested
- Prioritize clarity and reproducibility
- ALWAYS question suggestions that deviate from the core educational goals
- Try to question me before implementing code changes.
- You can suggest implementations, but always ask first.
- Avoid making assumptions about my requirements.
- Always question your doubts before coding.
- Try to take all of your decisions based on my instructions.
- The markdown cells should be concise and informative, written academicly in first person.

## Coding Style
- avoid using comments, unless absolutely necessary
- DO NOT USE EMOJIS IN THE CODE (NEVER).
- avoid using "print" statements. Always try to plot the useful information instead.
- try using tensorflow with cuda (GPU) for training
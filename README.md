# Atri Assignment

This repository contains the solutions I've came up with for the questions given to me in Atri assignment.  
From what I've understood, the core objective of this assignment is to build a feedforward neural network from the scratch only using **NumPy**, and use different variants of **gradient descent** with backpropogation for a classification task while tracking multiple runs and getting familiar with using **Weights & Biases (wandb)**.

---

## Repository Structure (and How to Run)

To make grading easy, **each assignment question that requires code is implemented in its own Jupyter notebook (`.ipynb`)**.  
Each notebook is **self-contained**, has a **clear file name that maps directly to the question number**, and can be **opened, run, and evaluated independently** without needing to run the other notebooks first.

This design allows a grader to:
- Open any notebook directly 
- Run it top-to-bottom
- Verify outputs for that specific question
- Repeat the same process for other questions

### Files

- `ATRI_Q1.ipynb`  
  **Question 1:** Load the Fashion-MNIST dataset and plot one sample image for each class in a grid format.  
  **Output:** A grid visualization containing one image from each class.

- `ATRI_Q2.ipynb`  
  **Question 2:** Implement a feedforward neural network from scratch using NumPy, with configurable hidden layers and neurons per layer.  
  **Output:** The number of hidden layers and neurons per layer can be configured via the `sizes` list, enabling flexible control. Running the code outputs a probability distribution over classes that always sums to 1.

- `ATRI_Q3.ipynb`  
  **Question 3:** Implement backpropagation with support for multiple optimization algorithms including SGD, Momentum, Nesterov, RMSProp, Adam, and Nadam.  
  **Output:** The optimization algorithm can be selected by assigning the desired method to the `step` variable. Similar to `sizes`, other parameters such as activation function, weight initialization method, batch size, learning rate, and number of epochs are configurable. Running the notebook top-to-bottom outputs loss and accuracy values after each epoch, showing a gradual decrease in loss and increase in accuracy.

- `ATRI_Q4.ipynb`  
  **Question 4:** Perform hyperparameter sweeps using Weights & Biases (wandb), with a validation split taken from the training data.  
  **Output:** This notebook is a modified version of `ATRI_Q3.ipynb` adapted to meet the requirements of Question 4. While it does not generate local visual output, it creates and manages a wandb project, executes hyperparameter sweeps, and logs all required metrics, plots, and summaries. All automatically generated visualizations and written analyses requested for this question are referenced in the wandb report linked in `wandb_report.md`.

- `ATRI_Q7.ipynb`  
  **Question 7:** Evaluate the best-performing model on the test dataset and generate a confusion matrix.  
  **Output:** The model with the highest accuracy identified from the wandb results is used in this notebook, which is an extension of `ATRI_Q3.ipynb`. The code outputs a creatively designed confusion matrix based on test predictions.

- `ATRI_Q8.ipynb`  
  **Question 8:** Compare Cross-Entropy loss with Squared Error loss using training curves and accuracy trends.  
  **Output:** This notebook trains two models, one using Mean Squared Error loss and the other using Cross-Entropy loss. Final accuracies for both models are printed, and epoch-wise accuracies are plotted on the same graph to provide clear visual comparison. Additional observations based on the experimental results are included.

- `ATRI_Q10.ipynb`  
  **Question 10:** Apply insights from Fashion-MNIST experiments to the MNIST dataset using only three selected hyperparameter configurations.  
  **Output:** Three configurations derived from prior wandb experiments are applied to the MNIST dataset to demonstrate that the learnings generalize across datasets. The notebook outputs the final accuracy for each configuration and includes written justification explaining why these configurations were selected.

- `wandb_report.md`  
  Contains the link to the wandb report with hand-written summaries and references to wandb plots and panels required for Questions 4, 5, and 6.

## Notes on Academic Integrity

- All neural network logic, backpropagation, and optimization algorithms were implemented from scratch using NumPy.
- No automatic differentiation tools or deep learning framework optimizers were used.
- The overall code structure, logic, and implementation are original and written by me.
- External resources were consulted only for conceptual understanding and to learn general programming tools and techniques (e.g., NumPy utilities such as `np.where`, array operations, and plotting methods), not for copying implementation code.

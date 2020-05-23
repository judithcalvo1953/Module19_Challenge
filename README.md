# Module19_Challenge
In this challenge, I made many attempts to reach 75% accuracy, but was not able to achieve this standard.  In all cases, I only achieved 53% accuracy with a high loss of 69%.  This was not any better than the distribution of successful in the original dataset, which was 53% were successful and 47% were not successful (per describe statistics in the challenge module with the "noisy" data removed).
## Findings and Discussion
I have included two notebooks, one of which entails use of a fuller dataset with removal of one EIN and NAME.  The other notebook shows a reduced dataset with possibly noisy variables removed, such as classification, which really did not appear to have any bearing on the outcome as it is merely a nomenclature for the more descriptive feature of organization type. The same applies for application type--it is an unordered nominal variable to classify the application, apparently.  In order to be safe, however, I also made several attempts using the fuller dataset which included classification and application type.
These are the models I tested with the full dataset:
- Attempt 1- eight hidden nodes at layer 1, and 5 at layer 2, and 100 epochs.  with Relu on the layers and sigmoid for the outcome, which is appropriate for binary type outcomes.  I didn't want to use more nodes, as there are not that many features.  I was trying not to underfit or overfit my models. I did some research (cite: https://www.heatonresearch.com/2017/06/01/hidden-layers.html ) and there are no hard and fast rules on number of nodes, other than they should follow this general rule of thumb (to quote Jeff Heaton:
" I have a few rules of thumb that I use to choose hidden layers. There are many rule-of-thumb methods for determining an acceptable  number of neurons to use in the hidden layers, such as the following:

  The number of hidden neurons should be between the size of the input layer and the size of the output layer.
  The number of hidden neurons should be 2/3 the size of the input layer, plus the size of the output layer.
  The number of hidden neurons should be less than twice the size of the input layer.
  These three rules provide a starting point for you to consider. Ultimately, the selection of an architecture for your neural network     will come down to trial and error. But what exactly is meant by trial and error? You do not want to start throwing random numbers of    layers and neurons at your network. To do so would be very time consuming.")
- Attempt 2 fuller dataset: added 2 neurons at layer 1 and tried only 62 epochs, as I had seen the previous iteration of 100 seem to rest on 69% accuracy around that point.  When actually executed, this did not successfully allow me to go beyond 53% accuracy, as the previous model.
- Attempt 3--2 nodes added at layer 2, experimented with "softmax" activation at input layers, and staying with sigmoid at output.
- Attempt 4 --increase nodes again
- Attempt 5--increased to 300 epochs

### Reduced Dataset Attempts
In this set of attempts, I removed EIN, Name, Application Type and Classification
- Attempt 1- 4 nodes at layer 1 and 2 at layer 2, with Relu for inputs and Sigmoid for output, 100 epochs
- Attempt 2- 2 neurons added at both layers, and same activations and epochs
- Attempt 3- stepped out to 300 epochs
- Attempt 4-- added a third hidden layer, with 3 neurons and stayed at 100 epochs

## Conclusions
The many models I attempted lead me to think a number of things: 1) I overlooked some aspect of the data that could have been better analyzed, 2) the data is not adequate in terms of features to train properly, thus never achieving a good accuracy, or another model, such as supervised machine learning using logistic regression might be a better approach.  I would have liked to try logistic regression, because having the beta weights to examine and having the log-odds for each feature might better delineate which feature/independent variable(s) carry the most weight in determining outcome. Also, I'd like to consider other factors not included in the dataset, such as geographic location of the entity, years the organization has been in business, and number of employees.

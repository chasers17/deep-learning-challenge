
1. **Overview** of the analysis: Explain the purpose of this analysis.

The purpose of this analysis is to build a deep learning model that can predict whether applicants who receive funding from Alphabet Soup will be successful. This will help Alphabet Soup in allocating resources to the most promising organizations.

2. **Results**: Using bulleted lists and images to support your answers, address the following questions:

* Data Preprocessing
  * What variable(s) are the target(s) for your model?
      - Target variable(s): IS_SUCCESSFUL

  * What variable(s) are the features for your model?
      -APPLICATION_TYPE
      -AFFILIATION
      -CLASSIFICATION
      -USE_CASE
      -ORGANIZATION
      -STATUS
      -INCOME_AMT
      -SPECIAL_CONSIDERATIONS
      -ASK_AMT

  * What variable(s) should be removed from the input data because they are neither targets nor features?
      EIN and NAME

* Compiling, Training, and Evaluating the Model
  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
      - 2 hidden layers, one with 128 neurons and another with 64 neurons, both using relu activation functions. The third layer was the output layer with 1 neuron and used a sigmoid activation function. I selected this because it's a common choice and introduces non-linearity into the model, and the sigmoid function outputs a probability that the output belongs to one of two classes--successful or not successful.

  * Were you able to achieve the target model performance?
      - No. My max accuracy was 74%

  * What steps did you take in your attempts to increase model performance?
      - I tried hyperparameter tuning, a different organization of layers and neurons, and tried adjusting variable exclusions.

3. **Summary**: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
    - The deep learning model achieved 74% accuracy, which is good but just under our 75% target. While this model has potential, it might need some improvements or a different approach. I could try tweaking the settings like the number of neurons or dropout rates. Looking at the data differently might help too, such as handling outliers or rare categories, or even creating new features that make more sense of the patterns. Other types of models like Random Forest, Gradient Boosting, or Support Vector Machines could be strong alternatives and might work better for this problem. Even combining different models could give us better performance by pulling the best parts of each. Overall, the model does a reasonable job of predicting success for Alphabet Soup-funded organizations, but there's room to experiment and potentially find a more accurate approach.

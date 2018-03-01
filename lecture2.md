# Linear classification Support Vector Machine Softmax
**Linear classifier:** *f(x<sub>i</sub>, W, b)=Wx<sub>i</sub> + b*,every row of *W* is a classifier 
for one of the classes

**Interpretation of linear classiퟓ?ers as template matching:** each row of <sub>W</sub> corresponds to 
a template (or sometimes also called a prototype) for one of the classes. The score of each class for 
an image is then obtained by comparing each template with the image using an inner product (or dot product) one by one
to and the one that “first” best. 

**Image data preproceessing:** center data by substracting the mean; scale each input feature to [-1, 1]

**Multiclass Support Vector Machine loss**
  - the SVM loss function wants the score of the corrrect class *y<sub>i</sub>* to be larger than the 
  incorrect class scores by a margin(positive)
  - hinge loss*max(0, -)*
  
**Regularization**
  -  penalizing large weights tends to improve generalization,because it means that **no input** 
  dimension can have a very large influence on the scores all by itself.
  - L2 penalty prefers smaller and more diffuse weight vectors, the final classifier is encouraged to take into 
  account all input dimensions to small amounts rather than a few input dimensions and very strongly
  
**Setting Delta**
  - data loss and regularization loss trade off
  -  the exact value of the margin between the scores is in some sense meaningless because 
  the weights can shrink or stretch the differences arbitrarily. Hence, the
  only real tradeoff is how large we allow the weights to grow (through the regularization strength).
  
**Softmax classifier**
  - softmax function
  - cross-entropy loss
  - information theory view
    - minimizing the cross-entropy between the estimated class probabilities and and the “true” distribution
    - minimizing the KL divergence between the two distributions
  - probabilistic interpretation
    - minimizing the negative log likelihood of the correct class,which can be interpreted as performing 
    Maximum Likelihood Estimation (MLE)
  - Numeric stability: substrct maximum score from all score
  - probabilities in softmax: how peaky or diffuse these probabilities are depends directly on the
regularization strength - which you are in charge of as input to the system. The stronger the regularization strength,
the more diffuse of the probabilites.

**SVM vs Softmax**
  -  the Softmax classifier is never fully happy with the scores it produces: the correct class could always have
a higher probability and the incorrect classes always a lower probability and the loss would
always get better. However, the SVM is happy once the margins are satisfied and it does not
micromanage the exact scores beyond this constraint. 


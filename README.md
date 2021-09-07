# LossFunctions

The aim of this repository is to have all the loss functions at one place for reference. The loss functions provides small explanation followed by mathematical formula.


| Contents|
| ---------------------- |
| 1. [**Mean Square Error**](#mean-square-error) |
| 2. [**Mean Square Lograthmic Error**](#mean-square-lograthmic-error) |
| 3. [**Mean Absolute Error**](#mean-absolute-error) |
| 4. [**Mean Absolute Percentage Error**](#mean-absolute-percentage-error) |
| 5. [**Binary Cross Entropy Loss/Log Loss**](#binary-cross-entropy) |
| 6. [**KL Divergence**](#kl-divergence) |
| 7. [**Multi-Class Classification Loss**]() |
| 8. [**Sparse multi-class loss function**]() |
| 9. [**Multi Class Cross Entropy Loss**]() |
| 10. [**Logistic loss**]() |
| 11. [**Huber loss**]() |
| 12. [**Hinge loss**]() |
| 13. [**Squared hinge loss**]() |
| 14. [**Contrastive loss & Triplet loss**]() |
| 15. [**Center loss**]() |
| 16. [**Exponential loss**]() |
| 17. [**Taylor Cross Entropy**]() |
| 18. [**Symmetric Cross Entropy**]() |
| 19. [**Bi-Tempered Logistic Loss**]() |
| 20. [**Bi-Tempered Loss**]() |
| 21. [**Class Balanced Loss**]() |
| 22. [**Focal Cosign Loss**]() |
| 23. [**Focal Loss**]() |
| 24. [**Label Smoothing Loss**]() |
| 25. [**Face loss function**]() |
| 26. [**Softmax**]() |



## **Mean Square Error** ##
* The mean squared error (MSE) tells you how close a regression line is to a set of points. 
* It does this by taking the distances from the points to the regression line (these distances are the “errors”) and squaring them. 
* The squaring is necessary to remove any negative signs. 
* It also gives more weight to larger differences. It’s called the mean squared error as you’re finding the average of a set of errors. 
* The lower the MSE, the better the forecast.


<p align="center">
<img src="https://latex.codecogs.com/png.latex?MSE%20=%20\frac{1}{n}\sum_{n}^{i=1}(Y_i-\hat{Y_i})^2" />
</p>

## **Mean Square Lograthmic Error** ##
* MSLE will treat small differences between small true and predicted values approximately the same as big differences between large true and predicted values
* Use MSLE when doing regression, believing that your target, conditioned on the input, is normally distributed, and you don’t want large errors to be significantly more penalized than small ones, in those cases where the range of the target value is large.


<p align="center">
<img src="https://latex.codecogs.com/png.latex?L(y,\hat{y})%20=%20\frac{1}{N}\sum_{N}^{i=0}(log(y_i+1)-log(\hat{y_i}+1))^2" />
</p>



## **Mean Absolute Error** ##
* Absolute Error is the amount of error in your measurements.
* The Mean Absolute Error(MAE) is the average of all absolute errors.

<p align="center">
<img src="https://latex.codecogs.com/png.latex?MAE%20=%20\frac{1}{n}\sum_{n}^{i=1}|Y_i-\hat{Y_i}|" />
</p>

## **Mean Percentage Absolute Error** ##
* The mean absolute percentage error (MAPE) is a measure of how accurate a forecast system is. 
* It measures this accuracy as a percentage,

<p align="center">
<img src="https://latex.codecogs.com/png.latex?M%20=%20\frac{1}{n}\sum_{n}^{i=1}\frac{A_t-F_t}{A_t}" />
</p>

M=mean absolute percentage error&emsp;&emsp; n=number of times the summation iteration

$A_t$=actual value&emsp;&emsp;$F_t$	=	forecast value


## **Binary Cross-Entropy Loss** ##
We will have 2 classes, positive and negative. In order to predict how good our predicted probabilities, we should return high values for bad predicitions and low values for good predictions. The formula for Binary Cross Entropy/Log loss can be given as below. 

<p align="center">
<img src="https://latex.codecogs.com/png.latex?H_p(q)=-\frac{1}{N}\sum_{i=1}^{N}y_i\cdot%20log(p(y_i))+(1-y_i)\cdot%20log(1-p(y_i))" />
</p>

Negative log helps in penalizing the postive loss if it is too low.

## **KL Divergence** ##
The Kullback-Leibler Divergence,or “KL Divergence” for short, is a measure of dissimilarity between two distributions.

This means that, the closer p(y) gets to q(y), the lower the divergence. So, we need to find a good p(y) to use. It looks for the best possible p(y), which is the one that minimizes the cross-entropy.
<p align="center">
<img src="https://latex.codecogs.com/png.latex?D_{KL}(q||p)=H_p(q)-H(q)=\sum_{c=1}^{C}q(y_c)\cdot%20[log(q(y_c))-log(p(y_c))]" />
</p>



# LossFunctions

The aim of this repo is to have all the loss functions at one place for reference. The loss functions provides small explanation followed by mathematical formula


| Contents|
| ---------------------- |
| 1. [**Mean Square Error**](#mean-square-error) |
| 2. [**Mean Square Lograthmic Error**](#mean-square-lograthmic-error) |
| 3. [**Mean Absolute Error**](#mean-absolute-error) |
| 4. [**Mean Absolute Percentage Error**](#mean-absolute-percentage-error) |
| 5. [**Binary Classification Loss**]() |
| 6. [**Binary Entropy Loss**]() |
| 7. [**Multi-Class Classification Loss**]() |
| 8. [**Sparse multi-class loss function**]() |
| 9. [**Multi Class Cross Entropy Loss**]() |
| 10. [**KL Divergence**]() |
| 11. [**Logistic loss**]() |
| 12. [**Huber loss**]() |
| 13. [**Hinge loss**]() |
| 14. [**Squared hinge loss**]() |
| 15. [**Contrastive loss & Triplet loss**]() |
| 16. [**Center loss**]() |
| 17. [**Exponential loss**]() |
| 18. [**Taylor Cross Entropy**]() |
| 19. [**Symmetric Cross Entropy**]() |
| 20. [**Bi-Tempered Logistic Loss**]() |
| 21. [**Bi-Tempered Loss**]() |
| 22. [**Class Balanced Loss**]() |
| 23. [**Focal Cosign Loss**]() |
| 24. [**Focal Loss**]() |
| 25. [**Label Smoothing Loss**]() |
| 26. [**Face loss function**]() |
| 27. [**Softmax**]() |



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

#### M	=	mean absolute percentage error
#### n	=	number of times the summation iteration happens
#### $A_t$	=	actual value
#### $F_t$	=	forecast value


## **Binary Classification Loss** ##


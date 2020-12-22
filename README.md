# Linear-Regression
It is a process of finding a linear relationship between input and output that is a best fit of observed data. Its ultimate aim is to learn a curve that fits the data well. It is used to predict continuous valued outputs.    

**Hypothesis:** It is nothing but a function used for prediction.    

**Univariate:**  Output is a function of single feature
 
 <img src="https://render.githubusercontent.com/render/math?math=h(x)=w_0%2Bw_1x">     
 
**Multivariate:** Output is a function of two or more(multiple) features

<img src="https://render.githubusercontent.com/render/math?math=h(x_1,x_2,...,x_n)=w_0%2Bw_1x_1%2Bw_2x_2%2B...%2Bw_nx_n">
                              
                           
  
   x<sub>i</sub>'s are features   
   w<sub>i</sub>'s are paramaters to be learned     
   w<sub>0</sub> is zero condition   
    
**We need to learn a function h(x) by tuning its parameters, so that it is a good predictor of y.** 

**How to learn the values of parameters?**   

**Training**

Training is a process of learning the values of parameters.  
1. Initialize parameters to random values
2. Measure how close the predictions are to the actual y-values using cost function
3. Update the values of parameters in the direction of decreasing error (Gradient Descent)
4. Repeat 2 and 3 until convergence (i.e error is less than the predefined error)  

**Cost function of linear regression:**  

**<img src="https://render.githubusercontent.com/render/math?math=J(w)=\frac{1}{2m}\sum_{i=1}^{m}(h_w(x^i)-y^i)^2">**

     m: number of training examples
     i: ith training example
     
**How to update values?**  

**Use gradient descent algorithm**    

A gradient measures the change in output with respect to the change in input. It is nothing but slope i.e., partial derivative of output with respect to input. Gradient descent is nothing but taking a step in the direction of decreasing slope. The higher the gradient, the steeper the slope and the faster a model can learn. If the slope is zero, the model stops learning.   

**Gradient Descent Algorithm:**  
It is an optimization algorithm that updates parameters iteratively to minimize a given function to its local minimum.   

**<img src="https://render.githubusercontent.com/render/math?math=\frac{\partial}{\partial w_j}(J(w))=\frac{1}{m}\sum_{i=1}^{m}(h_w(x^i)-y^i)x_j">**      

Repeat until convergence
{

<img src="https://render.githubusercontent.com/render/math?math=w_j: w_j-\alpha \frac{\partial}{\partial j}(J(w))">
             
              update all w's simultaneously
}     
 &alpha; is learning rate   
 choice of &alpha; is very important:   
    1. **Too small:** Very slow to converge ( more no. of iterations)          
    2. **Too large:** Overshoots minima (diverges)    
    
**Testing**  
For new data, predicted output=h(x)
 

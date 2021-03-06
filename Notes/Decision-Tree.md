# Summary
  - DT: Decision Tree (if-then rule & Conditional Probability Distribution)
  - DT First Step: Feature Selection
    - Information Gain (ID3)
    
    <a href="https://www.codecogs.com/eqnedit.php?latex=\\&space;g(D,A)=H(D)-H(D|A)&space;\\&space;H(D)=-\sum_{k=1}^{K}\frac{|C_k|}{|D|}log_2\frac{|C_k|}{|D|}&space;\\&space;H(D|A)=\sum_{i=1}^{n}\frac{|D_i|}{|D|}H(D_i)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\\&space;g(D,A)=H(D)-H(D|A)&space;\\&space;H(D)=-\sum_{k=1}^{K}\frac{|C_k|}{|D|}log_2\frac{|C_k|}{|D|}&space;\\&space;H(D|A)=\sum_{i=1}^{n}\frac{|D_i|}{|D|}H(D_i)" title="\\ g(D,A)=H(D)-H(D|A) \\ H(D)=-\sum_{k=1}^{K}\frac{|C_k|}{|D|}log_2\frac{|C_k|}{|D|} \\ H(D|A)=\sum_{i=1}^{n}\frac{|D_i|}{|D|}H(D_i)" /></a>
    
    > notes: $H(D)$ is the entropy of data set $D$, $H(D_i)$ is the entropy of data set $D_i$, 
    and $H(D|A)$ is the conditional entropy of data set $D$ versus feature $A$. 
    $D_i$ is a subset of samples in which feature $A$ takes the $i^{th}$ value in $D$, 
    and $C_k$ is a subset of samples belonging to the $k^{th}$ class in $D$. 
    $n$ is the number of values of feature $A$, and $K$ is the number of classes.
    
    - Information Gain Ratio(C4.5)
    
    <a href="https://www.codecogs.com/eqnedit.php?latex=g_R(D,A)=\frac{g(D,A)}{H_A(D)}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?g_R(D,A)=\frac{g(D,A)}{H_A(D)}" title="g_R(D,A)=\frac{g(D,A)}{H_A(D)}" /></a>
    
    > notes: $g(D,A)$ is the information gain, and $H_A(D)$ is the entropy of $D$ for the value of feature $A$.
    
    - Gini Index (CART: Classification And Regression Tree)
    
    <a href="https://www.codecogs.com/eqnedit.php?latex=Gini(D)=1-\sum_{k=1}^{K}(\frac{|C_k|}{|D|})^2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Gini(D)=1-\sum_{k=1}^{K}(\frac{|C_k|}{|D|})^2" title="Gini(D)=1-\sum_{k=1}^{K}(\frac{|C_k|}{|D|})^2" /></a>
    
    Gini index of set D under characteristic A condition:
    
    <a href="https://www.codecogs.com/eqnedit.php?latex=Gini(D,&space;A)=\frac{|D_1|}{|D|}Gini(D_1)&plus;\frac{|D_2|}{|D|}Gini(D_2)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Gini(D,&space;A)=\frac{|D_1|}{|D|}Gini(D_1)&plus;\frac{|D_2|}{|D|}Gini(D_2)" title="Gini(D, A)=\frac{|D_1|}{|D|}Gini(D_1)+\frac{|D_2|}{|D|}Gini(D_2)" /></a>

  - DT Second Step: DT Generation ---> Rule: Max(Information Gain) or Max(Information Gain Ratio) or Min(Gini Index)
  
  - DT Third Step: DT Pruning ---> Rule: Min(Loss Function) or Min(Cost Function)
  <a href="https://www.codecogs.com/eqnedit.php?latex=C_\alpha&space;(T)=C(T)&plus;\alpha&space;T" target="_blank"><img src="https://latex.codecogs.com/gif.latex?C_\alpha&space;(T)=C(T)&plus;\alpha&space;T" title="C_\alpha (T)=C(T)+\alpha T" /></a>
  
  > notes: $C(T)$ represents the prediction error of the model on the training data, that is, the degree of fitting of the model with the training data, $|T|$ represents the complexity of the model, and the parameter $\alpha>=0$ controls the influence between the two. $\alpha$ larger a prompts the selection of a simpler model (tree), and a smaller a prompts the selection of a more complex model (tree). $\alpha=0$ means that only the degree of fit of the model to the training data is considered, regardless of the complexity of the model.
 
 
----
# Exercise
[5.1 & 5.2 & 5.3 & 5.4 --- from CSDN](https://blog.csdn.net/familyshizhouna/article/details/72551841)

  
  
  
  
  
  
    

# Admin notes
- Teaching demos exist
- Grad student presentations in M7
- quiz 2 on Fri covering M3 Linear Models
- Paper 1 due Saturday

# Logistic Regression
Moving towards classification
>[!warning]
>Different from linear regression!
- line vs squiggle
	- conditional on $\sigma$, overfitting & dithering/noise
- Decision regions
- sigmoid of linear model
	- projecting to $[0,1]$ to treat as probability
- loss function
	- $L(h(x),y)=-y \ln(h(x)) - (1-y)\ln(1-h(x))$ where $h(x)=P(y=1 \mid x)$
	- very cautious, worst thing is to be confidently wrong
- Messing with weights and biases

# Multinomial Logistic Regression
For this class, labels are going to be mostly binary, but soft labels *can* exist as a special use case
- supports multi-class instead of just binary
- Similar changes to SLR -> MLR
	- $W$ is now a matrix, $b$ now a vector
- Do MLR $C$ times, take the highest value, kinda
	- which class is most confident that the point exists there?
- softmax: convert the output vectors into probabilities
- Cross-entropy
- Initialization matters with numerical instability
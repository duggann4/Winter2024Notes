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
- 
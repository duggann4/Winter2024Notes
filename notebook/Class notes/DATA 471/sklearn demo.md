- using the penguin dataset

```python
from sklearn.model_selection import train_test_split
X_tr, X_vl, y_tr, y_vl = train_test_split(X, y, train_size=0.6)
X_dv, X_te, y_dv, y_te = train_test_split(X_vl, y_vl)
```

Going to use MSE as our metric function; has been implemented by skl
```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()

model.fit(X_tr, y_tr)

y_hat_tr = model.predict(X_tr)
y_hat_dv = model.predict(X_dv)

print(mean_squared_error(y_tr, y_hat_tr))
print(mean_squared_error(y_dv, y_hat_dv))
```

Also, `matplotlib` exists for visualizing models...

- `torch` exists?

In an SVR, need to normalize data so that all data is in the same order of magnitude (e.g. Z-score normalization)
- there are a bunch of preprocessing tools in `sklearn`...
- What happens to y-stuff? (in this case, just also normed)

DNNs, `GridSearchCV`

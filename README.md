# Prueba
import numpy as np
import matplotlib.pyplot as plt

n = 30

mu, sigma = 0, 1 # mean and standard deviation
noise = np.random.normal(mu, sigma, n)

X = np.random.rand(n)*5
Y = 2*X + 1 + noise

plt.axis([0, 5, 0, 12])
plt.plot(X,Y,'bo')
plt.show()

m=(np.dot(X,Y)-n*np.mean(X)*np.mean(Y))/(np.dot(X,X)-(1/n)*(np.sum(X))*(np.sum(X)))
print(m)
b=np.mean(Y)-m*np.mean(X)
print(b)

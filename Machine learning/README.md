# Machine learning

## Why Go
As everyone knows, data analysis and machine learning related problems are best treated in Python and R. They have wonderful libraries doing all the hard work. However, their use encourages some practices into the workflow that became problematic during deployment. There is a good explanation at https://www.oreilly.com/content/data-science-gophers/

The other reason is speed. In order to manipulate large streams of data in several models, it is better if we use all the hardware at disposition in an efficent and consistent way. And that is the main strenght of Go.

## Tensorflow
As you probably already know, Tensorflow is a library written in C++ with bindings for Python, Java and Go. It has high level APIs for other languages as well, but we are interested in running our models with Go.

In order to understand how Tensorflow works in Go, there is some reading involved:
- https://pgaleone.eu/tensorflow/go/2017/05/29/understanding-tensorflow-using-go/
- https://github.com/galeone/tfgo


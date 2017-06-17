---
layout: default
title:  "DeepLearning4J MNIST Android app"
date:   2017-06-17 10:30:00
categories: main
---

DeepLearning4J seems like a pretty interesting project and I just gave a shot and made a simple digit recognition Android app. Here are some useful resources I found:
1. <a href="https://deeplearning4j.org/quickstart">It talks about how to open an existing project from DeepLearning4J examples.</a>
2. <a href="https://deeplearning4j.org/mnist-for-beginners">It shows the example of MNIST. Following this example, you can train the neural network.</a>
3. <a href="https://deeplearning4j.org/modelpersistence">How to save/read model</a>
4. <a href="https://deeplearning4j.org/android">It has an example of how to train the model in Android. I did not train the model in Android, since it is time- and resource-consuming. I pretrained the model in my desktop and then copied it to Android phone. After that, loading the model from the app, and predict the digit. </a>

The Android app is <a href="https://github.com/flyman3046/MNIST_DL4J">here</a>. The model is put <a href="https://github.com/flyman3046/MNIST_DL4J/tree/master/app/src/main/res/raw">here</a>.

[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com
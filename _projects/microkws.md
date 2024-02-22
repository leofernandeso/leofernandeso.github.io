---
layout: page
title: MicroKWS - TinyML Keyword Spotting
description: Running deep learning models with cheap hardware seems increasingly possible. This was the focus of this project.
img: assets/img/12.jpg
importance: 1
category: projects
related_publications: false
---

This project was done during the course of Embedded System Design for Machine Learning, offered at the Technical University of Munich.

Deploying a deep learning model in cheap hardware is often a challenge. Traditionally, running such models require expensive GPU's. However, this is rapidly changing, especially due to the advances in the field of TinyML - a field of machine learning which focuses on optimizing computational performance of expensive machine learning models.

Let's say you trained your deep learning model with TensorFlow. You can now make use of tools like [TensorFlow Lite](https://www.tensorflow.org/lite) in order to optimize your models. For instance, you can apply [post-training quantization](https://www.tensorflow.org/lite/performance/post_training_quantization) in order to force the layers of your model to perform its operation by using a smaller floating point representation, which saves hardware cycles and can lead to smaller memory usage and a significant speedup.

Beyond that, one can also make use of ML compilers, which can take your optimized TFLite models and compile them to a binary which can be run on any CPU. For instance, [Apache TVM](https://tvm.apache.org/) is a tool that can transpile your .tflite model to C code, enabling the use of any optimizations that your compiler might offer, which can lead to significant speedups in your model. It is even possible to get to the point where you can run a deep learning model in a microcontroller. Of course, you will not be able to run any model on a microcontroller, but the fact that you can run a small to medium-sized model is already something to be excited about.

And this was exactly the focus of this project. Given a simple ML task, the final goal was to have this task deployed in a microcontroller.

video demo coming soon!

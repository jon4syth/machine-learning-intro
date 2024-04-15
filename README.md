# Introduction to Deep Learning = Machine Learning + Neural Networks

## outline

1. Introduce myself
2. Share quote from Fastai about learning from peers/beginners
3. Show functions involved in a basic neural network
4. Explain WHERE these functions are used (neural network diagram)
5. Explain WHY these functions are used
6. Demonstrate a neural network using the javascript demo with Mnist Data
7. Refer to learning resources


## Introduction

Hello my name is Jon Forsyth, I am a former linguistics student at Brigham Young University and former anthropology student before that at the University of Utah.  During and after my studies I got into technology and programming.  At the end of my linguistics program in 2014, I finished a machine learning project.  This project did not use deep learning, but another flavor of machine learning.  Since then I have worked in web programming.  Recently however, I have had the machine learning itch again.  I actually volunteered to give this presentation since it aligned with my current pursuits.  I hope to help those who are looking to get into the field of deep learning whether applied to natural language processing or other areas of research.  The tools and mathematics of neural networks apply to many different kinds of tasks.

You may feel disheartened if I tell you that I'm a noob in this field, but I have an advantage because of that.  Rachel Thomas, the co-founder of fast.ai, an educational company that teaches deep learning, states:

"You are best positioned to help people one step behind you. The material is
still fresh in your mind. Many experts have forgotten what it was like to be a
beginner (or an intermediate) and have forgotten why the topic is hard to
understand when you first hear it. The context of your particular background,
your particular style, and your knowledge level will give a different twist to
what you’re writing about."<sup>1</sup>

So my brain and this presentation are hot off the press, especially helpful for those just learning about this field.

When I proposed this presentation, I made the case that there are too many introductions and tutorials available for doing deep learning using image recognition of different varieties.  Since my proposal was accepted, I have since learned that there is actually a lot of cross-over knowledge from image recognition to natural language processing applications of neural networks.  Neural networks themselves are very general purpose mathematical learning machines that can be applied to many problems which we have only begun to explore as practitioners.  Ooh, did I just say 'we' and include myself in the group of neural network practitioners.  Yes, yes I did.  And I believe that after you have heard or read my presentation, that you can, if you don't already, consider yourself as part of this community, just by jumping in and getting started.  It's not too hard.

Although Python is the dominant programming language for doing deep learning today, I will share a demo in javascript that I found on a Medium post by Lin Xiang<sup>2</sup> 

## Neural Networks overview

Neural networks are perhaps more accurately called artificial neural networks.  They are modeled after the brains of animals including humans.  Although they don't work exactly the same way as brains, and it is not known in full detail how the brain's neural network operates, but we know enough to take great advantage of them in this type of model.  Artificial neural networks were developed in the 1940s and 1950s by contributions of multiple neuro scientists and computer engineers (see https://cs.stanford.edu/people/eroberts/courses/soco/projects/neural-networks/History/history1.html).  Interest in neural networks has fluctuated over the decades since then, and was low in the first decade of the 2000's, but then Geoff Hinton led a team from the University of Toronto to win an annual computer vision challenge in 2012 using a neural network (see https://image-net.org/challenges/LSVRC/2012/results.html) which reignited interest.

Today I'm going to talk about the basics of a neural network without getting into the various modern enhancements that have come in recent years.  This foundation of neural networks is essential for understanding them well and their recent improvements.

### Mathematical Components of a Neural Network

- We combine inputs with weights (aka parameters): $$weight \cdot input = W \cdot I$$

- We can use the sigmoid function for a node's output: $$1 \over 1 + e^{-x}$$ where $e \approx 2.718$ and $x = W \cdot I$ from above

- We need a loss function such as: $$error = (t - o)^2$$ where $t$ is the target value and $o$ is the output of a final or head node.

- The derivative of the loss function or error with respect to current weights multiplied by the derivative of the sigmoid function (this is approximate): $$a \cdot E_k \cdot O_k(1 - O_k) \cdot^T_j$$ where $a$ = learning rate, $E_k$ = total error, $O_k$ = output of final nodes

### Training

To train a neural network, we feed it inputs in the form of numbers that represent the type of items that a completely trained neural network will be expected to identify or categorize when it is deployed into production.  These items could be images, pieces of text, audio input, etc.  Whatever the actual real-world representation of these items, they need to be converted into numbers, as that is what a neural network works with.  It doesn't actually know what it is doing, it just is very fast at doing computations when ran by a computer, especially GPUs.

The output is also some sort of number or set of numbers.  However, the final human-readable representation of the output will either be a number along a scale of acceptable values, or a category among a fixed number of categories represented by underlying numbers.  This choice depends upon what the goal of the project is.  We'll look at specific categorical outputs or predictions in this presentation.



## References
1. FastAI book Chapter 2 (https://github.com/fastai/fastbook/blob/master/02_production.ipynb), Accessed on 9 November 2022
2. "Build Your Own Neural Network with JavaScript" (https://javascript.plainenglish.io/make-your-own-neural-network-app-with-plain-javascript-and-a-tiny-bit-of-math-js-30ab5ff4cbd5) Accessed on 7 November 2022


# Introduction to Deep Learning = Machine Learning + Neural Networks

## outline
1. introduce myself
2. quote from fastai about learning from peers/beginners
3. functions involved in a basic neural network
4. where these functions are used (neural network diagram)
5. why these functions are used
6. javascript demo with Mnist Data
7. Other resources


## Introduction
Hello my name is Jon Forsyth, I am a former linguistics student at Brigham Young University and former anthropology student before that at the University of Utah.  During and after my studies I got into technology and programming.  During my linguistics program I did project that involved machine learning in 2014.  It was not a deep learning project, and I went into web programming afterwards.  However recently I have had the machine learning itch again.  I actually volunteered to give this presentation since it aligned with my current efforts.  So I hope to help those who are looking to get into the field of deep learning whether applied to natural language processing or other areas of research.  They actually have a lot of overlap in terms of the tools and mathematics.  Or at least I can speak to deep learning--machine learning with neural networks.

You may feel disheartened if I tell you that I'm a noob in this field, but I have an advantage because of that.  Rachel Thomas, the co-founder of fast.ai, an educational company that teaches deep learning, states:

"You are best positioned to help people one step behind you. The material is
still fresh in your mind. Many experts have forgotten what it was like to be a
beginner (or an intermediate) and have forgotten why the topic is hard to
understand when you first hear it. The context of your particular background,
your particular style, and your knowledge level will give a different twist to
what you’re writing about."<sup>1</sup>

So my brain and this presentation are hot off the press, especially helpful for those just learning about this field.

When I proposed this presentation, I made the case that there are too many introductions and tutorials available for doing deep learning using image recognition of different varieties.  Since my proposal was accepted, I have since learned that there is actually a lot of cross-over knowledge from image recognition to natural language processing applications of neural networks.  Neural networks themselves are very general purpose mathematical learning machines that can be applied to large number of problems which we have only begun to explore as practitioners.  Ooh, did I just say 'we' and include myself in the group of neural network practitioners.  Yes, yes I did.  And I feel that after you have heard or read my presentation, that you will, if you aren't already, be able to count yourself as part of this community, just by jumping in and getting started.  It's too not hard.

Orginally I was going to give a demo in Python as that is the dominant programming language for doing deep learning today.  However, because of technical difficulties--translation, too lazy to figure out how to host a working neural network model in Python--it's not that hard, I just distracted with a lot of brain splitting activities--therefore I have a demo in javascript that I ripped off of a Medium post by Lin Xiang<sup>2</sup> 

## Neural Networks overview

Neural networks are perhaps more accurately called artificial neural networks.  They are modeled after the brains of animals including humans.  Although they don't work exactly the same way as brains, and it is not known in full detail how the brain's neural network operates, but we know enough to take great advantage of them in this type of model.  Artificial neural networks were developed in the 1940s and 1950s by contributions of multiple neuro scientists and computer engineers (see https://cs.stanford.edu/people/eroberts/courses/soco/projects/neural-networks/History/history1.html), but they were largely ignored until Geoff Hinton led a team from the University of Toronto to win an annual computer vision challenge in 2012 using a neural network (see https://image-net.org/challenges/LSVRC/2012/results.html).

Today I'm going to talk about the basics of a neural network without getting into the various modern enhancements that have come in recent years.  This foundation neural networks is essential for understanding the more advanced and improvements, since they are built on this same foundation.

### Mathematical Components of a Neural Network
- $W \cdot I$ - weights (aka parameters) multiplied by the inputs using matrix multiplication, hence the dot-product notation.

- $1 \over 1 + e^-x$ - the sigmoid function, the x is the product from the matrix multiplication for this node's incoming inputs and weights

- $ (t - e)^2 $

- $ a \cdot E_k \cdot O_k(1 - O_k) \cdot^T_j $




### Training
To train a neural network, we feed it inputs in the form of numbers that represent the type of items that a completely trained neural network will be expected to identify or categorize when it is deployed into production.  These items could be images, pieces of text, audio input, etc.  Whatever the actual real-world representation of these items, they need to be converted into numbers, as that is what a neural network works with.  It doesn't actually know what it is doing, it just is very fast at doing computations when ran by a computer.

The output is also some sort of number, although the desired output will either be a number along a scale of acceptable values, or a category among a fixed number of categories which are still represented by a range of numbers ultimately.  This choice depends upon what the goal of the project is.  We'll look at specific categorical outputs or predictions in this presentation.



## References
1. FastAI book Chapter 2 (https://github.com/fastai/fastbook/blob/master/02_production.ipynb), Accessed on 9 November 2022
2. "Build Your Own Neural Network with JavaScript" (https://javascript.plainenglish.io/make-your-own-neural-network-app-with-plain-javascript-and-a-tiny-bit-of-math-js-30ab5ff4cbd5) Accessed on 7 November 2022


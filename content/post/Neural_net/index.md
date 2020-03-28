---
title: Neural Networks
tags : ["Machine learning", "Deep Learning", "Neural Networks"]
date : "2016-06-28"
type : "passages"
---

# Neural Networks - The first cut
As I get ready to do my first solo workshop on Deep learning in the field of NLP, my anxiety levels are extremely high and I am definitely excited. 
The anxiety levels have made me read numerous papers , blog posts and definitely some code. I feel I have made a small progress in understanding the subject and this makes me feel a little comfortable.

Deep learning is really not too hard to understand if you think about it from a real world angle. What we are really trying to do is to build systems that can emulate the human mind.  

To explain neural networks, I will take a an real world example and then we will see how they are represented in an NN world. Let us take the simple example of catching a ball when it is thrown at us. If you ask a small kid how he does it , you will hear him say well you throw the ball and I catch it. If you try to look a little closer , there are so many things that the human brain is doing in such a short span time and with the input data changing every second. The human brain is computing the size of the ball, the speed of the ball, the trajectory and checks how confident you are in catching this ball. All of these computations are done in real time and you have an outcome, either you catch the ball or you fail to catch it. Overtime if you are constantly trained to catch the ball, you will eventually see that your confidence levels are high and your outcome essentially is almost positive.

If you were to let a system catch a ball, the very first thing that you need to do is provide inputs to the system i.e translate the type of ball into something that a computer can understand. You would do the same for all the different forms of input. Now your input set is ready. 
The next step is defining what you want to do with these inputs and the process of performing an operation on a given input in the field of NN is defined as activation function. The node that performs this activation function on the input is essentially called the neuron. Our nervous system has 10^11 neurons so having just one neuron might not yield us good results.So you add multiple neurons that can perform the same function on the set of defined inputs. We call this bunch as the `hidden layer`. 

Now the very next question we ask ourselves is, okay what is the use of adding more neurons to do the same function, this is answered by `weight matrix`. Before explaining what weight matrix is, let us understand what it means in the real world. Every input we considered for the ball example plays some part in the outcome, how much part it plays is what is defined the Weight matrix. As we do not know what is the prominence of each input we just randomly assign weights to input to initiate the process. These weights, multiplied for every input combination are used as inputs for the neurons. Now we have considered all our inputs and we have built something that emulates the human brain. We still do not know if the system caught the ball or not. To know this we pass the output of all the neurons to another node that generates the output by behaving as another neuron that operates on incoming data i.e output of the `hidden layer`, thereby telling us if the ball has been caught for a given set of input.We are now done with the first pass of `NN` and this is termed as feed forward. 

Now this is where things get really interesting, we have the output from the system and the outcome of a real entity, there is a very high chance the system predicted the wrong outcome. The reason is, the system does not understand the inputs and their prominence aka weights properly. This needs to be corrected, we find the difference between the expected outcome and system generated outcome and we call this error. We need to reduce the error, we cannot modify the inputs but what we can modify are the weights. So that is exactly what happens in an `NN', by a process known as Back-propagation which is beautifully explained by Christopher Colahs Blog on Back propagation. This process of adjusting weights to reduce error is when the actual learning starts. Once the weights are adjusted, the feed forward process begins from the first layer all the way to the output. 

So now you have started training your model and your model is learning slowly. In the ball catching example, I mentioned that a person becomes a better catcher if you train him over time. This is exactly what we do with our model too, we keep reiterating our process eventually giving us an intelligent system that can predict if a person can catch the ball or not based on different criteria.

This is how an `NN` works and this is our first small step to building intelligent systems. 

## References and Additional Links :

[ Christopher Colah - Back propogation ](http://colah.github.io/posts/2015-08-Backprop/)
[Raghotham Sripadraj - Introduction To Artifical Neural Networks] (https://medium.com/@raghothams/introduction-to-neural-networks-944a7e38138e)
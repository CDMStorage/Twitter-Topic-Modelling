# Twitter-Topic-Modelling <br />
Topic Modelling and Sentiment Analysis on Tweets Using LDA 

## Contents
 - [About](#about)
 - [How does it Work?](#how-does-it-work)
 - [Dependencies](#dependencies)
 - [Future-Plans](#future-plans)

##About

This project utilizes LDA to model topics amongst queried tweets, and performs sentiment analysis on the tweets. The potential use cases of some of the concepts utilized in this project are almost infinite.


##How does it Work? 

*Note: I'll give it my best explanation which is very simplified.*

Assume we had only 3 topics in the world, and that each topic is represented by a collection of probabilities of words that belong to them

1. Programming (0.10*Python + 0.10*C++ + 0.10*C .... = 1)
2. Animals (0.10*Panda + 0.10*Bear + .... = 1)
3. Video Games (0.10*Dota2 + 0.10LeagueofLegends + ... = 1)


Now if we had an article about programming:

> "Python is my favourite programming language. It is a dynamically typed language, whereas C++ is static and as a result you run into alot more errors. However, pointers and references are life so I kinda like C++ a lot too"

As a Human, it is very obvious that this article is about Topic 1 (or programming) isnt it?

Well if we scrambled the text:

> "It errors. alot programming However, and references a too static and typed kinda you is into pointers a more Python result run are is so I whereas like language. C++ life C++ a language, my dynamically as lot favourite is"

As a Human, we can still kind of tell what the text is about can't we?

LDA (latent dirichlet allocation) Works in a very smilar way.

We feed it a bag of words which it assumes to be related (syntax, order, punctuation all dont matter!). And it tries to generate what the topics might have been, which made up these bag of words.

For such a reason, it makes sense to train the model using Wikipedia Articles where all the words in each article, ARE related (to an extent).


##Dependencies

Requires [Python 2.7.x]

[Gensim] requires [NumPy] and [SciPy]

```
pip install numpy
pip install scipy
```
Requires [Gensim]
```
pip install gensim
```
Requires [Twython]

```
pip install twython
```
Requires [Langdetect]
```
pip install langdetect
```
##Future Plans

While the current Flask-Application works well to visualize the calculated, much more could be done. I plan to build a REST-API, and build an express/angular/node Web-App that would communicate with the API and display the information in a much more visually pleasing way.

[Python 2.7.x]:https://www.python.org/downloads/
[Gensim]:https://pypi.python.org/pypi/gensim
[Numpy]:http://www.scipy.org/install.html
[SciPy]:http://www.scipy.org/install.html
[langdetect]:https://pypi.python.org/pypi/langdetect
[Twython]:https://twython.readthedocs.org/en/latest/usage/install.html

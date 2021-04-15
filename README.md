# Tv script generation
## Introduction
This is one of [Deep learning nanodegree](https://classroom.udacity.com/nanodegrees/nd101/parts/2e8d3b5d-aa70-4376-946f-0cdc37127d7d/modules/49d2e25d-6df2-48df-8ccd-88417ae208fc/lessons/368c9af3-c8b8-4b01-92ba-40d7e989d6e7/concepts/900d740a-e47d-4b67-be4c-ca27ea8981e2) major projects.
In this project, I generated my own Seinfeld TV scripts using RNNs. I used a Seinfeld dataset of scripts from 9 seasons. The Neural Network I built generated a new, "fake" TV script.

## Dataset
Seinfeld dataset of scripts from 9 seasons.


## Trials and observations
I was mainly tuning over three prameters : learning rate , number of epochs , batch size , sequence length

The set of values i tried for :

 * learning rate = [0.1 , 0.01 , 0.001]
 * num_epochs = [5 , 10 ,15 , 25]
 * batch_size = [32 , 64 ,128 ,64]
 * sequence_length = [ 5 , 8 ,10 ,12, 15, 100]

I made the following observations :

  1. The higher the batch size the lower loss i get.
  2. The lower the sequence length , the faster is my model in training and convergence.
  3. The 0.001 learning rate was the only one was succesfull with model. As for 0.1 learning rate , the model suffered from unstability and for 0.01 learning rate , the model wasn't able to converge (sounds like he stuck in with some loss).


## Model parameter
```
sequence_length = 12
batch_size = 256
num_epochs = 10
learning_rate = .001 
vocab_size = len(vocab_to_int)
output_size = vocab_size
embedding_dim = 300
hidden_dim = 205
n_layers = 2
```

## Training

```
final loss : 3.3668212304115297
```

## Results

The following is a sample of the output script.
 ```
 george: i'm a very nice person, and i don't even think so.

jerry: i don't know.

kramer:(to jerry) you know, i don't have a little nervous.

jerry: what?

george: i don't even want to know how much i want.

george:(to george) you got a little bit that?

kramer: oh, yeah.

george: i was a little anxious to go.

kramer: yeah?

jerry: what?

kramer: well.....

jerry: you know, you know what the hell was that?(he exits)

kramer: hey, you know how long you're thinking?

jerry: i was just thinking about the last time.

kramer: well, it's the damnedest thing...(to george) you know, i don't even think i should be able to get the way back to the table.

elaine: oh, no.

george:(on phone) hello. you know, i don't know what i do.

jerry: what do you mean?

jerry: i know, i think we could go.

jerry: well, what are you gonna get?

jerry: i was thinking of donating it to her! you know, i can't do the whole rotten.

elaine: what?

elaine: i know.(elaine enters)

jerry:(shocked) i know you don't.

elaine: well, it's just a long time.

elaine: what?(he gets up) i think i could get the car. i don't know what i do, you know what i think?!

jerry: well, i don't think it might be.

morty: you got that, a lot of pressure soups.

kramer: oh, you don't know how i do.

george: well, you know, i don't think i can get you a couple of hours to get a little bit.

elaine:(to
 ```


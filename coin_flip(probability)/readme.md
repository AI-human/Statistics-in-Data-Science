#### Experiments and Sample Spaces

In probability, an  _experiment_  is something that produces observation(s) with some level of uncertainty. A  _sample point_  is a single possible outcome of an experiment. Finally, a  _sample space_  is the set of all possible sample points for an experiment.

For example, suppose that we run an experiment where we flip a coin twice and record whether each flip results in heads or tails. There are four sample points in this experiment: two heads (_HH_), tails and then heads (TH), heads and then tails (HT), or two tails (TT). We can write the full sample space for this experiment as follows:


Suppose we are interested in the probability of one specific outcome:  _HH_. A specific outcome (or set of outcomes) is known as an  _event_  and is a subset of the sample space. Three events we might look at in this sample space are:

Getting Two Heads Getting Two Tails Getting Both a Heads and Tails Getting Two Heads A Getting Two Tails B  Getting Both a Heads and Tails C 

The frequentist definition of  _probability_  is as follows: If we run an experiment an infinite amount of times, the probability of each event is the proportion of times it occurs. Unfortunately, we don’t have the ability to flip two coins an infinite amount of times — but we can estimate probabilities by choosing some other large number, such as 1000. Let’s give it a try!

Okay, we have flipped two coins 1000 times. Wasn’t that FUN? Here are each of the outcomes and the number of times we observed each one:

-   _{HH}_: 252
-   _{TT}_: 247
-   _{HT}_: 256
-   _{TH}_: 245

To calculate the estimated probability of any one outcome, we use the following formula:

Number of Times Event OccurredTotal Number of TrialsP(Event)=Total Number of TrialsNumber of Times Event Occurred​

In this scenario, a  _trial_  is a single run of our experiment (two coin flips). So, the probability of two heads on two coin flips is approximately:

2521000=.252P(HH)=1000252​=.252

Based on these 1000 trials, we would estimate there is a 25.2 percent chance of getting two heads on two coin flips. This is great! However, if we do this same procedure over and over again, we may get slightly different results. For example, if we repeat the experiment another 1000 times, we might get two heads only 24.2 percent of the time.

If we want to feel confident that we are close to the true probability of a particular event, we can leverage the  _law of large numbers_.

#### Law of Large Numbers

We can’t repeat our random experiment an infinite amount of times (as much FUN as that would be!). However, we can still flip both coins a large number of times. As we flip both coins more and more, the observed proportion of times each event occurs will converge to its true probability. This is called the  _law of large numbers_.

Let’s observe the law of large numbers in real-time. We will use Python to simulate flipping both coins as many times as we want and watch the proportion of two heads converge to its true probability.

Let’s walk through each part of the code below one step at a time. You do not need to worry about every line of code, but understanding the overall objective will help you build your understanding of probability.

Coding question

In the code editor below, we have written out a function called  `coin_flip_experiment()`  that simulates flipping two fair coins. Using a  `for`  loop we run  `coin_flip_experiment()`  a specific number of times. As this loop iterates, we track how often both coins come up as heads. Finally, using matplotlib, we plot the proportion of experiments resulting in two heads after each trial.

The number of times  `coin_flip_experiment()`  runs is determined by the  `num_trials`  variable on line 21. Currently, this variable is set to 5. Run the program a few times. On the resulting plot, the orange horizontal line is the true probability of observing two heads (0.25). The blue line is the proportion of heads we see throughout our trials. What do you notice about the blue line after each run?

You should see that the proportion of two heads after five trials is inconsistent. In some experiments, we may see zero observations of two heads, while in others, we may see almost all five observations are two heads. To simulate the law of large numbers, we need to do more trials. Set the  `num_trials`  variable to different values, such as these below:

-   100
-   1000
-   100000

Take note of what you observe. Where does the blue line on the graph converge to after many trials?

# checking if both flips are heads

if  coin1_result == 'Heads'  and

coin2_result = np.random.choice(coin2)

coin1_result = np.random.choice(coin1)

# "flipping" both coins randomly

coin1 = ['Heads', 'Tails']

coin2 = ['Heads', 'Tails']

def coin_flip_experiment():

# defining our two coins as lists

import  codecademylib3

import  matplotlib.pyplot  as  plt

import  numpy  as  np

Run

Check answer

After setting  `num_trials`  to large numbers, we see that the proportion of trials resulting in two heads converges to 0.25. The horizontal line at  _y=0.25_  is completely covered after about one hundred thousand flips. By simulating a huge number of flips in Python, we have shown that the true probability of seeing two heads on two separate coin flips is equal to 0.25.
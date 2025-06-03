# Understanding Nuclear Decay and Diffusion Phenomena with Dice: Presentation Script

## Slide 0: Title

Hello everyone! Today I'll be talking about "Understanding Nuclear Decay and Diffusion Phenomena with Dice." I hope you'll appreciate the power of understanding physical phenomena through simple models.

## Slide 1: Self-introduction

I'm a freelance software engineer, normally working with computer vision, geographic information processing, and cloud infrastructure. I'm also enrolled in an online university as a working student.

## Slide 2: Today's Topics

Today I'll be discussing:

1. A simple game where we move balls based on dice rolls
2. How this game can reproduce nuclear decay and diffusion phenomena
3. The power of understanding physical phenomena through simple models

## Slide 3: Modeling Nuclear Decay

Let me start with the first example: nuclear decay.
Surprisingly, we can reproduce phenomena like nuclear decay using a simple dice game.

## Slide 4: Review of Nuclear Decay

Let's first review what nuclear decay is. Nuclear decay occurs when radioactive materials emit radiation, and the atomic nuclei that emit radiation transform into stable nuclei.

## Slide 5: Rate of Nuclear Decay

The number of radioactive isotopes decreases exponentially: N of t equals N sub zero times e raised to the power of negative lambda times t.
The time it takes for the number of radioactive isotopes to decrease by half is called the half-life T one-half. This half-life varies depending on the radioactive isotope.

## Slide 6: Reproducing Nuclear Decay with Dice

Now, let's reproduce this nuclear decay using dice.

Imagine a box containing N sub zero balls. We roll a die, and if it shows an even number, we remove the ball; if it shows an odd number, we leave it in the box. We perform this operation for all balls.
Let's think about how the balls will move when we perform this operation.

## Slide 7: Decrease in Balls After One Operation

In this example, the probability of a ball being removed is p equals one-half, and the probability of it remaining is one minus p equals one-half.

Since this one-half value doesn't have any specific meaning, 
I'll simply write it as p from now on.

After one operation, the number of balls will be:
N sub one equals N sub zero minus N sub zero times p equals N sub zero times open parenthesis one minus p close parenthesis
Due to the randomness of the dice, there may be slight variations,
but if N sub zero is sufficiently large, these variations can be ignored.
N sub zero times p balls are removed from the box, and N sub zero times open parenthesis one minus p close parenthesis balls remain in the box.

## Slide 8: Decrease in Balls After the Second Operation

What happens if we repeat the same process?
After the first operation, we had N sub zero times open parenthesis one minus p close parenthesis balls left.
The same thing happens in the second operation, so after two operations, the number of balls will be:
N sub two equals N sub zero times open parenthesis one minus p close parenthesis squared
We simply multiply by open parenthesis one minus p close parenthesis again.

## Slide 9: Repeating the Same Operation

It becomes clear that we can perform the same calculation no matter how many times we repeat this operation.
Since it's the exact same process repeated, after n operations, the number of balls will be:
N sub n equals N sub zero times open parenthesis one minus p close parenthesis raised to the power of n

## Slide 10: Generalizing the Dice Game

Let's say we perform this operation lambda times with a frequency of delta t. We define time t equals n times delta t and p equals lambda times delta t.
Our previous example can be considered as the case where lambda equals 1 and delta t equals 1.

The number of balls at time t is:
N of t equals N sub zero times open parenthesis one minus p close parenthesis raised to the power of n equals N sub zero times open parenthesis one minus lambda times delta t close parenthesis raised to the power of n

## Slide 11: Limit of the Exponent

Let's recall this formula:
The limit as n approaches infinity of open parenthesis one minus x divided by n close parenthesis raised to the power of n equals e raised to the power of negative x

Don't you think we can apply this formula to our equation?
N of t equals N sub zero times open parenthesis one minus lambda times delta t close parenthesis raised to the power of n equals N sub zero times open parenthesis one minus lambda times t divided by n close parenthesis raised to the power of n

## Slide 12: Reproducing Nuclear Decay

The parameters delta t and n were introduced for modeling purposes.
It's natural to want to eliminate these two parameters and derive an equation that only contains the physically meaningful time t.

If we let delta t approach zero and allow n to change so that t converges, we get:
N of t equals N sub zero times e raised to the power of negative lambda times t

This matches the nuclear decay equation!
We've successfully reproduced nuclear decay with our dice game.

## Slide 13: Half-life

Recalling the definition of half-life T one-half,
it's the time it takes for the initial number of balls N sub zero to decrease to half, N sub zero divided by 2.
Applying this:

N of T one-half equals N sub zero divided by 2 equals N sub zero times e raised to the power of negative lambda times T one-half
T one-half equals natural logarithm of 2 divided by lambda

The half-life can be interpreted as the inverse of "the frequency of dice rolls lambda"!

## Slide 14: Modeling Diffusion Phenomena

Nuclear decay isn't the only physical phenomenon we can reproduce with such dice games.
In fact, diffusion phenomena can also be reproduced with a similar game.
Let's examine this in detail.

## Slide 15: Review of Diffusion Phenomena

Imagine dropping a drop of ink on a piece of gauze.
Initially, only the area where the ink was dropped is stained,
but the ink diffuses through the gauze, and the stain gradually spreads.
This is a typical diffusion phenomenon.

## Slide 16: Diffusion Equation

Diffusion phenomena are described by this partial differential equation, called the diffusion equation.

Here, D is the diffusion coefficient, and rho is the concentration.
As an initial condition, we set the distribution function at time t equals zero as Dirac's delta function.

## Slide 17: Solution to the Diffusion Equation

In this case, the solution to the diffusion equation is a Gaussian distribution:
The standard deviation increases with time t, and the rate of increase is determined by the diffusion constant D.

## Slide 18: Reproducing Diffusion with Dice

Now, let's reproduce this diffusion phenomenon using dice.

At time t equals zero, all balls are at the origin x equals zero. We move the balls based on the dice roll:

- If 1 or 2 is rolled, move plus a (probability p)
- If 3 or 4 is rolled, move minus a (probability p)
- If 5 or 6 is rolled, don't move (probability one minus two times p)

This is a very simple rule, just like the nuclear decay we explained earlier.

## Slide 19: Movement of Balls After One Operation

What happens after performing this operation once for all balls, after time delta t?
If we denote the density of balls as rho of t comma x, the density after delta t is represented by this equation.
It expresses that with probability p, the balls go right; with probability p, they go left; and with probability one minus two times p, they don't move.

## Slide 20: Repeating the Same Operation

As with nuclear decay, we consider repeating this operation.
If the density of balls at time t is rho of t comma x, the density at time t plus delta t can be written like this.
The basic concept is exactly the same.
Our goal is to eliminate the arbitrarily introduced parameters delta t and a from this equation.

## Slide 21: Taylor Expansion of Ball Density

Using Taylor expansion, we can rewrite the partial differential equation as follows.

For the time derivative, we use up to the first-order term.
For the spatial derivative, we use up to the second-order term.
This might seem like an odd logical development, but it actually explains diffusion phenomena well.

## Slide 22: Deriving the Diffusion Equation

We substitute the Taylor expansion into the equation for ball density.
If we set the diffusion coefficient to converge to D equals p times a squared divided by delta t as delta t approaches zero,
this matches the solution to the diffusion equation!
We've successfully reproduced diffusion phenomena with our dice game.

## Slide 23: Physical Meaning of the Diffusion Coefficient

Let's delve a bit deeper into the meaning of this diffusion coefficient.
The diffusion coefficient D represents the speed of diffusion. The larger the diffusion coefficient, the faster the diffusion, and the larger the probability p, the larger the diffusion coefficient.
When the time interval delta t approaches zero, we assumed that a behaves such that the diffusion coefficient converges to D equals the limit as delta t approaches zero of p times a squared divided by delta t.
The question naturally arises as to whether this assumption actually holds,
but from a physics perspective, it's natural to think that if it accurately reproduces physical phenomena,
then something that makes it valid is at work.

## Slide 24: Additional Notes

I've explained using somewhat forced logical developments and assumptions,
but the mathematical rigor is actually guaranteed by "Itô's formula."
I'll skip the details today, but I hope to talk about Brownian motion in the future.

## Slide 25: Summary

To summarize today's talk:
We confirmed that with a game where balls are moved based on dice rolls, we can reproduce physical phenomena such as:

- Nuclear decay
- Diffusion phenomena

These facts demonstrate that we can understand the essence of physics with simple models,
and that even complex physical phenomena can be described by extremely simple models.

I believe this is an excellent example of how, when studying and researching physics,
bold simplification can be a shortcut to understanding the essence.

## Slide 26: 2025 Boltzmann Medal

There's some wonderful news regarding such mathematical models.

Professor Yoshiki Kuramoto, a Japanese physicist who proposed the "Kuramoto model" that reproduces synchronization phenomena,
has been awarded the 2025 Boltzmann Medal!
The Boltzmann Medal can be considered the most prestigious award in the field of thermodynamics and statistical mechanics.
The award recognizes his achievements in developing numerous theories that universally and simply describe complex physical phenomena,
with the Kuramoto model being one of his important research contributions.
By developing mathematical models like the ones we considered today, one can reach the forefront of global research.

The Kuramoto model is applied not only in physics but also in biology, engineering, and social sciences.
The video of metronomes synchronizing is fascinating, so please check it out.
I hope to talk about this sometime as well.

## Slide 27: References

- A. Murray and I. Hart, "The 'radioactive dice' experiment: why is the 'half-life' slightly wrong?"
  - A paper explaining how nuclear decay can be reproduced by a dice game with a sufficient number of trials

- Haruaki Tasaki, "Brownian Motion and Non-equilibrium Statistical Mechanics"
  - Has a very clear explanation of diffusion phenomena through Brownian motion

## Slide 28: Call for LT Speakers

The Physics Meeting is looking for LT speakers! Any genre is welcome.
If we don't get any submissions, the organizer will have to do another "LT" (which is actually just a solo recital)...
If you're interested, please contact us on the Physics Meeting Discord server!

## Slide 29: Announcements

The next meeting is scheduled for May 31st.
In addition to LTs, we also welcome suggestions for physics videos on YouTube that you'd like to watch together!

This concludes my presentation. Thank you for your attention! 
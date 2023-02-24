---
title: 'Virtual voltage clamp'
date: 2021-03-12
header:
permalink: /posts/2021/03/virtual-voltage-clamp/
tags:
  - research
  - voltage-clamp
  - patch-clamp
  - artefacts
  - electrophysiology
  - app
---

An online app to simulate a patch-clamp voltage-clamp experiment:
[virtual-voltage-clamp.up.railway.app](https://virtual-voltage-clamp.up.railway.app/) or [virtual-voltage-clamp.onrender.com](https://virtual-voltage-clamp.onrender.com/).


Voltage clamp
======

Our heart and many other muscles are 'controlled' via (bio-)electrical signals.
Electric pulses are effectively what our body use to tell our muscle cells when to contract, similarly for how neurons 'communicate' within our body;
these cells are called '[excitable cells](https://en.wikipedia.org/wiki/Membrane_potential)'.
Understanding the basic mechanisms of these cells is vital to many medical applications &mdash; the study of electrophysiology.
Membranes of these excitable cells contain many different kinds of [ion channels](https://en.wikipedia.org/wiki/Ion_channel) which carries the current of the cell.
Some of these ion channels are voltage-dependent;
often we want to learn how these channels (and their currents) reacts to voltage changes.
[Voltage clamp](https://en.wikipedia.org/wiki/Voltage_clamp) is perhaps one of the most important experimental methods for studying these excitable cells;
it _attempts_ to measure the currents through the membranes of these cells, whilst holding the membrane voltage at a fixed level.


How does it work?
------
If we inject a current into a cell, it will change the membrane potential (voltage) of the cell.
The basic idea of a voltage clamp is to iteratively measure the membrane potential, and then add in the necessary current to bring the membrane potential to a desired level.
The current applied to the cell is in fact equal to (with the opposite sign/direction of) the current going across the cell membrane at the set voltage.
Then we have achieved the goal: holding the membrane potential whilst measuring the current of the cell responding to it.


All good then?
------
Well, not quite...
If there is absolutely zero-resistance between the voltage-clamp machine ([amplifier](https://en.wikipedia.org/wiki/Negative-feedback_amplifier)) and the cell, then everything will be fine.
However, any (electric) resistance sits between the machine and the cell (which there is!) will take up the current that the machine is injecting into the cell, causing the voltage not properly clamped at the desired level.
Also, this whole idea of voltage clamp is effectively based on a feedback system, which relies heavily on how quickly the system (both the machine and the cell!) can response to a change.
There are capacitors within this feedback system, together with some resistors, forming an RC-circuit which introduces some form of ''time-delay'' between its input and output when a voltage is applied to it.
And these capacitors also draws what is called a ''charging current'' or gives a ''discharge current'', which contaminates the recorded current.
Therefore, the measurements using voltage clamp &mdash; both the voltage that we set and the current that we record &mdash; become not quite the same as what we want to measure.


The end of the (voltage-clamp) world?
------
No again.
Smart scientists/engineers who built these voltage clamp machines came up ways to compensate some of these undesired effects.
For example, if you tell them what the total resistance that sits between the machine and the cell is, they can calculate and add some extra current in to compensate the current loss before reaching the cell.
And if you tell them what the capacitance is, they can inject more current to speed up the ''time-delay'', and they can also subtract off the (dis-/)charging current from the recordings.
This gets us closer to what we intended to measure.


Are we close enough to the ideal?
------
No.
I mean, I don't know.
It all depends on what we are trying to learn from the experiments.
So I can't tell you for sure whether the compensation is good enough, but I can instead tell you how close you are to the ideal case.
[Our study](https://doi.org/10.1098/rsta.2019.0348)<sup>1</sup> developed a mathematical model for the entire voltage-clamp experiment.
We can simulate what is happening in the voltage-clamp experiments, and we can readout, study and analyse things that cannot be observed in the actual experiments, such that we can have a better idea of whether we are happy with what we measured in the experiments.

The model that we developed is deployed on
[virtual-voltage-clamp.up.railway.app](https://virtual-voltage-clamp.up.railway.app/) and [virtual-voltage-clamp.onrender.com](https://virtual-voltage-clamp.onrender.com/)<sup>2</sup>,
so that everyone can play around with different settings/conditions of the experiment and see how the ideal case differs from the observation.
Have fun and enjoy _virtual voltage clamping_!


<sup>1</sup> Lei _et al._ 2020, _Phil. Trans. R. Soc. A._ 378:20190348. [doi:10.1098/rsta.2019.0348](https://doi.org/10.1098/rsta.2019.0348).

<sup>2</sup> (_edited: 2023-02-23_) It used to be [virtual-voltage-clamp.heroku.com](https://virtual-voltage-clamp.heroku.com/) but since November 2022, [Heroku](https://heroku.com/) has removed all free deployment, therefore we are now deploying on [Railway](https://railway.app/) (with 500 hours (~21 days) per month) and [Render](https://render.com/) (with downtime and much slower).

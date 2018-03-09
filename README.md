# Pulse2
An 18-state CA for making logic gates with (relative) ease

This rule was created out of the desire to make logic gates that are small, have an easy to learn ruleset, and also run fairly quickly. The "2" in the name is because this is the second of two CA's; the old one was very similar but was cumbersome to use. 

I might add some more states to support polymorphism and self-replication, but I'm not entirely sure how to go about it without doubling the state count or adding diagonals to the neighborhood.

## Instructions

To run the examples, download Golly (http://golly.sourceforge.net), download this repository and move it inside the Golly directory, and copy the .rule files into the Rules folder.

You can also simply copy-paste the raw .rule files into an open Golly window to install the rule, and copy-paste the example files into a blank universe to load them.

## Details

Pulse2 revolves around two types of pulses, "gate" and "signal". Gate pulses are used to toggle gates, which transmit or block signals. Signal pulses do nothing, but can be converted into gate pulses. Pulses always propogate to directly adjacent cells that will accept them.

There are six basic types of cell:

|# |Color |Name    |Description                          |
|--|------|--------|-------------------------------------|
|0 |black |Empty   |Never changes.                       |
|3 |green |On gate |Accepts gate and signal pulses.      |
|8 |red   |Off gate|Accepts gate pulses.                 |
|11|cyan  |Setter  |Turns signal pulses into gate pulses.|
|14|yellow|Getter  |Turns gate pulses into signal pulses.|
|17|blue  |Wire    |Carries signal pulses.               |

Every other state is a state of excitation, and represents a gate or signal pulse.
Note that green gates have both gate pulse (1 & 2) and signal pulse (4 & 5) states. Gate pulses override signal pulses.

## Examples

Several examples have been included, including a working microprocessor! See [examples.md](examples.md) for more info.

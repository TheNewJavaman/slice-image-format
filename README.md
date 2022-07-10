# slice-image-format

## Introduction

The Slice Image Format (SIF) is a digital compression scheme best suited for data that is primarily composed of
gradients or curves. Examples include real-world images, simulated three-dimensional environments, or other situations
in which lighting causes a general smoothing effect.

## Overview

Encoder process:

1. "Slicing" (segmenting) data into one-dimensional rows
2. Identifying "stops" (sharp cutoffs between intervals of similar points along the slice)
3. Approximating each interval as an independent mathematical function, usually using a simple quadratic equation

Decoder process:

1. Evaluate each interval for the specified number of points
2. Join together the intervals into a slice
3. Join together the slices into the final data structure

## Future Development

It is possible to express intervals along multiple axes using a single equation; consequently, it may be feasible to
approximate a 2D interval (to do: think of proper name) using a single equation, which would greatly increase storage
efficiency.

## Rights

SIF is currently a work in progress, and was first invented by Gabriel Pizarro on July 8, 2022, at 10:57 PM after waking
up from a bad dream. As far as I am aware, there are no existing data formats that use this technique. All rights are
reserved for this invention. No other parties have permission to use this idea.

## Technique

Let's begin with the most common form of an image-data problem. There is a two-dimensional grid of pixels that each have
their own colors. The most common way to store these colors on modern computers is via RGB (red, green, blue) channels.
Other color spaces exist, including YCbCr (luma, chroma blue, chroma red). Most commonly, each channel holds eight bits
of data, allowing for a range from 0 through 255. Most images do not need to actually store this much data, however.
Other image compression algorithms may approximate

## File Format

---
date: 2016-04-25T11:47:32+02:00
title: Entropy
type: page
---

## What the hell is entropy?

> In computing, entropy is the randomness collected by an operating system
> or application for use in cryptography or other uses that require random
> data. This randomness is often collected from hardware sources, either
> pre-existing ones such as mouse movements or specially provided
> randomness generators. A lack of entropy can have a negative impact on
> performance and security.

Have you ever tried to generate a `ssh` key and ran out of entropy?
Your system maintains and refills entropy from various sources. Key
strokes, mouse movement, disk activity. Basically, everything that can be
measured in a non-deterministic way.

For example you can act completely retarded by collecting entropy with an
accelerometer.

<center>
{{< figure src="/img/1.gif" >}}
</center>

If you really wanna know how to deal with entropy nicely and how it evolved
watch [Randomness: how arc4random has grown since
1998](https://www.youtube.com/watch?v=gp_90-3R0pE) (OpenBSD).
A short summary of how different operating systems deal with randomness can be
found on [Wikipedia](https://en.wikipedia.org/wiki/Entropy_(computing)).
There are also some new interesting ideas for the Linux kernel see
[lwn.net](http://lwn.net/Articles/691941/).



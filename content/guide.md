---
date: 2016-04-25T11:47:32+02:00
title: Guide
type: page
---

## How to build your own organic entropy harvester

To collect all those information from the environment, you need some fancy
devices. We chose [tinkerforge](https://tinkerforge.com) for easy
assembling without the soldering and so-called "fun".

### Sensors (Bricklets)

All you need are the following sensors: [Accelerometer](https://www.tinkerforge.com/en/shop/bricklets/accelerometer-bricklet.html),
[Temperature](https://www.tinkerforge.com/en/shop/bricklets/sensors/temperature-bricklet.html),
[UV light](https://www.tinkerforge.com/en/shop/bricklets/sensors/uv-light-bricklet.html),
[Sound intensity](https://www.tinkerforge.com/en/shop/bricklets/sensors/sound-intensity-bricklet.html)
and one
[Masterbrick](https://www.tinkerforge.com/en/shop/bricks/master-brick.html)
to connect them all together. Right after that, you purchase an RaspberryPI
and attach the entropy milking machine to it.

{{< figure src="/img/3.jpg" class="img-responsive">}}

Other sensors are possible. If you live in Fukushima or near Chernobyl, you
propably like to attach a [Geiger counter](https://en.wikipedia.org/wiki/Geiger_counter). Some others living in Tokyo may find a [dust
sensor](https://www.tinkerforge.com/en/shop/bricklets/sensors/dust-detector-bricklet.html)
interesting. Just use whatever humanity did/gave to you.

This is probably the most expensive `GPG` key you will ever generate. But
hey. You also pay extra for organic food!

### The Harvestor

Set up your RaspberryPi and
[brickd](http://www.tinkerforge.com/en/doc/Software/Brickd_Install_Linux.html#brickd-install-linux).
The secure harvesting software (multiple times audited by the council of
the elder hedgehogs) has to be installed on the system.

``` bash
$ sudo pip install tinkerforge
$ git clone https://github.com/noqqe/organic-entropy
$ cd organic-entropy
$ ./harvestd > /mnt/entropy.txt
```

You probably want to configure this daemon to be started automatically in
some way. I'm sure you will find a way. You're a big boy.

## How to collect entropy

You are done! Go out and collect some green-bio-organic-superfair-traded
entropy!

To give you some inspirations:

{{< figure src="/img/5.jpg" class="img-responsive">}}
<center>
{{< figure src="/img/7.jpg" class="img-responsive">}}
</center>
{{< figure src="/img/12.jpg" class="img-responsive">}}

### How to insert...

After a hard day out on the field. There's nothing better than enjoying the
fruits of your work. Grab the SD-Card of your RaspberryPI and plug(&pray)
it into your laptop.

```
$ git clone https://github.com/noqqe/organic-entropy
$ cd organic-entropy/add_entropy
$ make
```

Go ahead and finally get the entropy into the system!

```
$ cat /proc/sys/kernel/random/entropy_avail
> 608
$ cat /mnt/sdcard1/mnt/entropy.txt | ./rndaddentropy
$ cat /proc/sys/kernel/random/entropy_avail
> 3982
```

Doesn't it feel great? Come on. It does! Feel it.

### End

Congrats! You supplied real organic entropy to your system. How wonderful
is that? It's really important to tell all your friends that you collect
entropy by yourself. There's absolutely no necessity if the topic of the
conversation is related anyhow. Quite the opposite!

And if you're vegan its even better. You can combo organic entropy with
stating that you're a vegan guy and growing a beard. Multi-Annoyance!

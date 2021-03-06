Graffiti Netplay Enhancement
============================

Graffiti allows you to draw on the surface of your game. It can be used locally
or during netplay. It is intended to be a fun addition to the netplay experience.

![graffiti gameplay example](./pics/mednafen-graffiti1.png)



Trying it out
=============

First you'll need a binary of this software. That likely means you'll have to build it yourself. See the **Building** section below.

Once you've opened a ROM up (eg. `mednafen mario.smc`), you can immediately begin testing the graffiti feature! Now, it's most fun with a friend online, but you can run it locally too.

### Testing locally

First, press 't' to get a console prompt, then type `/g on` to enable graffiti mode. Now, when your mouse is over the game screen, you see a black square. You can now do the following:

- Left-Click and Drag: Draw
- Mouse Wheel: Change brush size
- Right-Click and Drag: Erase

### Playing Online

Make sure that both you and your buddy have Graffiti, and an identical copy of the game you're gonna play. Once you open the rom up, press 't' to get a console prompt, then type `/connect` to connect to mednafen's server. Once connected, the graffiti feature will automatically become activated. Once your friend joins the game, you can use 't' to chat with each other, and also have fun playing with graffiti together!


Building
========

When building directly from git, run the following commands from the project directory:

```
aclocal -I .; autoconf; automake --add-missing -c
./configure
make
sudo make install
```

About The Implementation
========================

When I aspired to create the graffiti feature, I knew for it to be successful, it had to simply work with the pre-existing netplay servers. This meant opting for an implementation that takes place completely over the client. By having it done this way, there was no need to require a custom server. It *just worked*.
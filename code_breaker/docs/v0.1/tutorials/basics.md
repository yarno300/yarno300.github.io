---
hide:
  - navigation
---


# Basic rendering tutorial

## Introduction
This is a tutorial so you would understand the basics of the engine and how it works. In this tutorial we will learn how to render a window and draw some images on it. If you want to learn more, then go to [our docs](https://yarno300.github.io/code_breaker/docs/index.html) and select wiki.

This tutorial also expect you to have everything setup, if not, head over to [tutorial 1: setting everything up](setup.md)

## Creating a window

So if you read tutorial 1 you know we have the main variable running our engine object. So now we create a window with the help of that main object:
```python
window = cb.Window("Tutorial 2", 600, 600)
```
The first argument that we give our function is our title, second argument is our width and third one is height

## Pre-loading image
We will now pre-load a image so we can draw it later on our window. We do it like this:
```python
image = cb.Image(window, cb.DEBUGIMAGE, 0, 0, 600, 600)
```
Fist argument is our window, second is our image path, third is our x position, fourth is our y position, fifth is our width and sixth is our height. As you maybe see were using cb.DEBUGIMAGE, which is a build in image into our engine for testing purposes. We will use it for our tutorial

## Starting a loop
A loop is basicly what lets our window be open the whole time and not be automaticly closed. You also run there functions that need to ran every frame. So we start a loop like this:
```python
@window.loop
def loop():
	... # Code goes here

```

## Drawing image
So we still need to draw our image after loading it, and you can do that easily inside a loop like this:
```python
@main.window.loop
def loop():
    image.draw()

```
As you see we have a draw function in our loop with the image loaded image as base (object).

## Full code
Here is our full code that we could through this tutorial:
```python
import code_breaker_engine as cb

window = cb.Window("Example: 1", 600, 600)
image = cb.Image(window, cb.DEBUGIMAGE, 0, 0, 600, 600)


@window.loop
def loop():
    image.draw()

```

## Ending
This was our basic tutorial to images. There are (or will be) more tutorials, so check them our. Or otherwise you could check our [docs](<https://yarno300.github.io/code_breaker/docs/index.html>) for more information. Happy coding!


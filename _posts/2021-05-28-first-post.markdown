---
layout: post
title:  "First Post...What is an Image? What is Noise?"
date:   2021-05-28 16:13:23 -0600
categories: introcv
---
This is my first post, so I thought I'd jot down some notes about Computer Vision basics. I'll also add simple MATLAB code snippets here and there that I could foresee myself using fairly often in the future. To start off, here are some key takeaways, particularly about how to view images mathematically:

*  An image can be defined as a function; you could think of an image as an object within a 2D coordinate system with an intensity at each point, f:R^2->R
* A color image can be defined as a function, f: R^2->R^3, with color planes r, g, b

<strong>Loading Images and Inspecting its Values in MATLAB</strong>

In the code snippet below, I give an example of how you can load an image in MATLAB and extract some data from the image. Keep in mind that the data type determines the max intensity of each coordinate. That means if the data type is a uint8, then the max intensity would be 2^8-1=255 (pretty common knowledge). Also, the image size is given as [height, width, # color planes] in Matlab.

{% highlight matlab %}
%load an image
img = imread('example.png');
imshow(img);

%image size
disp(size(img));

%img class or data type:
disp(class(img));

%value at a given location (row, col):
disp(img(15, 200));

%plot value from an entire row:
plot(img(15, :));
{% endhighlight %}

<strong>Noise in An Image</strong>
*  Noise in an image can be written as a function I'(x,y) = I(x,y) + n(x,y), where I(x,y) represents the original function and n(x,y) the noise 
*  Gaussian noise is the most common type

Below is a snippet of code I wrote in MATLAB that demonstrates how to generate gaussian noise and apply it to an image.
{% highlight matlab %}
%load an image
img = imread('example.png');

%generate gaussian noise
sigma = 64;
noise = uint8(randn(size(img)).*sigma);

%display noisy image
output = img + noise;
imshow(output);
{% endhighlight %}

And voilà! We can display both figures and get the following images generated from the MATLAB code.

Before:
![Before](/assets/example_before.png) 

After:
![After](/assets/example_after.png)

Stay tuned for tomorrow's post where I'll be covering <strong>Filtering</strong> and talking more <strong>Noise</strong>!





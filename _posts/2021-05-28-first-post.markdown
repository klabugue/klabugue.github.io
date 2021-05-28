---
layout: post
title:  "First Post and Computer Vision Basics"
date:   2021-05-28 16:13:23 -0600
categories: cvnotes
---
This is my first post! I thought I'd take down some notes about Computer Vision basics and how we could think about images as functions. Here are some key takeaways:

*  An image can be defined as a function; you could think of an image as a 2D object within an XY axis and with an certain intensity at each point in the coordinate system, f:R^2->R
    * A color image can also be defined as a function, f: R^2->R^3, with chanels r, g, b
*  second item
*  third item
Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

---
layout: post
title: The Second Circle Of Vagrant Hell
category: technical
description: I went back and forth in a nightmare, and brought back some solutions.
tags: Poetry
---

This is a fake post to test syntax highliting

The FizzBuzz test is common to separate people on their coding capabilities.

#### FizzBuzz in Ruby
{% highlight ruby %}
1.upto(100) do |num|
  if num % 5 == 0 and num % 3 == 0
    puts 'CocaCola'
  elsif num % 5 == 0
    puts 'Cola'
  elsif num % 3 == 0
    puts 'Coca'
  else
    puts num
  end
end

{% endhighlight %}

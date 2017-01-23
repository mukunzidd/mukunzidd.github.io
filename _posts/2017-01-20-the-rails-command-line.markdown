---
layout: post
title:  "The Rails Command Line"
date:   2017-01-21
---

<p class="intro"><span class="dropcap">R</span>ails is on of the popular fullstack web framework. Rails is powered by <a href="https://www.ruby-lang.org/en/">Ruby</a> programming language, which known to be built with the programmer in mind.</p>

When building web applications with Ruby on Rails, it is of great importance that you get familiar with the most important _Rails Command Line Commands_ that you are going to using almost in all projects.

There are a few commands that are absolutely critical to your everyday usage of Rails. In the order of how much I use them are:

- rails console
- rails server
- rake db:migrate
- rails generate
- rails new app_name


## _Rails Commands Explained_

##### rails new you_app_name

Use this command in the terminal in a directory where you want create your new rails application.

{% highlight rails %}
rails new your_app_name
{% endhighlight %}

##### bundle install or just bundle

Rails is awesome guys it even provide shorthand for most of the commands, _did you notice railss c can be used in place of rails console?_. Okay, enough of me talking! 

Use this command in the terminal in a directory where you created your new rails application to install rails dependencies defined in the Gemfile at the root of your application.

{% highlight rails %}
bundle install
{% endhighlight %}

You can run <code>bundle check</code> to check if you have installed all of your dependecies.

{% highlight rails %}
bundle check
{% endhighlight %}

_If you have run bundle install with success you will see this message_
{% highlight rails %}
The Gemfile's dependencies are satisfied
{% endhighlight %}

##### rails generate or just rails g

Use this command inside the directory of your application. This is the command that triggers rails generator to create files and folders as you instructed. This command is used for a variety of awesome rails features like generating: a controller, a model, a scaffold, and so on. 

{% highlight rails %}
rails g controller controller_name action_name
{% endhighlight %}
_Remember that its always healthy to pluralize your controlers._

{% highlight rails %}
rails g model ModelName attribute:type attribute:type
{% endhighlight %}

{% highlight rails %}
rails g scaffold ScaffoldName attribute:type attribute:type
{% endhighlight %}

*Note:*
_Always remember to run <code>rake db:migrate</code>  everytime 	        you generate a model or a scaffold in order to add your      model to whatever the database you are using._


##### rails console or rails c

Use this command to get into the rials console where you can test your code. This is where the magic happens.

{% highlight rails %}
dodo@dodo-HP-Notebook:~/rails$ rails c
Loading development environment (Rails 5.0.1)
irb(main):001:0> 
{% endhighlight %}



##### rails server or rails s

Run this command in order to run the rails server. If you didn't mess up with the rials configuration file, you will be able to view your app on [http://localhost:3000].
{% highlight rails %}
dodo@dodo-HP-Notebook:~/rails/ rails s
=> Booting Puma
=> Rails 5.0.1 application starting in development on http://localhost:3000
=> Run `rails server -h` for more startup options
Puma starting in single mode...
* Version 3.6.2 (ruby 2.3.3-p222), codename: Sleepy Sunday Serenity
* Min threads: 5, max threads: 5
* Environment: development
* Listening on tcp://localhost:3000
Use Ctrl-C to stop
{% endhighlight %}

_If you see this open browser to localhost:3000 and Voila!_






Check out the official [Rails Command Line Docs](http://guides.rubyonrails.org/v3.2/command_line.html) for more commands and detailed usage.

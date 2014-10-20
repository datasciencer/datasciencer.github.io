---
layout: post
title:  "My first blog"
date:   2014-10-19 18:20:11
categories: blog
---

Finally, I have a blog run on Jekyll and Github. In my case, the simplest way is using pure Jekyll. Others solutions such as Octopress or Jekyllbootstrap have cost me a lot energy and time. Moreover, I felt that these latters have taken away from the UNIX's KISS principle. What please me the most with pure Jekyll is the Spartan configurations. Everythins is about the contents, the appearance is reduced to the strict necessary.

Here are steps (in my case) to lauch the [datasciencer] blog:

* Pre-install nodejs to have a javascript instant : sudo pacman -S nodejs
* Create within my Github account the repository *datasciencer.github.io*
* Add the public ssh key to this repository inside Settings/Deploy key. The key is show by enter this command line inside the terminal : cat .ssh/id_rsa.pub
* Let's start now by creating the jekyll blog : 
	* source .bash_profile
	* gem install jekyll
	* jekyll new datasciencer.github.io
	* jekyll serve
	* cd datasciencer.github.io
	* git remote set-url origin git@github.com:datasciencer/datasciencer.github.io.git
	* git add .
	* git commit -m "first commit"
	* git pull
	* git push origin master


Let's check if jekyll could highlight R code

{% highlight R %}

packages_vec <\- c('reshape2', 'ggplot2', 'XLConnect', 'dplyr')
lapply(packages_vec, require, character.only=T)

{% endhighlight %}


In case of multi-github-accounts: follow [this link](http://code.tutsplus.com/tutorials/quick-tip-how-to-work-with-github-and-multiple-accounts--net-22574) : 

* Generate a key for each repository of different github accounts
* Create a config file inside .ssh/ for ghaccount-1 and ghaccount-2
* Inside each origin folder, for example github account-1, enter this command into the terminal : git remote set-url origin git@ghaccount-1:nameaccount1/nameaccount1.github.io.git



Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
[datasciencer] : http://datasciencer.github.io/

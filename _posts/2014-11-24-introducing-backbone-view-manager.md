---
layout: post
title: Introducing Backbone View Manager
---

![](/public/projects/backbone.viewmanager.png)

Your probably asking yourself why would anyone be releasing a new plugin for managing [Backbone](http://backbonejs.org) views.  Especially now that Backbone is no longer in vogue.  Well, in short, I am still a strong supporter of Backbone. I believe in it's minimal unopionated philosophy.  I prefer frameworks which give each project the most flexibility possible while providing a minimal application structure and utility.  

As a software architect for many different projects, I have been reasonable for making technology decisions as it applies to the software stack.  I have selected to work with everything from very large frameworks [ExtJS](http://www.sencha.com/products/extjs/) to minimal frameworks like Backbone.  As a result, I have come to appreciate the value in flexibility that minimum frameworks provide.  

With this being said, Backbone provides you with many ways to shoot yourself in the foot.  One of them is creating memory leaks in a Backbone application as a result of mismanaged views.   When I searched for a simple solution to this problem I couldn't seem to find something that fit my needs.  This resulted in the creation Backbbone.ViewManager.  Which follows in the footsteps of Backbone and provides a minimal approach to manage views and subviews. It also provides a default rendering implementation just to help cut down on bowler plate code.

View Manager can be used in whole or in parts.  If you think you might be interested in using this plugin, I have several articles to help you get started:

* [Usage Documentation](https://github.com/nnance/backbone-viewmanager/wiki/usage)
* [Slide Presentation](http://slides.com/nicknance/viewmanager/)
* [API](https://github.com/nnance/backbone-viewmanager/wiki/api)

If you find this plugin useful please star the [Github Project](https://github.com/nnance/backbone-viewmanager).  Or better yet [fork it](https://github.com/nnance/backbone-viewmanager) and contribute.

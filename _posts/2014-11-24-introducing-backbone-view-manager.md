---
layout: post
title: Introducing Backbone View Manager
---

You are probably asking yourself why would anyone be releasing a new plugin for managing [Backbone](http://backbonejs.org) views and especially now that Backbone is no longer in vogue.  Well I am still a strong supporter of Backbone as I believe in it's minimal / unopionated philosophy.  I believe in frameworks that give each project the most flexibility possible while providing a minimal application structure while providing functional utility.  

As a software architect for many different projects I have been reasonable for making technology decisions as it applies to the software stack.  I have selected to work with everything from very large frameworks [ExtJS](http://www.sencha.com/products/extjs/) to minimal frameworks like Backbone.  As a result I have come to appreciate the value in flexibilty the minim frameworks provide.  

With this being said, Backbone provides you with many ways to shoot yourself in the foot.  One of them is creating memory leaks in a Backbone application as a result of mismanaging views.   When I searched for a simple solution to this problem I couldn't seem to find something that fit my needs.  As a result, I created Backbbone.ViewManager.  Which follows in the footsteps of Backbone and provides a minimal approach to manage views and subviews. It also provides a default rendering implementation just to help cut down on bowler plate code.

View Manager can be used in whole or in parts.  If you think you might be interested in using my plugin I have several articles that documents the plugin:

* [Usage Documentation](https://github.com/nnance/backbone-viewmanager/wiki/usage)
* [Slide Presentation](http://slides.com/nicknance/viewmanager/)
* [API](https://github.com/nnance/backbone-viewmanager/wiki/api)

If you find this plugin useful please star the [Github Project](https://github.com/nnance/backbone-viewmanager) and your are welcome to contribute.

---
comments: true
date: 2012-03-01 12:51:07
layout: post
slug: links-cheap-wardrobe-app-stores-javascript-parsing
title: 'Links: Cheap wardrobe, App Stores, Javascript & Parsing.'
wordpress_id: 711
categories:
- links
tags:
- apple
- appstore
- clothes
- dressing
- javascript
- led
- lint
- nud
- parser-generator
- parsing
- pinboard-links
- pratt
- programming
- put-this-on
- python
- ties
- tools
- wardrobe
---

My shared links for February 23rd:






  * [Strategic Frugality If you're just starting to build a...](http://putthison.com/post/17161826063) - where you can skimp!


  * [Dealing with Crap apps in the catalog…](http://www.chuqui.com/2012/02/dealing-with-crap-apps-in-the-catalog/) - chuq on the tough problem of policing app stores.


  * [JSLint,The JavaScript Code Quality Tool](http://www.jslint.com/) - From Douglas Crockford


  * [JavaScript Lint](http://www.javascriptlint.com/) - 


  * [Jison](http://zaach.github.com/jison/) - javascript bison with a yacc-alike too


  * [Simple Top-Down Parsing in Python](http://effbot.org/zone/simple-top-down-parsing.htm) - Pratt Parsing in Python. (After Douglas Crockford's Javascript version)

def expression(rbp=0):
    global token
    t = token
    token = next()
    left = t.nud()
    while rbp < token.lbp:
        t = token
        token = next()
        left = t.led(left)
    return left




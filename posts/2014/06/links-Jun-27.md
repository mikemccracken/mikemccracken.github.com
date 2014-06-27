<!--
.. title: Links for June 27, 2014
.. date: 2014-06-27 12:24
.. slug: links-for-June-27-2014
.. tags: , criticism, art, reference, data-structures, tree, app, recipe, sync, culture, haskell, video, oatmeal, fatherhood, racket, research, visualization, paleo, tuning, nikola, housing, octopress, CRDT, writing, maps, music, typesetting, performance, calculator, real, finance, estate, pittsburgh, eventual-consistency, internet, autotuning, acheme, gluten-free, diagram, parenting, cookie, graphics, data, blogging, publishing, plants, quickref, workstation, kids, language, solver, programming, up, analysis, howto, merging, optimization, algorithms, growing, ergonomics, constraints
-->
* [Alloy](http://alloy.mit.edu/alloy/)
	Alloy is a language for describing structures and a tool for exploring them. It has been used in a wide range of applications from finding holes in security mechanisms to designing telephone switching networks.

* [OpenTuner by jansel](http://opentuner.org/)
	"OpenTuner is a new framework for building domain-specific multi-objective program autotuners. OpenTuner supports fully customizable configuration representations, an extensible technique representation to allow for domain-specific techniques, and an easy to use interface for communicating with the tuned program. A key capability inside OpenTuner is the use of ensembles of disparate search techniques simultaneously, techniques which perform well will receive larger testing budgets and techniques which perform poorly will be disabled." -- This looks really useful. I started on something like this long ago at LLNL, but since I was so young I focused mostly on fancy plots and designing a language for describing experiments.

* [Paper to Plants on Vimeo](http://vimeo.com/95534178)
	A really cute video about a game that seems pretty charming. I'm still not sold on little kids using iPads so much, I'm told it's bad for their eye development.

* [Ergonomic Workspace Planner Tool | ComputingComfort.org](http://www.computingcomfort.org/create2.asp)
	Use this to figure out the optimal height of your standing desk

* [pollen](http://mbutterick.github.io/pollen/doc/)
	Write web based books in racket

* [Finding the perfect house using open data — dealloc.me](http://dealloc.me/2014/05/24/opendata-house-hunting/)
	A guy builds a map of available houses in Portland that match his desires. Seems like a good real estate agent should do this for you - but how do you know you've got a good one? I guess you have to write some code.

* [Drawing Presentable Trees](http://billmill.org/pymag-trees/)
	"When I needed to draw some trees for a project I was doing, I assumed that there would be a classic, easy algorithm for drawing neat trees. What I found instead was much more interesting: not only is tree layout an NP-complete problem1, but there is a long and interesting history behind tree-drawing algorithms. I will use the history of tree drawing algorithms to introduce central concepts one at a time, using each of them to build up to a complete O(n) algorithm for drawing attractive diagrams of trees." -- I've always wondered what a good way to do this would be. Knew it had to be a solved problem.

* [Grain-Free Oatmeal Raisin Cookies | Against All Grain - Delectable paleo recipes to eat & feel great](http://againstallgrain.com/2013/10/12/grain-free-oatmeal-raisin-cookies/)
	If you want oatmeal-raisin but you're trying to avoid oats and sugar, these are really quite good. The coconut makes a great texture.

* [Lev Grossman on his daughter, Lily: How being a father ruined my life and made me a better writer.](http://www.slate.com/articles/life/family/2014/06/lev_grossman_on_his_daughter_lily_how_being_a_father_ruined_my_life_and.html)
	A really heartfelt story about becoming a dad and getting your act together. Now that I have kids I'm a total sucker for this kind of article.

* [HAL :: [inria-00555588, version 1] A comprehensive study of Convergent and Commutative Replicated Data Types](http://hal.archives-ouvertes.fr/inria-00555588/)
	Formal exploration of sync-able data types. Abstract: "Eventual consistency aims to ensure that replicas of some mutable shared object converge without foreground synchronisation. Previous approaches to eventual consistency are ad-hoc and error-prone. We study a principled approach: to base the design of shared data types on some simple formal conditions that are sufficient to guarantee eventual consistency. We call these types Convergent or Commutative Replicated Data Types (CRDTs). This paper formalises asynchronous object replication, either state based or operation based, and provides a sufficient condition appropriate for each case. It describes several useful CRDTs, including container data types supporting both \add and \remove operations with clean semantics, and more complex types such as graphs, montonic DAGs, and sequences. It discusses some properties needed to implement non-trivial CRDTs."

* [What I Wish I Knew When Learning Haskell 2.1 ( Stephen Diehl )](http://dev.stephendiehl.com/hask/#intro)
	Nice quick article with practical tips for beginners.

* [Not So Much 'New York Poor' as 'Pittsburgh Rich' - Pacific Standard: The Science of Society](http://www.psmag.com/navigation/business-economics/talent-migration-work-creative-much-new-york-poor-pittsburgh-rich-82894/)
	You can get a lot for your money in Pittsburgh, and lots of other places throughout the US. I'm from Pgh, and have fond memories. I'd consider moving back there if they could fix the weather.

* [Call me maybe: Elasticsearch](http://aphyr.com/posts/317-call-me-maybe-elasticsearch)
	Part of a series of irreverent but thorough explorations of various popular distributed systems.

* [What Do We Save When We Save the Internet](http://m.theatlantic.com/technology/archive/2014/05/what-do-we-save-when-we-save-the-internet/370885/)
	So as you proceed with your protests, I wonder if you might also ask, quietly, to yourself even, what new growth might erupt if we let the Internet as we know it burn. Shouldn't we at least ponder the question? Perhaps we’d be better off tolerating the venial regret of having lost something than suffering the mortal regret of enduring it."

* [Music Animation Machine — "Music Worth Watching"](http://www.musanim.com/)
	Old stuff, but great. Couldn't believe I hadn't bookmarked it long ago.

* [Moving from Octopress to Nikola | serialized.net](http://serialized.net/2013/03/moving-from-octopress-to-nikola/)
	This post and a few tweaks got me into nikola without much hassle.
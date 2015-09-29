---
layout: project
course: intro

number: 1
title: Nursery Rhyme
due: 2015-9-28
turnin: #
forum: https://groups.google.com/forum/#!categories/ihsintrocompsci/project-1---nursery-rhyme

rubric:
  total: 20
  behavior:
    criteria:  
      - criterion: Animation depicts a full nursery rhyme (or approved smaller portion)
        value: 2
      - criterion: Nursery rhyme is shown one line at a time
        value: 2
      - criterion: Each line is accompanied by sprites depicting the story, and all action is related to the current line
        value: 3
      - criterion: Clicking	green	flag	starts	animation	from	beginning
        value: 1
      - criterion: Animation	progresses	at	a	reasonable	pace
        value: 2
      - criterion: User	is	able	to	restart	animation	when	it	concludes
        value: 2
    total: 12
  implementation:
    criteria:
      - criterion: Program shows good creativity and effort
        value: 2
      - criterion: At least two sprites participate in the action
        value: 2
      - criterion: At least one sprite moves
        value: 1
      - criterion: At	least	one	sprite	rotates
        value: 1
      - criterion: At	least	one	sprite	changes	costume
        value: 1
      - criterion: At	least	one	sprite	hides	and/or	appears
        value: 1
    total: 8
---
## Overview
A	nursery	rhyme	is	a	short	poem	or	song	written	for	children.	Though	the	term	is	typically	applied	to	British	or
other	English	language	poems,	similar	concepts	exist	in	many	world	cultures.	These	short	stories	are	generally	
meant	to	entertain	and/or	calm	young	children.	Some	are	believed	to	have	a	hidden	moral	or	meaning	related	
to	historical	events,	but	many	of	these	meanings	are questionable.

## Details

### Behavior
You	will	create	a	short	animation	in	BYOB	depicting	a	nursery	rhyme	of	your	choice.
(See [http://en.wikipedia.org/wiki/Nursery_rhymes](http://en.wikipedia.org/wiki/Nursery_rhymes) for	a	list	of	possibilities.)  Your program should meet the following requirements:

* Whenever	the	green	flag	is	clicked,	your	BYOB	animation	should	display	your	chosen	nursery	rhyme
line	by	line	somewhere	on	the	stage.	(This	should	work	correctly	even	if	the	last	run	was	interrupted	
and	restart.)
* As	each	line	is	shown,	sprites	should	act	out	the	story.
* The	animation	should	advance	on	its	own,	but	should	do	so	at	a	pace	that	allows	each	action	to	
complete	and	the	viewer	to	read	the	line	before	the	next	line	is	shown	and	new	action	begins.
* In	addition,	the	sprites	must	act	out	the	rhyme;	you	should	not	simply	create	a	series	of	static	
backgrounds	or	costumes	that	show	a	stop-motion	version	of	the	story.
* Each	line	must	be	readable	and	must	stay	shown	while	the	corresponding	action	is	occurring.
* When	the	story	ends,	there	should	be	a	way	for	the	user	to	replay	the	entire	animation	from	the	
beginning.
* You	are	free	to	be	as	creative	as	you	like	with	your	choice	of	sprites	and	actions.

You	may	choose	from	the	sprites	provided	by	BYOB	or	create	your	own.	(You	will	not	be	graded	on
your	artistic	skills.)	You	may	interpret	the	nursery	rhyme	literally	or	be	clever	with	your	depiction	(but	
don't	go	too	far).	However,	all	sprites,	behaviors,	words,	and	animations	must	be	school-appropriate.

If	you	choose	a	particularly	long	nursery	rhyme,	you	may	not	need	to	animate	the	whole	thing.	Please	
check	with	your	teacher	if	you	think	your	rhyme	is	long	enough	for	this.

### Implementation Details
As	mentioned	above,	your	animation	must	display	the	nursery	rhyme	in	its	entirety	and	animate	each	line.
Action	must	be	performed	by	sprites	and	must	consist	of	more	than	simply	changing	costumes.	You	must	
include	the	following	components	in	your	animation:

* At	least	two	sprites	that	act	in	some	way	to	contribute	to	the	depiction	of	the	story
* At	least	one	sprite	that moves
* At	least	one	sprite	that	rotates
* At	least	one	sprite	that	changes	costume
* At	least	one	sprite	that	is	both	hidden	and	shown	at	some	point

Note	that	multiple	of	these	requirements	may	be	satisfied	by	the	same	sprite	(e.g.	the	same	sprite	can	both
move	and	change	costume),	but	you	must	have	at	least	two	separate	sprites	that	act	in	the	animation.
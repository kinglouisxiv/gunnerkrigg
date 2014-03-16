#Gunnerkrigg Online Searchable Site
Files for the online searchable Gunnerkrigg Court site: http://www.louisxiv.co.uk/gunnerkrigg/
Index.txt is parsed into HTML by a python script [cig.py](https://github.com/kinglouisxiv/cig)

##Getting Started
Please send snipergirl a PM on the <a href="http://gunnerkrigg.proboards.com/">forums</a> or reply to the <a href="http://gunnerkrigg.proboards.com/thread/1883/searchable-database-comics?page=1">forum post</a> if you want to get involved and we can get you started.

For more information see the <a href="https://github.com/snipergirl/gunnerkrigg/wiki">Wiki</a> for this project

###Tagging guide
- What to tag? Anything relevant that can be seen in the page that people might want to search for
- The top priority is to tag all the characters, settings and important props; other things can be added later if you're not sure.
- It's best to use tags that already exist (check alltags.txt) if possible. If you need to add a new tag, add it to alltags.txt at the same time with a description; keep tags short but meaningful: "GoodHope" rather than "GoodHopeHospital" -- as tags can be described.
- At the moment, just tag characters who are seen (in the main action, flashbacks, memories), rather than mentioned (this may change).
- Important props/items such as the blinker stone need to be tagged.
- Recurring characters should be tagged by name or a specific description if possible; generic characters should be referred to as "teacher" or "students" or "LaserCow".
- If you can tag things like alchemical symbols that would be very useful. If you are not sure what a symbol is, tag it as "symbol" and make a new post on the forum and ask -- there are a lot of knowledgeable people out there!
- The forum, tvtropes and the Gunnerkrigg Wiki (gunnerkrigg.wikia.com) are invaluable for information on who and what exists in the comic
- At the moment we are not tagging the cover pages however this might change (update: it has changed!)
- Treatises are obviously full of tag-material! Have a go and we'll all contribute further tags as necessary.

###How to use the tagging helper
_N.B. the tagging helper probably does not work with the newer ```key:value``` index_

- The tagging helper will work out of the box- just open "taghelper.htm".
- Ideally, install Python 2.x.x (current production version 2.7.5) (available at http://www.python.org/getit/); then whenever you want to update it with your latest index.txt, just run "taghelper.py".

###Starting with GitHub
- First you need one of us (probably snipergirl) to give you access to the repo. Please send snipergirl a PM on the <a href="http://gunnerkrigg.proboards.com/">forums</a> or reply to the <a href="http://gunnerkrigg.proboards.com/thread/1883/searchable-database-comics?page=1">forum post</a> if you want access.
- You can either edit the files directly on the website and commit changes that way or:
- You can download a program for win/mac/linux
- Install it and run it
- Sign in and click on your username below "github" on the far left of the program
- Click on the repository in the middle that you want (snipergirl/gunnerkrigg) and click 'clone'; that will give you a copy on your computer.
- Each time before editing, in the main part of the program can click "refresh" at the top middle, click on the repo and click "sync" up the top.
- Then edit the files yourself
- When you are ready to submit your changes, save the file
- Go into your github program, which will show that you have unsaved changes in whichever file(s)
- Put in a commit message about what you have done in the right hand area and click "commit"
- Then click "sync" and it should upload.
- This is also a tutorial about Git in general: try.github.io/levels/1/challenges/1

##Format

###Index of pages - Index.txt
- The comics are in reverse order, most recent at the top.
- Each comic has a bunch of entries, in ```key: value``` format, starting with a ```page:``` and the page number (look at the URL of the comic and find the number at the end)
- KEYS
	- page: 	comic page ID and link: heads a comic page entry.
	- url: 	the actual comic page url (to insert page ID  value replace in the url with {0} )
	- tag: 	tags for the page's story items of note: character, item, location, etc.
	- desc: 	text relevant to the page (description, line of dialogue, etc)
	- note:	footnotes, links, etc
	- auth:	relevant notes from 
- Each ```key: value``` pair is on a separate line
- the text in desc:, note: and auth: can have Markdown formatting and links.

E.g.:
```markdown
page:16
	url: http://www.gunnerkrigg.com/?p={0}
	; the page number is substituted for the {0}
	tag: ch-01
	; tags starting ch- are special case chapter identifiers & selectors
	tag: Bonus
	tag: Blackboard
	tag: Chester
	tag: Foley
	tag: Queslett
	tag: Tea
	tag: Thornhill
	desc: Bonus Page: Houses at Gunnerkrigg Court
	auth: **Tom**: Year 7 is the first year of [UK] secondary school, and is the equivalent of 6th grade in the US. Children in Year 7 are 11-12 years old.
page:15
	url: http://www.gunnerkrigg.com/?p=15
	tag: ch-01
	tag: Annie
	tag: Bridge
	tag: Gillitie
	tag: Teacher
	desc: Sorry sir. I got lost.
page: AitF-1
	;N.B. different style of page ID to avoid clash with original comic page 1
	tag: ch-31b
	tag: Annie
	tag: Bind
	tag: Coyote
	tag: Gillitie
	tag: Jones
	tag: Ysengrin
	desc: I can stay here?
	url: http://www.gunnerkrigg.com/extracomics/comic.php?c=Annie%20in%20the%20Forest%20Part%201&p=1
	;N.B. fully specified url as the page: id can't be substituted
```

###Tags & descriptions -- Alltags.txt
- The tags are in alphabetical order
- Each tag is on a separate line
- The tag and its description are separated by tab-spacing: [tag] tab [description]
- the description can have Markdown formatting and links to other tags or out to the wiki.
- tag names should be unique when folded to lowercase (for links)

E.g.:

```markdown
AnimalCells	the Court’s large animal holding cells
AnimalLab	a Court research lab _{[wiki](http://gunnerkrigg.wikia.com/wiki/Animal_Lab)}_
Anja	Anja Donlan, [Kat](#kat)’s mother; Roma origin but lived mostly in Spain _{[wiki](http://gunnerkrigg.wikia.com/wiki/Anja)}_
Ankou	Breton grim reaper; [psychopomp](#psychopomps)_{[wiki](http://gunnerkrigg.wikia.com/wiki/Psychopomps#Ankou)}_
Annan	Annan Waters, a wide river in a deep gorge which separates [Gunnerkrigg Court](#court) from [Gillitie Wood](#gillitie), the 'forest' _{[wiki](http://gunnerkrigg.wikia.com/wiki/Annan_Waters)}_
Annie	Antimony Carver, our protagonist ([fire](#fire) Head Girl) _{[wiki](http://gunnerkrigg.wikia.com/wiki/Antimony_Carver)}_
AnnieCut	The cut on [Annie](#annie)’s ethereal face from [Jeanne](#jeanne)’s [sword](#sword)
AnnieJumper	[Annie](#annie)’s original school jumper
```


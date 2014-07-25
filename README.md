#Gunnerkrigg Online Searchable Site
Files for the online searchable Gunnerkrigg Court page: http://www.louisxiv.co.uk/gunnerkrigg/

Two files, index.txt & alltags.txt, are parsed into HTML parts by a python script [cig.py](https://github.com/kinglouisxiv/cig)

###Tagging guide
- What to tag? Anything relevant that can be seen in the page that people might want to search for
- The top priority is to tag all the characters, settings and important props; other things can be added later if you're not sure.
- It's best to use tags that already exist (check alltags.txt) if possible. If you need to add a new tag, add it to alltags.txt at the same time with a description; keep tags short but meaningful: "GoodHope" rather than "GoodHopeHospital" -- as tags can be described.
- At the moment, just tag characters who are seen (in the main action, flashbacks, memories), rather than mentioned (this may change).
- Important props/items such as the blinker stone need to be tagged.
- Recurring characters should be tagged by name or a specific description if possible; generic characters should be referred to as "Teacher" or "Students" or "LaserCow".
- If you can tag things like alchemical symbols that would be very useful. If you are not sure what a symbol is, tag it as "symbol" and make a new post on the forum and ask -- there are a lot of knowledgeable people out there!
- The forum, tvtropes and the Gunnerkrigg Wiki (gunnerkrigg.wikia.com) are invaluable for information on who and what exists in the comic

##Format

###Index of pages - Index.txt
- The comics are in reverse order, most recent at the top.
- Each comic has a bunch of entries, in ```key: value``` format, starting with a ```page:``` and the page number (look at the URL of the comic and find the number at the end)
- KEYS
	- page: 	comic page ID and link: heads a comic page entry.
	- url: 	optional in the main comic, needed for side-comics
	- tag: 	tags for the page's story items of note: character, item, location, etc.
	- desc: 	text relevant to the page (description, line of dialogue, etc)
	- note:	footnotes, links, etc
	- auth:	relevant notes from 
- Each ```key: value``` pair is on a separate line
- the text in desc:, note: and auth: can have Markdown formatting and links.

(There is a more detailed and likely more up to date note of this in the file's header comment)

E.g.:
```
page:16
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
	tag: ch-01
	tag: Annie
	tag: Bridge
	tag: Gillitie
	tag: Teacher
	desc: Sorry sir. I got lost.
page: AitF-1
	;N.B. different style of page ID to avoid clash with original comic page 1
	url: http://www.gunnerkrigg.com/extracomics/comic.php?c=Annie%20in%20the%20Forest%20Part%201&p=1
	;N.B. fully specified url as it isn't the main comic's url
	tag: ch-31b
	tag: Annie
	tag: Bind
	tag: Coyote
	tag: Gillitie
	tag: Jones
	tag: Ysengrin
	desc: I can stay here?
```

###Tags & descriptions -- Alltags.txt
- The tags are in alphabetical order
- Each tag is on a separate line
- The tag and its description are separated by tab-spacing: [tag] tab [description]
- the description can have Markdown formatting and links to other tags or out to the wiki.
- tag names should be unique when folded to lowercase (for links)

(There is a more detailed and likely more up to date note of this in the file's header comment)

E.g.:

```
AnimalCells	the Court’s large animal holding cells
AnimalLab	a Court research lab _{[W](http://gunnerkrigg.wikia.com/wiki/Animal_Lab)}_
Anja	Anja Donlan, [Kat](#kat)’s mother; Roma origin but lived mostly in Spain _{[W](http://gunnerkrigg.wikia.com/wiki/Anja)}_
Ankou	Breton grim reaper; [psychopomp](#psychopomps)_{[W](http://gunnerkrigg.wikia.com/wiki/Psychopomps#Ankou)}_
Annan	Annan Waters, a wide river in a deep gorge which separates [Gunnerkrigg Court](#court) from [Gillitie Wood](#gillitie), the 'forest' _{[W](http://gunnerkrigg.wikia.com/wiki/Annan_Waters)}_
Annie	Antimony Carver, our protagonist ([fire](#fire) Head Girl) _{[W](http://gunnerkrigg.wikia.com/wiki/Antimony_Carver)}_
AnnieCut	The cut on [Annie](#annie)’s ethereal face from [Jeanne](#jeanne)’s [sword](#sword)
AnnieJumper	[Annie](#annie)’s original school jumper
```


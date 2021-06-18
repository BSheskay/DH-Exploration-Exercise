# Picking sources
Frankly a very hard process as it has to be something that I can work with. I spend about two days browsing the different archives between essay writing for other classes.
I always seem to find myself back at the (Diary Index)[https://diaryindex.com/digitized-diaries/]. I feel as though I can do better work with them -- As in I feel as though its easier to comprehend when its a single author.
I originally wanted to work with the (diary of a Japanese civilian in Kuala Lumpur)[http://cudl.lib.cam.ac.uk/view/MS-RCMS-00103-00012-00023/1], however, there was no transcription of it.
From the [Digital Archives of Latvian Folklore](http://garamantas.lv/en/collection/index?ManuscriptSearch%5Brepository_id%5D=1115628), I found a very interesting sounding one of (Folklore materials collected by school children)[http://garamantas.lv/en/collection/885704/Collection-of-Bauni-Milites-Primary-School]. Heartbreakingly, the transcription is in Latvian, and I searched around and was unable to find an English version.
From the (National Security Archive)[https://nsarchive.gwu.edu/briefing-book/russia-programs/2020-05-25/irreplaceable-chernyaev-diary-1980], there was a Diary from a prominent soviet advisor. Mercifully in English. Will probably use this one.

# Chernyaev
Now that I've decided on the source, there are a few ways I can go over this. Whatever I do, I'd like to use what I did for the static websites tutorial as a hub for the info. That way I can easily link to all my progress, as well as any other Twine game or podcast or whatever I make, and I can keep it all nicely sorted.
In terms of what I will do, I have some possible ideas about perhaps instances of 'negative' vs 'positive' words as the end of the Soviet Union draws closer? But there is of course the issue that this a translated Russian text, and many words require context to be considered positive or negative.

# Scraping with wget
The way that NS Archive is set up makes it really difficult to use wget or any scraping tools, as instead of everything being in directories as would be easy, its all seemingly sorted randomly with no sorting of URLs between different projects, and with hundreds of active projects occurring there, it would be easier to manually download the 13 entries.  
This has become painful. It turns our some of the entries are hosted on a different website ```https://nsarchive2.gwu.edu/```meaning all of my attempts to to automated / recursive scraping has been a waste. Furthermore, the NS Archive itself is so out of date their "Main page" on Chernyaev is missing key entries of his diary including the one that covers 1980, which they themselves call "Irreplaceable" ironically enough.

# API tutorial
Hopefully I can use the APIs tutorial to get some requests for 'Chernyaev' on the NS Archives website.
```
Traceback (most recent call last):
  File "ca.py", line 38, in <module>
    data = response.json()
  File "C:\Users\brend\anaconda3\lib\site-packages\requests\models.py", line 898, in json
    return complexjson.loads(self.text, **kwargs)
  File "C:\Users\brend\anaconda3\lib\json\__init__.py", line 357, in loads
    return _default_decoder.decode(s)
  File "C:\Users\brend\anaconda3\lib\json\decoder.py", line 337, in decode
    obj, end = self.raw_decode(s, idx=_w(s, 0).end())
  File "C:\Users\brend\anaconda3\lib\json\decoder.py", line 355, in raw_decode
    raise JSONDecodeError("Expecting value", s, err.value) from None
json.decoder.JSONDecodeError: Expecting value: line 1 column 1 (char 0)
```
This error code is spit out every time I try using it on the ```https://nsarchive.gwu.edu/search/node/``` website. I tried searching for possible issues to no avail. I checked old logs from the tutorial, and I could find nothing useful. I'll put this off to the side for now.

# Though I had something: I did not.
Apparently the NS Archives have a 'virtual reading room'. I was excited and spent more time than I am willing to admit redoing everything I did in the last two steps to attempt to actually have anything work. Nothing worked.

# Going Crazy
At this point, I have an idea. I know its not technically part of the assignment and it'll take time and progress away from other parts of the presentation, but simply for my own peace of mind, I have deiced to make a ```archives``` directory in my project. There, I will place all the unordered PDFs, create a master PDF, put csv files of everything with the hope that if anyone chooses to ever use these diary entries for any sort of work in the future they will not have to go through what I went through.

As it stands now, regular ways of accessing this information is impossible using the technics we learned. The only people who have access to these files are the NS Archives and they translate them in random order, only upload them in PDF fromat, they format the PDFs differently for whatever so I will fix that. For example, the PDF for 1976 entries is hosted on ```https://nsarchive2.gwu.edu/``` whereas 1977 is hosted on ```https://assets.documentcloud.org/``` . Clearly they changed their site at some point, but seeing as they do not archive or translate anything chronologically it goes back and forth across those two sites.

# Static Website
I used what I learned in the static website tutorial to make a site to hold my work for this assignment. I even made some quick art in photoshop to make it look a bit more aesthetically pleasing. I've spend over a week now chasing dead ends and trying to keep up with my other class and work, so my goal at this point is to *at least* have a website where I can complain about the NS Archives by the end of this.

# Sound and Sonification
I looked over and was rather interested in the Sound and Sonification tutorial during the third unit. I did not get around to doing it, however I am still interested in it, and I think a podcast would be an interesting addition to the page and the project.
I would like to have an embedded audio player if I can make that in time, however the 11th hour is approaching, so I may just have to do with my link.

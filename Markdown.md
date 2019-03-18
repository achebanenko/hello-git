Wes Bos - Mastering Markdown - My Playground  
http://masteringmarkdown.com

## 2. Paragraphs and Text Decoration

one
two
three

One

Two

Three

This is *italic* and this is **bold**. Alo this is _italic_ and this is __bold__.

This is **_bold italic_**. This is ~~strike~~ text.


## 3. Headings

# H1
## H2
### H3
Headings have automatic id set
#### H4
##### H5
###### H6
####### H7
Indeed H7 does not exist?

Another way just for h1 and h2

Heading 1
===
Heading 2
---
As many signs as you need (min 3)
-------------------


## 4. Links in Markdown

Wrap <http://link.com> inside <> to be a link, but it also works auto http://link.com

Link just with [text](//link.com) wrap in [] and just after put link in () 

You also can add title by adding quotes inside () here my [example.com](//example.com "Link to Example") of it

This course is brought you by [Wes][1] how is very cool teacher.  
Check [wes'][1] site - one more link with [][] here - it's recommended because then you would need to change link only in one place after end of the text

Or you use [text][word] as index, and then even only shortcut itself [word]

[1]: http://wesbos.com
[word]: //word.com


## 5. Markdown Images

Inserting image is similar to linking, just use ! before [] which stands for alt - maybe empty, and then () where you place source and "title" if needs.
![Alt for image](http://unsplash.it/300/200?random "Title for image")

[pup]: http://unsplash.it/300/200?image=1012

Or you can use reference same as in link, ex. pup image  
![Pup image][pup]
and put value of your ref before or after this peace of text.

You can use nested markdown to put link for larger image  
[![](http://unsplash.it/50/50?image=1000)](http://unsplash.it/500/500?image=1000)  

Or use html inside  
[<img src="http://unsplash.it/50/50?image=1000"/>](http://unsplash.it/500/500?image=1000)

In markdown you can use html tags and even style for css wherever you can't control  
<img src="dog.jpg" width="300" height="50" />  
<img class="cat-img" src="cat.jpg" />

<style>
  img {width: 400;}
</style>  
!?Not working for me

You write use figure and figcaption in html  
<figure>
  <img src="fox.jpg"/>  
  <figcaption>
    Fox image figcaption
  </figcaption>
</figure>

<style>
  figcaption {color: red}
</style>


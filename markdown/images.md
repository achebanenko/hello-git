Inserting image is similar to linking, just use `!` before `[]` which stands for alt (maybe empty), and then `()` where you place source and "title" if needs.
![Alt for image](http://picsum.photos/300/200 'Title for image')

[pup]: http://picsum.photos/id/237/300/200

Or you can use reference same as in link, ex. _pup_ image  
![Pup image][pup]
and put value of your ref before or after this peace of text.

You can use nested markdown to put link for larger image  
[![](http://picsum.photos/id/870/50/50)](http://picsum.photos/id/870/500/500)

Or use html inside  
[<img src="http://picsum.photos/id/0/50/50"/>](http://picsum.photos/id/0/500/500)

In markdown you can use html tags and even style for css wherever you can't control  
<img class="dog-img" src="dog.jpg" width="300" height="50" />  

<style>
  /* img, */
  .dog-img {
    height: 400;
  }
</style>

?Styling not working

You write use figure and figcaption in html

<figure>
  <p><img src="fox.jpg"/></p>
  <figcaption>
    Fox image figcaption
  </figcaption>
</figure>

<style>
  figcaption {color: red}
</style>

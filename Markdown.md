Wes Bos - Mastering Markdown  
http://masteringmarkdown.com

Look **Raw** mode

## 10. Github Treats

**Checkboxes**

Write list and after \* put [] with space inside, then put **x** for done todos

- [ ] Gert milk
- [x] Crack eggs
- [ ] Cook bacon

**Reference to pull request**

I had the same problem in #51 but fixed it with @person - should appear select-list to choose from pull requests and people after typing # and @

## 9. Tables

Use **pipe around** columns and also separate table head from table body with : and any of -

| Dog's name | Dog's age |
| :--------- | :-------- |
| Snickers   | 2         |
| Prudence   | 8         |

And also you can align text in columns with : on left, right or on both sides for centering

|   Name   | Age |
| :------: | --: |
| Snickers |   2 |
| Prudence |   8 |

## 8. Code Blocks

Here is my code - but! **indentation** doesn't work for me:  
 var x = 100;
const dog = 'snickers';

Using **code block** instead with before tree `and` after - but as you can see - you can use **one backquote to highlight code inline**:

```php
$age = 50;
$name = "wes";
echo strtoupper($name);
```

And if you write `name` of the language (js, php, exc.) it also makes a coloring of your code.

You can use `diff` to show difference between lines of code

```diff
var x = 100;
- var y = 200;
+ var y = 300;
```

## 7 Line Breaks, Horizontal Rules and BlockQuotes

**Line Breaks**

Wes is cool. Use **br** tag<br>
He really is. Or **two spaces** works for me.  
Really works.

**Horisontal rules**

Why = this doesnt work?

===

But leave empty lines between **three signs of = or -**

---

Also this \* three times works for horisontal rules

---

**Blockquotes**

> You miss 100% of the shots you don't take. - Wayne Gretzky
>
> Next line hhere
>
> - One more line maybe separated **Author**

## 6. Lists — Ordered, Unorderd, Bullets and Nesting

Use whatever or \* or - or + for list, then combine few for nested lists

- milk
- eggs
- bread

Ordered list - use 1. before every line

1. Combine ingredients
1. Gently stir together
1. Bake at 350 for 20 minutes

For nesting use tab or two spaces to indenting

1. Step 1

- Substep
  - Sub-substep

1. Step 2 main
1. Sub-ordered
   1. sub-subordered
   1. sub-subordered2
1. Sub-ordered line 2
1. Step 3 main

#### Complex

1. Complex sub

- Here

  This is inline  
  ![](http://unsplash.it/150/100?random)

  ```js
  var x = 100
  ```

1. Second step

## 5. Markdown Images

Inserting image is similar to linking, just use ! before [] which stands for alt - maybe empty, and then () where you place source and "title" if needs.
![Alt for image](http://unsplash.it/300/200?random 'Title for image')

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
  img {
    width: 400;
  }
</style>

!?Not working for me

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

## 4. Links in Markdown

Wrap <http://link.com> inside <> to be a link, but it also works auto http://link.com

Link just with [text](//link.com) wrap in [] and just after put link in ()

You also can add title by adding quotes inside () here my [example.com](//example.com 'Link to Example') of it

This course is brought you by [Wes][1] how is very cool teacher.  
Check [wes'][1] site - one more link with [][] here - it's recommended because then you would need to change link only in one place after end of the text

Or you use [text][word] as index, and then even only shortcut itself [word]

[1]: http://wesbos.com
[word]: //word.com

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

# Heading 1

## Heading 2

## As many signs as you need (min 3)

## 2. Paragraphs and Text Decoration

one
two
three

One

Two

Three

This is _italic_ and this is **bold**. Alo this is _italic_ and this is **bold**.

This is **_bold italic_**. This is ~~strike~~ text.

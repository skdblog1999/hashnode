## Complete Markdown Tutorial From Beginners To Advance

Hello everyone I am *Shashikant* and in this article I'm gonna give you a complete tutorial on **Markdown**.

## What is Markdown ?

Markdown is a simple and lightweight markup language that can be use to make formatting in a normal text files.

**In simple terms**

Its is just a simple and small language that is used format text files same as we do in HTML.

## How much time does it take to become expert ?

It will hardly take 1 to 2 hours to become expert in **Markdown**.

## Where it is used ?

**Markdown** is used in many places like:

1. Slack supports markdown
2. Github and Github wiki
3. Project management products like Target Process or Trello
4. Confluence and Mediawiki have plug-ins to support markdown
5. Blog-aware static site generators like Jekyll or Hugo
6. Technical documentation in markdown is available, for example, on Github or on XebiaLabs.

## Running Markdown

Every markdown file has extension `.md` or `.markdown`. So to open and preview it        you must have an markdown editor or editor with markdown support.

Here you can download [typora](https://typora.io/) one of the best markdown editor that i use        personally.

## Let's Start

### Heading

+ Heading in markdown can be generated using `#` tag.

+ Number of `#` tags represents the heading level.

+ In total there are 6 heading levels.

+ And you can also use HTML `h` tag to generate heading in markdown.

  Example
```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

  Result
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

As I stated earlier you can also use HTML `h` tags here to generate heading.

## Paragraphs

Simply write on a new line. It will get converted into a paragraph.

Example:
```markdown
Hey there I am Shashikant Dwivedi from Shashikant Blog
```

Result

Hey there I am Shashikant Dwivedi from Shashikant Blog

Again here you can also use `p` tag as you did in HTML.

## Line Breaks

To create a line break you can simple write to the next line or use `<br>` tag as you do in HTML.

Example

```markdown
Hey there I am Shashikant from Shashikant Blog.<br>And today i am sharing my learning on markdown.<br>And believe me its awesome.
```

Result

Hey there I am Shashikant from Shashikant Blog.

And today i am sharing my learning on markdown.

And believe me its awesome.

## Text Styling

1. #### Bold

   + To bold any content just do like this `**text**` or `__text__`
   + Both will get converted into **text**
   + You can also use `<b></b>` tag to do the same.

2. #### Italic

   + To style italic any content just do like this `*text*` or                            `_text_`
   + Both will get converted into *text*.
   + You can also user `<em>` tag to do the same.

3. #### Bold and Italic Both

   + To make any content bold and italic both just do like this  `***text***` or `___text___`.                        
   + Both will get converted into ***text***.

## Block Quotes

To create a block quote just add `>` in the starting of line.

Example

```markdown
> this is a block quoute
```

Result

> this is a block quote

You can also use HTML `<blockquote>` tag to do the same.

To create a nested block quote add  `>` , number of time you want the                        level of quote to be nested.

Example

```markdown
> this is a blockquote.
>> this is a nested blockquote.
>>> this is also a nested blockquote.
```

Result

> this is a blockquote.
>
> > this is a nested blockquote.
> >
> > > this is also a nested blockquote.

You can also use some of the other markdown elements inside a block quote.

## Lists

1. #### Ordered List

   + To create an ordered list simply write any number then dot and press space and then enter next item in list.

   + You can also use `<ol>` tag to do the same.

     Example

     ```markdown
     1. One
     1. Two
     1. Three
     ```

     OR

     ```markdown
     1. One
     2. Two
     3. Three
     ```

     Result

     1. One
     2. Two
     3. Three

2. #### Unordered List

   + To create an unordered list simple use any one of these symbols `*` or                                `+` or `-` and press space.

   + You can also use `<ul>` tag to do the same.

     Example

     ```markdown
     - one
     - two
     - three
     ```

     OR

     ```markdown
     + one
     + two
     + three
     ```

     OR

     ```markdown
     * one
     * two
     * three
     ```

     Result

     * one
     * two
     * three

3. #### Nested List

   + To created a nested list you simply press tab when you want your list to be nested.

     Example

     ```markdown
     1. one
     2. two
     	1. one
     	2. two
     		1. one
     		2. two
     ```

       Result

     1. one
     2. two
       3. one
       4. two
           1. one
           2. two

     You can also combine ordered and unordered list while nesting.

## Code

To add single line code just put code between tick (`) marks.

You can also use `<code>` tag to do the same.

Example

```
python first program - `print('Hello World')`
```

Result

python first program - `print('Hello World')`

To add multiple line code with syntax highlighting put code between three tick marks(```) and you can also specify the language.

## Horizontal Lines

To create an horizontal line you can use this `***` or `---` or                        `___`.

You can also use `<hr>` tag to do the same.

Example

```markdown
One
---
Two
***
Three
___
Four
```

Result

One

---

Two

***

Three

___

Four



## Links

+ To define a link you can simply write the link like `https://shashikant.xyz` it                        will result in https://shashikant.xyz .

+ To give and alternate name to a link put `[name here](and link here)`

  Example

  ```markdown
  Welcome to my blog [shashikant blog](https://shashikant.xyz)
  ```

  Result

  Welcome to my blog [shashikant blog](https://shashikant.xyz)

  

+ To give link a tile you can do like this `[name](link "title")`

  Example

  ```markdown
  Check this link title [shashikant blog](https://shashikant.xyz " In this blog, I write what I learn")
  ```

  Result

  Check this link title [shashikant blog](https://shashikant.xyz" In this blog, I write what I learn")

+ You can also use `<a>` tag to do the same.



## Images

+ To add image to the markdown use the syntax same as link just put an `!` mark before the link title bracket like `![image name](image link "title")`

+ You can also use `<img>` tag to do the same.

  Example

  ```markdown
  ![python](https://www.python.org/static/opengraph-icon-200x200.png)
  ```

  Result

  

![python](https://www.python.org/static/opengraph-icon-200x200.png)

## Escape Characters

+ To escape character or if we say to use literal that have an special meaning in markdown you can use `\`.

  Example

  ```markdown
  \*\*bold\*\*
  ```

  Result:

  \*\*bold\*\*



## Note

There are many flavors of markdown that support additional features. And these are the basic features that every markdown flavor supports.



So this is all that you have to know about Markdown.

If you have any problem you can ask me in the comment section.
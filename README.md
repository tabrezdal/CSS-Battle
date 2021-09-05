# CSS-Battle

🏆To Score Higher in CSSBattle, You need to follow this hacks.🏆


👉 Avoid Uing White Spaces

The most basic strategy for code-golfing — remove unnecessary spaces, tabs, newlines, etc.
These characters are not necessary for the code to work functionally. This is one of the things that minifiers do to your code too.

    ✔ Practice this 
    <style>div{color:red;}</style>
    
    ❌Instead of This
    <style>
      div {
        color: red;
      }
    </style>






👉 Omit the last semi-colon

You can ommit the only last semi-colon, don't ommit in beteen the declaration

    ✔ Practice this 
    <style>
      div {
        background: red;
        height: 200px
      }
    </style>

    ❌Instead of this
    <style>
      div {
        background: red;
        height: 200px;
      }
    </style>





👉 Omit the closing tags

In most cases, you can omit the closing tag of an element.
This works because the Browser closes them for you, to make the HTML valid.
Though, be cautious as in some cases seemingly unclosed sibling tags can become parent-child of each other.

    ✔ Practice this 
    <div>
    <style>
      div {
        color: red;
      }

    ❌Instead of this

    <div></div>
    <style>
      div {
        color: red;
      }
    </style>
  
  
  


👉 Remove Double Quotes
  
You can remove the quotes from HTML attributes and replace the white-spaces before numbers with a +/-. 
Though, some re-ordering might be required to make things work. This is a very good example of exploiting how parsers understand your code. 
In the following example, we reorder things such that + marks the beginning of border-width and # marks the start of border-color.
  
    ✔ Practice this 
    <div style=border:solid+10px#00f></div>

    ❌Instead of This
    <div style="border:1px solid blue"></div>
  
  
  
  
  
👉 <body> has some ancient super-attributes!
There are old deprecated attributes available on body tag to give background and text color. These can prove deadly in battles!

    ✔ Practice this
    <body bgcolor=red text=green>

    ❌Instead of This
    <style>
    body {
      background: red;
      color:green;
    }
    </style>

  
  
  
  
👉 Shorten selectors with made-up attributes
  
You can assign made-up attribute to any element to target it specifically in your selectors.
Here is an example where you want to select the 3rd <P> tag.
  
    ✔ Practice this
   <p><p><p i><p><p>
    <style>
      p[i]{
        background: red;
      }
    </style>

   ❌Instead of this
   <p><p><p><p><p>
    <style>
      p:nth-child(3){
        background: red;
      }
    </style>
  
  
  
  
  
👉 position:fixed beats position:absolute, mostly
  
In most cases, you might want to absolutely position an element with respect to the window/viewport instead of another element.
In such position: fixed can save you a good 3 characters! Neat, right?!
  
    ✔ Practice this 
    <style>
      div{
        position: fixed;
      }
    </style>

    ❌Instead of this
    <style>
      div{
        position: absolute;
      }
    </style>





👉 Play with the units
Experimenting with different units can save you a character or two, and give you that extra edge.
For eg. 100px is better written as 25vw for CSSBattle's 400px target width.
You can use px also, but while you use px you can actually ommit suffix px and you will get same result.

    ✔ Practice this 
    <style>
      div{
        width: 25vw / 100;
      }
    </style>
    
    ❌Instead of this
    <style>
      div{
        width: 100px;
      }
    </style>





👉 You don't always need to add an HTML element to style!
By default, you have the html and body elements to style in your code! It will work in some cases.

    ✔ Practice this 
    <style>
      body{
        background: red;
      }
    </style>

    ❌Instead of this
    <div>
    <style>
      div{
        background: red;
      }
    </style>

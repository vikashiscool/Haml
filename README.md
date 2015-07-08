# Haml

###According to haml.info: 
**Haml** (HTML abstraction markup language) is based on one primary principle: markup should be beautiful. It’s not just beauty for beauty’s sake either; Haml accelerates and simplifies template creation down to veritable haiku.

###According to Wikipedia:
**Haml** (HTML Abstraction Markup Language) is a lightweight markup language that is used to describe the XHTML of any web document without the use of traditional inline coding. It is designed to address many of the flaws in traditional templating engines, as well as making markup as elegant as it can be. Haml functions as a replacement for inline page templating systems such as PHP, RHTML, and ASP. However, Haml avoids the need for explicitly coding XHTML into the template, because it is itself a description of the XHTML, with some code to generate dynamic content.

**Haml's equivalent for CSS is Sass.**


###Core Principles:
* Markup should be beautiful
* Markup should be DRY
* Markup should be well-indented
* HTML structure should be clear

###Other fun facts:
* Developed by Hampton Catlin (also the creator of Sass)
* Second most popular templating language for RoR
* Can also be used in Node.js, PHP, and .NET 

##ERB
```
<section class=”container”>
  <h1><%= post.title %></h1>
  <h2><%= post.subtitle %></h2>
  <div class=”content”>
    <%= post.content %>
  </div>
</section>
```

##HAML
```
%section.container
  %h1= post.title
  %h2= post.subtitle
  .content
    = post.content
```


* Haml uses whitespace and indenting to format the HTML.
* Tags are prefixed with a %. Closing tags aren’t required.

##HTML
```
<html> 
  <head> 
    <title>Our Awesome Haml Template</title> 
  </head> 
  <body> 
    Abstracting HTML since 2006 </body> </html> 

```

##HAML
```
%html 
  %head 
    %title Our Awesome Haml Template 
  %body 
    Abstracting HTML since 2006
```

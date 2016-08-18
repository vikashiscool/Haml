# Haml

##According to haml.info: 
"**Haml** (HTML abstraction markup language) is based on one primary principle: markup should be beautiful. It’s not just beauty for beauty’s sake either; Haml accelerates and simplifies template creation down to veritable haiku."

##According to Wikipedia:
"**Haml** (HTML Abstraction Markup Language) is a lightweight markup language that is used to describe the XHTML of any web document without the use of traditional inline coding. It is designed to address many of the flaws in traditional templating engines, as well as making markup as elegant as it can be. Haml functions as a replacement for inline page templating systems such as PHP, RHTML, and ASP. However, Haml avoids the need for explicitly coding XHTML into the template, because it is itself a description of the XHTML, with some code to generate dynamic content."

##Core Principles:
* Markup should be *beautiful*
* Markup should be *DRY*
* Markup should be *well-indented*
* HTML structure should be *clear*

##Other fun facts:
* Developed by Hampton Catlin (also the creator of Sass)
* Second most popular templating language for RoR
* Can also be used in Node.js, PHP, and .NET 


##HTML --> HAML

###HTML
```
<html> 
  <head> 
    <title>Our Awesome Haml Template</title> 
  </head> 
  <body> 
    Abstracting HTML since 2006 </body> </html> 
```

* Haml uses whitespace and indenting to format the HTML. A tag's children are indented beneath the parent tag.
* Tags are prefixed with a %. Closing tags aren’t required.


###HAML
```
%html 
  %head 
    %title Our Awesome Haml Template 
  %body 
    Abstracting HTML since 2006
```


##ERB --> HAML
###ERB
```
<section class=”container”>
  <h1><%= post.title %></h1>
  <h2><%= post.subtitle %></h2>
  <div class=”content”>
    <%= post.content %>
  </div>
</section>
```

###HAML
```
%section.container
  %h1= post.title
  %h2= post.subtitle
  .content
    = post.content
```

##Classes (.classname)
```
%body
  .address
    .name
    .street
    .country
      .zip
```

##IDs (#idname)
```
%body
  #container 
    %header
      %h1 This is where I live
    #main Rocking SF since 2014
    %footer Copyright 2015
```

##Specifying attributes
* You can use curly braces and specify your attributes with a Ruby hash. Holy crap!
```
%img{ :src => "/path/to/image", :alt => "Image description" }
```

* OR you can use parentheses and use a more HTML approach (e.g. foo="bar")!
```
%img{ src="/path/to/image", alt="Image description" }
```

Both yield the following HTML:
```
<img src="/path/to/image" alt="Image description">
```

Other attribute examples
```
%link {rel="stylesheet" href="/css/master.css"}
```

##Installing Haml with Rails
```
gem 'haml'
```

* If you need to replace Rails's Erb-based generators with haml, add `haml-rails` to your Gemfile as well.

To insert Ruby code, just add the `'='` sign followed by the code:
```
%p = Person.name
```
##More resources
* [http://haml.info/](http://haml.info/)
* [https://github.com/haml/haml](https://github.com/haml/haml)
* [http://www.cheatography.com/specialbrand/cheat-sheets/haml/pdf/](http://www.cheatography.com/specialbrand/cheat-sheets/haml/pdf/)
* [http://learn.shayhowe.com/advanced-html-css/preprocessors/](http://learn.shayhowe.com/advanced-html-css/preprocessors/)
* [http://www.sitepoint.com/an-introduction-to-haml/](http://www.sitepoint.com/an-introduction-to-haml/)

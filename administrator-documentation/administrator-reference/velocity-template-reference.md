---
cover: ../../.gitbook/assets/Untitled-1-01.png
coverY: 0
---

# Velocity Template Reference

You are here: [Section Two: Administrator reference](https://www.nexportcampus.com/Content/Guides/aweb/Content/Module\_Topics/Administration\_reference.htm) > Velocity Template Reference > Velocity User Guide

## **About this Guide** <a href="#about-this-guide" id="about-this-guide"></a>

> Many areas of NexPort Campus support the use of system or context properties that allow you to include text that dynamically changes for each user. For instance you can create group pages that display a logged in user's name or the current date. In assignment descriptions you can include information about the assignment including the current score, status, due date or many other properties. This is all possible because these text areas are actually templates written using the Velocity Templating Language (VTL).
>
> &#x20;
>
> The Velocity User Guide is intended to help page designers and content providers get acquainted with Velocity and the syntax of its simple yet powerful scripting language, the Velocity Template Language (VTL). Many of the examples in this guide deal with using Velocity to embed dynamic content in NexPort Campus, but all VTL examples are equally applicable to other pages and templates.

&#x20;

&#x20;

## **What is Velocity?** <a href="#what-is-velocity" id="what-is-velocity"></a>

> Velocity is a template engine. It permits editors and content designers to reference proterties defined by NexPort. This allows curriculum designers to create robust content that dynamically changes.

&#x20;

## **Velocity Template Language (VTL): An Introduction** <a href="#velocity-template-language-vtl-an-introduction" id="velocity-template-language-vtl-an-introduction"></a>

> The Velocity Template Language (VTL) is meant to provide the easiest, simplest, and cleanest way to incorporate dynamic content in a web page. Even a web page developer with little or no programming experience should soon be capable of using VTL to incorporate dynamic content in a in their campus and curriculum.
>
> VTL uses _references_ to embed dynamic content in the text displayed in various areas of NexPort Campus, and a variable is one type of reference. Variables are one type of reference that can refer to something defined in NexPort Campus, or it can get its value from a VTL _statement_ in the web page itself. Here is an example of a VTL statement that could be embedded in an HTML document:
>
> ```
> #set( $a = "Velocity" )
> ```
>
> This VTL statement, like all VTL statements, begins with the _#_ character and contains a directive: _set_. When an online visitor requests your web page, the Velocity Templating Engine will search through your web page to find all _#_ characters, then determine which mark the beginning of VTL statements, and which of the _#_ characters that have nothing to do with VTL.
>
> The _#_ character is followed by a directive, _set_. The _set_ directive uses an expression (enclosed in brackets) -- an equation that assigns a _value_ to a _variable_. The variable is listed on the left hand side and its value on the right hand side; the two are separated by an _=_ character.
>
> In the example above, the variable is _$a_ and the value is _Velocity_. This variable, like all references, begins with the _$_ character. Values are always enclosed in quotes; with Velocity there is no confusion about data types, as only strings (text-based information) may be passed to variables.
>
> The following rule of thumb may be useful to better understand how Velocity works: **References begin with **_**$**_** and are used to get something. Directives begin with **_**#**_** and are used to do something.**
>
> In the example above, _#set_ is used to assign a value to a variable. The variable, _$a_, can then be used in the template to output "Velocity".

&#x20;

&#x20;

## **Hello Velocity World!** <a href="#hello-velocity-world" id="hello-velocity-world"></a>

> Once a value has been assigned to a variable, you can reference the variable anywhere in your HTML document. In the following example, a value is assigned to _$foo_ and later referenced.
>
> ```
> <p>#set( $foo = "Velocity" )
> Hello $foo World!</p>
> ```
>
> The result is a paragraph (\<p>)that prints "Hello Velocity World!".
>
> To make statements containing VTL directives more readable, we encourage you to start each VTL statement on a new line, although you are not required to do so. The _set_ directive will be revisited in greater detail later on.

&#x20;

&#x20;

## **Comments** <a href="#comments" id="comments"></a>

> Comments allows descriptive text to be included that is not placed into the output of the template engine. Comments are a useful way of reminding yourself and explaining to others what your VTL statements are doing, or any other purpose you find useful. Below is an example of a comment in VTL.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> ## This is a single line comment.
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> A single line comment begins with _##_ and finishes at the end of the line. If you're going to write a few lines of commentary, there's no need to have numerous single line comments. Multi-line comments, which begin with _#\*_ and end with _\*#_, are available to handle this scenario.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> This is text that is outside the multi-line comment.
> Online visitors can see it.
> #* Thus begins a multi-line comment. 
> Online visitors won't see this text because 
> the Velocity Templating Engine will ignore it.*#
> Here is text outside the multi-line comment; it is visible.
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Here are a few examples to clarify how single line and multi-line comments work:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> This text is visible. 
> ## This text is not.
> This text is visible.
> This text is visible. 
> #* This text, as part of a multi-line comment,is not visible. 
> This text is not visible; it is also part of themulti-line comment. 
> This text still not visible. *# This text is outside the comment, so it is visible.## This text is not visible.
> ```

## **References** <a href="#references" id="references"></a>

> There are three types of references in the VTL: variables, properties and methods. As a designer using the VTL, you and your engineers must come to an agreement on the specific names of references so you can use them correctly in your templates.
>
> Everything coming to and from a reference is treated as a String object. If there is an object that represents _$foo_ (such as an Integer object), then Velocity will call its `.toString()` method to resolve the object into a String.
>
> **Variables**\
> The shorthand notation of a variable consists of a leading "$" character followed by a VTL _Identifier_. A VTL Identifier must start with an alphabetic character (a .. z or A .. Z). The rest of the characters are limited to the following types of characters:
>
> &#x20;
>
> * alphabetic (a .. z, A .. Z)
> * numeric (0 .. 9)
> * hyphen ("-")
> * underscore ("\_")
>
> &#x20;
>
> Here are some examples of valid variable references in the VTL:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> $foo$mudSlinger$mud-slinger$mud_slinger$mudSlinger1
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> When VTL references a variable, such as _$foo_, the variable can get its value from either a _set_ directive in the template. For example, if the Java variable _$foo_ has the value _bar_ at the time the template is requested, _bar_ replaces all instances of _$foo_ on the web page. Alternatively, if I include the statement
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $foo = "bar" )
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> The output will be the same for all instances of _$foo_ that follow this directive.
>
> **Properties**\
> The second flavor of VTL references are properties, and properties have a distinctive format. The shorthand notation consists of a leading _$_ character followed a VTL Identifier, followed by a dot character (".") and another VTL Identifier. These are examples of valid property references in the VTL:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> $customer.Address
> ```
>
> ```
> $purchase.Total
> ```
>
> &#x20;
>
> Take the first example, _$customer.Address_. It can have two meanings. It can mean, Look in the hashtable identified as _customer_ and return the value associated with the key _Address_. But _$customer.Address_ can also be referring to a method (references that refer to methods will be discussed in the next section); _$customer.Address_ could be an abbreviated way of writing _$customer.getAddress()_. When your page is requested, Velocity will determine which of these two possibilities makes sense, and then return the appropriate value.
>
> **Methods**\
> A method is defined in NexPort Campus and is capable of doing something useful, like running a calculation or arriving at a decision. Methods are references that consist of a leading "$" character followed a VTL Identifier, followed by a VTL _Method Body_. A VTL Method Body consists of a VTL Identifier followed by an left parenthesis character ("("), followed by an optional parameter list, followed by right parenthesis character (")"). These are examples of valid method references in the VTL:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> $customer.getAddress()$purchase.getTotal()$page.setTitle( "My Home Page" )$person.setAttributes( ["Strange", "Weird", "Excited"] )
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> The first two examples -- _$customer.getAddress()_ and _$purchase.getTotal()_ -- may look similar to those used in the Properties section above, _$customer.Address_ and _$purchase.Total_. If you guessed that these examples must be related some in some fashion, you are correct!
>
> VTL Properties can be used as a shorthand notation for VTL Methods. The Property _$customer.Address_ has the exact same effect as using the Method _$customer.getAddress()_. It is generally preferable to use a Property when available. The main difference between Properties and Methods is that you can specify a parameter list to a Method.
>
> The shorthand notation can be used for the following Methods
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> $sun.getPlanets()$annelid.getDirt()$album.getPhoto()
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> We might expect these methods to return the names of planets belonging to the sun, feed our earthworm, or get a photograph from an album. Only the long notation works for the following Methods.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> $sun.getPlanet( ["Earth", "Mars", "Neptune"] )## Can't pass a parameter list with $sun.Planets$sisyphus.pushRock()## Velocity assumes I mean $sisyphus.getRock()$book.setTitle( "Homage to Catalonia" )## Can't pass a parameter list
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> **Formal Reference Notation**\
> Shorthand notation for references was used for the examples listed above, but there is also a formal notation for references, which is demonstrated below:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> ${mudSlinger}${customer.Address}${purchase.getTotal()}
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> In almost all cases you will use the shorthand notation for references, but in some cases the formal notation is required for correct processing.
>
> Suppose you were constructing a sentence on the fly where _$vice_ was to be used as the base word in the noun of a sentence. The goal is to allow someone to choose the base word and produce one of the two following results: "Jack is a pyromaniac." or "Jack is a kleptomaniac.". Using the shorthand notation would be inadequate for this task. Consider the following example:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> Jack is a $vicemaniac.
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> There is ambiguity here, and Velocity assumes that _$vicemaniac_, not _$vice_, is the Identifier that you mean to use. Finding no value for _$vicemaniac_, it will return _$vicemaniac_. Using formal notation can resolve this problem.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> Jack is a ${vice}maniac.
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Now Velocity knows that _$vice_, not _$vicemaniac_, is the reference. Formal notation is often useful when references are directly adjacent to text in a template.
>
> **Quiet Reference Notation**\
> When Velocity encounters an undefined reference, its normal behavior is to output the image of the reference. For example, suppose the following reference appears as part of a VTL template.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> <input type="text" name="email" value="$email"/>
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> When the form initially loads, the variable reference _$email_ has no value, but you prefer a blank text field to one with a value of "$email". Using the quiet reference notation circumvents Velocity's normal behavior; instead of using _$email_ in the VTL you would use _$!email_. So the above example would look like the following:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> <input type="text" name="email" value="$!email"/>
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Now when the form is initially loaded and _$email_ still has no value, an empty string will be output instead of "$email".
>
> Formal and quiet reference notation can be used together, as demonstrated below.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> <input type="text" name="email" value="$!{email}"/>
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)

&#x20;

&#x20;

## **Getting literal** <a href="#getting-literal" id="getting-literal"></a>

> VTL uses special characters, such as _$_ and _#_, to do its work, so some added care should be taken where using these characters in your templates. This section deals with escaping the _$_ character.
>
> **Currency**\
> There is no problem writing "I bought a 4 lb. sack of potatoes at the farmer's market for only $2.50!" As mentioned, a VTL identifier always begins with an upper- or lowercase letter, so $2.50 would not be mistaken for a reference.
>
> **Escaping Valid VTL References**\
> Cases may arise where there is the potential for Velocity to get confused. _Escaping_ special characters is the best way to handle VTL's special characters in your templates, and this can be done using the backslash ( _\\_ ) character.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $email = "foo" )$email
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> If Velocity encounters a reference in your VTL template to _$email_, it will search the Context for a corresponding value. Here the output will be _foo_, because _$email_ is defined. If _$email_ is not defined, the output will be _$email_.
>
> Suppose that _$email_ is defined (for example, if it has the value _foo_), and that you want to output _$email_. There are a few ways of doing this, but the simplest is to use the escape character.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> ## The following line defines $email in this template:#set( $email = "foo" )$email\$email\\$email\\\$email
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> renders as
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> foo$email\foo\$email
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Note that the _\\_ character bind to the _$_ from the left. The bind-from-left rule causes _\\\\\\$email_ to render as _\\\\$email_. Compare these examples to those in which _$email_ is not defined.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> $email\$email\\$email\\\$email
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> renders as
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> $email\$email\\$email\\\$email
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Notice Velocity handles references that are defined differently from those that have not been defined. Here is a set directive that gives _$foo_ the value _gibbous_.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $foo = "gibbous" )$moon = $foo
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> The output will be: _$moon = gibbous_ -- where _$moon_ is output as a literal because it is undefined and _gibbous_ is output in place of _$foo_.
>
> It is also possible to escape VTL directives; this is described in more detail in the Directives section.

&#x20;

&#x20;

## **Case Substitution** <a href="#case-substitution" id="case-substitution"></a>

> Now that you are familiar with references, you can begin to apply them effectively in your templates. Velocity references take advantage of some Java principles that template designers will find easy to use. For example:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> $foo$foo.getBar()## is the same as$foo.Bar$data.getUser("jon")## is the same as$data.User("jon")$data.getRequest().getServerName()## is the same as$data.Request.ServerName## is the same as${data.Request.ServerName}
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> These examples illustrate alternative uses for the same references. Velocity takes advantage of Java's introspection and bean features to resolve the reference names to both objects in the Context as well as the objects methods. It is possible to embed and evaluate references almost anywhere in your template.
>
> Velocity, which is modelled on the Bean specifications defined by Sun Microsystems, is case sensitive; however, its developers have strove to catch and correct user errors wherever possible. When the method _getFoo()_ is referred to in a template by `$bar.foo`, Velocity will first try `$getfoo`. If this fails, it will then try `$getFoo`. Similarly, when a template refers to `$bar.Foo`, Velocity will try _$getFoo()_ first and then try _getfoo()_.
>
> Note: _References to instance variables in a template are not resolved._ Only references to the attribute equivalents of JavaBean getter/setter methods are resolved (i.e. `$foo.Name` does resolve to the class Foo's `getName()` instance method, but not to a public `Name` instance variable of Foo).

&#x20;

&#x20;

## **Directives** <a href="#directives" id="directives"></a>

> References allow template designers to generate dynamic content for their campus, while _directives_ -- easy to use script elements that can be used to creatively manipulate the output of the template-- permit web designers to truly take charge of the appearance and content of your campus.
>
> **#set**
>
> The _#set_ directive is used for setting the value of a reference. A value can be assigned to either a variable reference or a property reference, and this occurs in brackets, as demonstrated:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $primate = "monkey" )#set( $customer.Behavior = $primate )
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> The left hand side (LHS) of the assignment must be a variable reference or a property reference. The right hand side (RHS) can be one of the following types:
>
> &#x20;
>
> * Variable reference
> * String literal
> * Property reference
> * Method reference
> * Number literal
> * ArrayList
>
> &#x20;
>
> These examples demonstrate each of the aforementioned types:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $monkey = $bill ) ## variable reference#set( $monkey.Friend = "monica" ) ## string literal#set( $monkey.Blame = $whitehouse.Leak ) ## property reference#set( $monkey.Plan = $spindoctor.weave($web) ) ## method reference#set( $monkey.Number = 123 ) ##number literal#set( $monkey.Say = ["Not", $my, "fault"] ) ## ArrayList
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> NOTE: In the last example the elements defined with the \[..] operator are accessible using the methods defined in the ArrayList class. So, for example, you could access the first element above using $monkey.Say.get(0).
>
> The RHS can also be a simple arithmetic expression:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $value = $foo + 1 )#set( $value = $bar - 1 )#set( $value = $foo * $bar )#set( $value = $foo / $bar )
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> If the RHS is a property or method reference that evaluates to _null_, it will **not** be assigned to the LHS. It is not possible to remove an existing reference from the context via this mechanism. This can be confusing for newcomers to Velocity. For example:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $result = $query.criteria("name") )The result of the first query is $result#set( $result = $query.criteria("address") )The result of the second query is $result
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> If _$query.criteria("name")_ returns the string "bill", and _$query.criteria("address")_ returns _null_, the above VTL will render as the following:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> The result of the first query is billThe result of the second query is bill
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> This tends to confuse newcomers who construct _#foreach_ loops that attempt to _#set_ a reference via a property or method reference, then immediately test that reference with an _#if_ directive. For example:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $criteria = ["name", "address"] )#foreach( $criterion in $criteria )    #set( $result = $query.criteria($criterion) )    #if( $result )        Query was successful    #end#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> In the above example, it would not be wise to rely on the evaluation of _$result_ to determine if a query was successful. After _$result_ has been _#set_ (added to the context), it cannot be set back to _null_ (removed from the context). The details of the _#if_ and _#foreach_ directives are covered later in this document.
>
> One solution to this would be to pre-set _$result_ to _false_. Then if the _$query.criteria()_ call fails, you can check.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $criteria = ["name", "address"] )#foreach( $criterion in $criteria )    #set( $result = false )    #set( $result = $query.criteria($criterion) )    #if( $result )        Query was successful    #end#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Unlike some of the other Velocity directives, the _#set_ directive does not have an _#end_ statement.
>
> **String Literals**
>
> When using the _#set_ directive, string literals that are enclosed in double quote characters will be parsed and rendered, as shown:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $directoryRoot = "www" )#set( $templateName = "index.vm" )#set( $template = "$directoryRoot/$templateName" )$template
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> The output will be
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> www/index.vm
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> However, when the string literal is enclosed in single quote characters, it will not be parsed:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $foo = "bar" )$foo#set( $blargh = '$foo' )$blargh
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
>   bar  $foo
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> By default, this feature of using single quotes to render unparsed text is available in Velocity. This default can be changed by editing `velocity.properties` such that `stringliterals.interpolate=false`.

&#x20;

&#x20;

## **Conditionals** <a href="#conditionals" id="conditionals"></a>

> **If / ElseIf / Else**
>
> The _#if_ directive in Velocity allows for text to be included when the web page is generated, on the conditional that the if statement is true. For example:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #if( $foo )   <strong>Velocity!</strong>#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> The variable _$foo_ is evaluated to determine whether it is true, which will happen under one of two circumstances: (i) _$foo_ is a boolean (true/false) which has a true value, or (ii) the value is not null. Remember that the Velocity context only contains Objects, so when we say 'boolean', it will be represented as a Boolean (the class). This is true even for methods that return `boolean` - the introspection infrastructure will return a `Boolean` of the same logical value.
>
> The content between the _#if_ and the _#end_ statements become the output if the evaluation is true. In this case, if _$foo_ is true, the output will be: "Velocity!". Conversely, if _$foo_ has a null value, or if it is a boolean false, the statement evaluates as false, and there is no output.
>
> An _#elseif_ or _#else_ element can be used with an _#if_ element. Note that the Velocity Templating Engine will stop at the first expression that is found to be true. In the following example, suppose that _$foo_ has a value of 15 and _$bar_ has a value of 6.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #if( $foo < 10 )    <strong>Go North</strong>#elseif( $foo == 10 )    <strong>Go East</strong>#elseif( $bar == 6 )    <strong>Go South</strong>#else    <strong>Go West</strong>#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> In this example, _$foo_ is greater than 10, so the first two comparisons fail. Next _$bar_ is compared to 6, which is true, so the output is **Go South**.
>
> Please note that currently, Velocity's numeric comparisons are constrained to Integers - anything else will evaluate to _false_. The only exception to this is equality '==', where Velocity requires that the objects on each side of the '==' is of the _same_ class.
>
> **Relational and Logical Operators**
>
> Velocity uses the equivalent operator to determine the relationships between variables. Here is a simple example to illustrate how the equivalent operator is used.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set ($foo = "deoxyribonucleic acid")#set ($bar = "ribonucleic acid")#if ($foo == $bar)  In this case it's clear they aren't equivalent. So...#else  They are not equivalent and this will be the output.#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Velocity has logical AND, OR and NOT operators as well. For further information, please see the [VTL Reference Guide](http://velocity.apache.org/engine/1.4/vtl-reference-guide.html) Below are examples demonstrating the use of the logical AND, OR and NOT operators.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> ## logical AND#if( $foo && $bar )   <strong> This AND that</strong>#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> The _#if()_ directive will only evaluate to true if both _$foo_ and _$bar_ are true. If _$foo_ is false, the expression will evaluate to false; _$bar_ will not be evaluated. If _$foo_ is true, the Velocity Templating Engine will then check the value of _$bar_; if _$bar_ is true, then the entire expression is true and **This AND that** becomes the output. If _$bar_ is false, then there will be no output as the entire expression is false.
>
> Logical OR operators work the same way, except only one of the references need evaluate to true in order for the entire expression to be considered true. Consider the following example.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> ## logical OR#if( $foo || $bar )    <strong>This OR That</strong>#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> If _$foo_ is true, the Velocity Templating Engine has no need to look at _$bar_; whether _$bar_ is true or false, the expression will be true, and **This OR That** will be output. If _$foo_ is false, however, _$bar_ must be checked. In this case, if _$bar_ is also false, the expression evaluates to false and there is no output. On the other hand, if _$bar_ is true, then the entire expression is true, and the output is **This OR That**
>
> With logical NOT operators, there is only one argument :
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> ##logical NOT#if( !$foo )  <strong>NOT that</strong>#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Here, the if _$foo_ is true, then _!$foo_ evaluates to false, and there is no output. If _$foo_ is false, then _!$foo_ evaluates to true and **NOT that** will be output. Be careful not to confuse this with the _quiet reference $!foo_ which is something altogether different.

&#x20;

&#x20;

## **Loops** <a href="#loops" id="loops"></a>

> **Foreach Loop**
>
> The _#foreach_ element allows for looping. For example:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> <ul>#foreach( $product in $allProducts )    <li>$product</li>#end</ul>
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> This _#foreach_ loop causes the _$allProducts_ list (the object) to be looped over for all of the products (targets) in the list. Each time through the loop, the value from _$allProducts_ is placed into the _$product_ variable.
>
> The contents of the _$allProducts_ variable is a Vector, a Hashtable or an Array. The value assigned to the _$product_ variable is a Java Object and can be referenced from a variable as such. For example, if _$product_ was really a Product class in Java, its name could be retrieved by referencing the _$product.Name_ method (ie: _$Product.getName()_).
>
> Lets say that _$allProducts_ is a Hashtable. If you wanted to retrieve the key values for the Hashtable as well as the objects within the Hashtable, you can use code like this:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> <ul>#foreach( $key in $allProducts.keySet() )    <li>Key: $key -> Value: $allProducts.get($key)</li>#end</ul>
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Velocity provides an easy way to get the loop counter so that you can do something like the following:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> <table>#foreach( $customer in $customerList )    <tr><td>$velocityCount</td><td>$customer.Name</td></tr>#end</table>
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> The default name for the loop counter variable reference, which is specified in the velocity.properties file, is $velocityCount. By default the counter starts at 1, but this can be set to either 0 or 1 in the `velocity.properties` file. Here's what the loop counter properties section of the `velocity.properties` file appears:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> # Default name of the loop counter# variable reference.directive.foreach.counter.name = velocityCount# Default starting value of the loop# counter variable reference.directive.foreach.counter.initial.value = 1
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)

&#x20;

&#x20;

## **Include** <a href="#include" id="include"></a>

> The _#include_ script element allows the template designer to import a local file, which is then inserted into the location where the _#include_ directive is defined. The contents of the file are not rendered through the template engine. For security reasons, the file to be included may only be under TEMPLATE\_ROOT.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #include( "one.txt" )
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> The file to which the _#include_ directive refers is enclosed in quotes. If more than one file will be included, they should be separated by commas.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #include( "one.gif","two.txt","three.htm" )
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> The file being included need not be referenced by name; in fact, it is often preferable to use a variable instead of a filename. This could be useful for targeting output according to criteria determined when the page request is submitted. Here is an example showing both a filename and a variable.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #include( "greetings.txt", $seasonalstock )
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)

&#x20;

&#x20;

## **Parse** <a href="#parse" id="parse"></a>

> The _#parse_ script element allows the template designer to import a local file that contains VTL. Velocity will parse the VTL and render the template specified.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #parse( "me.vm" )
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Like the _#include_ directive, _#parse_ can take a variable rather than a template. Any templates to which _#parse_ refers must be included under TEMPLATE\_ROOT. Unlike the _#include_ directive, _#parse_ will only take a single argument.
>
> VTL templates can have _#parse_ statements referring to templates that in turn have _#parse_ statements. By default set to 10, the _parse\_directive.maxdepth_ line of the `velocity.properties` allows users to customize maximum number of _#parse_ referrals that can occur from a single template. (Note: If the _parse\_directive.maxdepth_ property is absent from the `velocity.properties` file, Velocity will set this default to 10.) Recursion is permitted, for example, if the template `dofoo.vm` contains the following lines:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> Count down.#set( $count = 8 )#parse( "parsefoo.vm" )All done with dofoo.vm!
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> It would reference the template `parsefoo.vm`, which might contain the following VTL:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> $count#set( $count = $count - 1 )#if( $count > 0 )    #parse( "parsefoo.vm" )#else    All done with parsefoo.vm!#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> After "Count down." is displayed, Velocity passes through `parsefoo.vm`, counting down from 8. When the count reaches 0, it will display the "All done with parsefoo.vm!" message. At this point, Velocity will return to `dofoo.vm` and output the "All done with dofoo.vm!" message.

&#x20;

&#x20;

## **Stop** <a href="#stop" id="stop"></a>

> The _#stop_ script element allows the template designer to stop the execution of the template engine and return. This is useful for debugging purposes.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #stop
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)

&#x20;

&#x20;

## **Velocimacros** <a href="#velocimacros" id="velocimacros"></a>

> The _#macro_ script element allows template designers to define a repeated segment of a VTL template. Velocimacros are very useful in a wide range of scenarios both simple and complex. This Velocimacro, created for the sole purpose of saving keystrokes and minimizing typographic errors, provides an introduction to the concept of Velocimacros.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #macro( d )<tr><td></td></tr>#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> The Velocimacro being defined in this example is _d_, and it can be called in a manner analogous to any other VTL directive:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #d()
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> When this template is called, Velocity would replace _#d()_ with a row containing a single, empty data cell.
>
> A Velocimacro could take any number of arguments -- even zero arguments, as demonstrated in the first example, is an option -- but when the Velocimacro is invoked, it must be called with the same number of arguments with which it was defined. Many Velocimacros are more involved than the one defined above. Here is a Velocimacro that takes two arguments, a color and an array.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #macro( tablerows $color $somelist )#foreach( $something in $somelist )    <tr><td bgcolor=$color>$something</td></tr>#end#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> The Velocimacro being defined in this example, _tablerows_, takes two arguments. The first argument takes the place of _$color_, and the second argument takes the place of _$somelist_.
>
> Anything that can be put into a VTL template can go into the body of a Velocimacro. The _tablerows_ Velocimacro is a _foreach_ statement. There are two _#end_ statements in the definition of the _#tablerows_ Velocimacro; the first belongs to the _#foreach_, the second ends the Velocimacro definition.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $greatlakes = ["Superior","Michigan","Huron","Erie","Ontario"] )#set( $color = "blue" )<table>    #tablerows( $color $greatlakes )</table>
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Notice that _$greatlakes_ takes the place of _$somelist_. When the _#tablerows_ Velocimacro is called in this situation, the following output is generated:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> <table>    <tr><td bgcolor="blue">Superior</td></tr>    <tr><td bgcolor="blue">Michigan</td></tr>    <tr><td bgcolor="blue">Huron</td></tr>    <tr><td bgcolor="blue">Erie</td></tr>    <tr><td bgcolor="blue">Ontario</td></tr></table>
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Velocimacros can be defined _inline_ in a Velocity template, meaning that it is unavailable to other Velocity templates in the same campus. Defining a Velocimacro such that it can be shared by all templates has obvious advantages: it reduces the need to redefine the Velocimacro on numerous templates, saving work and reducing the chance of error, and ensures that a single change to a macro available to more than one template.
>
> Were the _#tablerows($color $list)_ Velocimacro defined in a Velocimacros template library, this macro could be used on any of the regular templates. It could be used many times and for many different purposes. In the template `mushroom.vm` devoted to all things fungi, the _#tablerows_ Velocimacro could be invoked to list the parts of a typical mushroom:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $parts = ["volva","stipe","annulus","gills","pileus"] )#set( $cellbgcol = "#CC00FF" )<table>#tablerows( $cellbgcol $parts )</table>
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> When fulfilling a request for `mushroom.vm`, Velocity would find the _#tablerows_ Velocimacro in the template library (defined in the `velocity.properties` file) and generate the following output:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> <table>    <tr><td bgcolor="#CC00FF">volva</td></tr>    <tr><td bgcolor="#CC00FF">stipe</td></tr>    <tr><td bgcolor="#CC00FF">annulus</td></tr>    <tr><td bgcolor="#CC00FF">gills</td></tr>    <tr><td bgcolor="#CC00FF">pileus</td></tr></table>
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)**Velocimacro Arguments**
>
> Velocimacros can take as arguments any of the following VTL elements :
>
> * Reference : anything that starts with '$'
> * String literal : something like "$foo" or 'hello'
> * Number literal : 1, 2 etc
> * IntegerRange : \[ 1..2] or \[$foo .. $bar]
> * ObjectArray : \[ "a", "b", "c"]
> * boolean value true
> * boolean value false
>
> When passing references as arguments to Velocimacros, please note that references are passed 'by name'. This means that their value is 'generated' at each use inside the Velocimacro. This feature allows you to pass references with method calls and have the method called at each use. For example, when calling the following Velocimacro as shown
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
>      #macro( callme $a )         $a $a $a     #end     #callme( $foo.bar() )   
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> results in the method bar() of the reference $foo being called 3 times.
>
> At first glance, this feature appears surprising, but when you take into consideration the original motivation behind Velocimacros -- to eliminate cut'n'paste duplication of commonly used VTL -- it makes sense. It allows you to do things like pass stateful objects, such as an object that generates colors in a repeating sequence for coloring table rows, into the Velocimacro.
>
> If you need to circumvent this feature, you can always just get the value from the method as a new reference and pass that :
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
>      #set( $myval = $foo.bar() )     #callme( $myval )   
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)**Velocimacro Properties**
>
> Several lines in the `velocity.properties` file allow for flexible implementation of Velocimacros. Note that these are also documented in the [Developer Guide](http://velocity.apache.org/engine/1.4/developer-guide.html).
>
> `velocimacro.library` - A comma-separated list of all Velocimacro template libraries. By default, Velocity looks for a single library: _VM\_global\_library.vm_. The configured template path is used to find the Velocimacro libraries.
>
> `velocimacro.permissions.allow.inline` - This property, which has possible values of true or false, determines whether Velocimacros can be defined in regular templates. The default, true, allows template designers to define Velocimacros in the templates themselves.
>
> `velocimacro.permissions.allow.inline.to.replace.global` - With possible values of true or false, this property allows the user to specify if a Velocimacro defined inline in a template can replace a globally defined template, one that was loaded on startup via the `velocimacro.library` property. The default, `false`, prevents Velocimacros defined inline in a template from replacing those defined in the template libraries loaded at startup.
>
> `velocimacro.permissions.allow.inline.local.scope` - This property, with possible values of true or false, defaulting to false, controls if Velocimacros defined inline are 'visible' only to the defining template. In other words, with this property set to true, a template can define inline VMs that are usable only by the defining template. You can use this for fancy VM tricks - if a global VM calls another global VM, with inline scope, a template can define a private implementation of the second VM that will be called by the first VM when invoked by that template. All other templates are unaffected.
>
> `velocimacro.context.localscope` - This property has the possible values true or false, and the default is false. When true, any modifications to the context via #set() within a Velocimacro are considered 'local' to the Velocimacro, and will not permanently affect the context.
>
> `velocimacro.library.autoreload` - This property controls Velocimacro library autoloading. The default value is `false`. When set to `true` the source Velocimacro library for an invoked Velocimacro will be checked for changes, and reloaded if necessary. This allows you to change and test Velocimacro libraries without having to restart your application or servlet container, just like you can with regular templates. This mode only works when caching is _off_ in the resource loaders (e.g. `file.resource.loader.cache = false` ). This feature is intended for development, not for production.
>
> **Velocimacro Trivia**
>
> Currently, Velocimacros must be defined before they are first used in a template. This means that your #macro() declarations should come before using the Velocimacros.
>
> This is important to remember if you try to #parse() a template containing inline #macro() directives. Because the #parse() happens at runtime, and the parser decides if a VM-looking element in the template is a VM at parsetime, #parse()-ing a set of VM declarations won't work as expected. To get around this, simply use the `velocimacro.library` facility to have Velocity load your VMs at startup.

&#x20;

&#x20;

## **Escaping VTL Directives** <a href="#escaping-vtl-directives" id="escaping-vtl-directives"></a>

> VTL directives can be escaped with the backslash character ("\\") in a manner similar to valid VTL references.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> ## #include( "a.txt" ) renders as <contents of a.txt>#include( "a.txt" )## \#include( "a.txt" ) renders as \#include( "a.txt" )\#include( "a.txt" )## \\#include ( "a.txt" ) renders as \<contents of a.txt>\\#include ( "a.txt" )
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Extra care should be taken when escaping VTL directives that contain multiple script elements in a single directive (such as in an if-else-end statements). Here is a typical VTL if-statement:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #if( $jazz )    Vyacheslav Ganelin#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> If _$jazz_ is true, the output is
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> Vyacheslav Ganelin
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> If _$jazz_ is false, there is no output. Escaping script elements alters the output. Consider the following case:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> \#if( $jazz )    Vyacheslav Ganelin\#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Whether _$jazz_ is true or false, the output will be
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
>  #if($ jazz )     Vyacheslav Ganelin #end 
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> In fact, because all script elements are escaped, _$jazz_ is never evaluated for it's boolean value. Suppose backslashes precede script elements that are legitimately escaped:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> \\#if( $jazz )   Vyacheslav Ganelin\\#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> In this case, if _$jazz_ is true, the output is
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> \ Vyacheslav Ganelin\
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> To understand this, note that the `#if( arg )` when ended by a newline (return) will omit the newline from the output. Therefore, the body of the `#if()` block follows the first '\\', rendered from the '\\\\' preceding the `#if()`. The last \ is on a different line than the text because there is a newline after 'Ganelin', so the final \\\\, preceding the `#end` is part of the body of the block.
>
> If _$jazz_ is false, there is no output. Note that things start to break if script elements are not properly escaped.
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> \\\#if( $jazz )    Vyacheslave Ganelin\\#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Here the _#if_ is escaped, but there is an _#end_ remaining; having too many endings will cause a parsing error.

&#x20;

&#x20;

## **VTL: Formatting Issues** <a href="#vtl-formatting-issues" id="vtl-formatting-issues"></a>

> Although VTL in this user guide is often displayed with newlines and whitespaces, the VTL shown below
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> #set( $imperial = ["Munetaka","Koreyasu","Hisakira","Morikune"] )#foreach( $shogun in $imperial )    $shogun#end
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> is equally valid as the following snippet that Geir Magnusson Jr. posted to the Velocity user mailing list to illustrate a completely unrelated point:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> Send me #set($foo = ["$10 and ","a cake"])#foreach($a in $foo)$a #end please.
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> Velocity's behaviour is to gobble up excess whitespace. The preceding directive can be written as:
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> Send me#set( $foo = ["$10 and ","a cake"] )#foreach( $a in $foo )$a#endplease.
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> or as
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> ```
> Send me#set($foo       = ["$10 and ","a cake"])                 #foreach           ($a in $foo )$a         #end please.
> ```
>
> ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> In each case the output will be the same.

&#x20;

&#x20;

## **Other Features and Miscellany** <a href="#other-features-and-miscellany" id="other-features-and-miscellany"></a>

> ### **Math** <a href="#math" id="math"></a>
>
> > Velocity has a handful of built-in mathematical functions that can be used in templates with the _set_ directive. The following equations are examples of addition, subtraction, multiplication and division, respectively:
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > #set( $foo = $bar + 3 )#set( $foo = $bar - 4 )#set( $foo = $bar * 6 )#set( $foo = $bar / 2 )
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > When a division operation is performed, the result will be an integer. Any remainder can be obtained by using the modulus (_%_) operator.
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > #set( $foo = $bar % 5 )
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > Only integers (...-2, -1, 0, 1, 2...) are permissible when performing mathematical equations in Velocity; when a non-integer is used, it is logged and a null will be returned as the output.
>
> &#x20;
>
> ### **Range Operator** <a href="#range-operator" id="range-operator"></a>
>
> > The range operator can be used in conjunction with _#set_ and _#foreach_ statements. Useful for its ability to produce an object array containing integers, the range operator has the following construction:
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > [n..m]
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > Both _n_ and _m_ must either be or produce integers. Whether _m_ is greater than or less than _n_ will not matter; in this case the range will simply count down. Examples showing the use of the range operator as provided below:
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > First example:#foreach( $foo in [1..5] )$foo#endSecond example:#foreach( $bar in [2..-2] )$bar#endThird example:#set( $arr = [0..1] )#foreach( $i in $arr )$i#endFourth example:[1..3]
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > Produces the following output:
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > First example:1 2 3 4 5Second example:2 1 0 -1 -2Third example:0 1Fourth example:[1..3]
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > Note that the range operator only produces the array when used in conjunction with _#set_ and _#foreach_ directives, as demonstrated in the fourth example.
> >
> > Web page designers concerned with making tables a standard size, but where some will not have enough data to fill the table, will find the range operator particularly useful.
>
> &#x20;
>
> ### **Advanced Issues: Escaping and !** <a href="#advanced-issues-escaping-and" id="advanced-issues-escaping-and"></a>
>
> > When a reference is silenced with the _!_ character and the _!_ character preceded by an _\\_ escape character, the reference is handled in a special way. Note the differences between regular escaping, and the special case where _\\_ precedes _!_ follows it:
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > #set( $foo = "bar" )$\!foo$\!{foo}$\\!foo$\\\!foo
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > This renders as:
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > $!foo$!{foo}$\!foo$\\!foo
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > Contrast this with regular escaping, where _\\_ precedes _$_:
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > \$foo\$!foo\$!{foo}\\$!{foo}
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > This renders as:
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > \$foo\$!foo\$!{foo}\bar
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
>
> &#x20;
>
> ### **Velocimacro Miscellany** <a href="#velocimacro-miscellany" id="velocimacro-miscellany"></a>
>
> > This section is a mini-FAQ on topics relating to Velocimacros. Thissection will change over time, so it's worth checking for new informationfrom time to time.
> >
> > Note : Throughout this section, 'Velocimacro' will commonly be abbreviatedas 'VM'.
> >
> > **Can I use a directive or another VM as an argument to a VM?**
> >
> > Example : `#center( #bold("hello") )`
> >
> > No. A directive isn't a valid argument to a directive, and for most practicalpurposes, a VM is a directive.
> >
> > _However..._, there are things you can do. One easy solution is to takeadvantage of the fact that 'doublequote' (") renders it's contents. So youcould do something like
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > #set($stuff = "#bold('hello')" )#center( $stuff )
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > You can save a step...
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > #center( "#bold( 'hello' )" )
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > Please note that in the latter example the argis evaluated _inside_ the VM, not at thecalling level. In other words, the argument tothe VM is passed in in its entirety and evaluated within the VMit was passed into. This allows you to do things like :
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > #macro( inner $foo )  inner : $foo#end#macro( outer $foo )   #set($bar = "outerlala")   outer : $foo#end#set($bar = 'calltimelala')#outer( "#inner($bar)" )
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > Where the output is
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > Outer : inner : outerlala
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > because the evaluation of the "#inner($bar)" happens inside #outer(), so the$bar value set inside #outer() is the one that's used.
> >
> > This is an intentional and jealously guarded feature - args are passed 'byname' into VMs, so you can hand VMs things like stateful references such as
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > #macro( foo $color )  <tr bgcolor=$color><td>Hi</td></tr>  <tr bgcolor=$color><td>There</td></tr>#end#foo( $bar.rowColor() )
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > And have rowColor() called repeatedly, rather than just once. To avoid that,invoke the method outside of the VM, and pass the value into the VM.
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> > #set($color = $bar.rowColor())#foo( $color )
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)**Can I register Velocimacros via #parse() ?**
> >
> > Currently, Velocimacros must be defined before they are first used in a template. This means that your #macro() declarations should come before using the Velocimacros.
> >
> > This is important to remember if you try to #parse() a template containing inline #macro() directives. Because the #parse() happens at runtime, and the parser decides if a VM-looking element in the template is a VM at parsetime, #parse()-ing a set of VM declarations won't work as expected. To get around this, simply use the `velocimacro.library` facility to have Velocity load your VMs at startup.
> >
> > **What is Velocimacro Autoreloading?**
> >
> > There is a property, meant to be used in _development_, not production :
> >
> > `velocimacro.library.autoreload`
> >
> > which defaults to false. When set to true _along with_
> >
> > `<type>.resource.loader.cache = false`
> >
> > (where \<type> is the name of the resource loader that you are using, such as 'file') then the Velocity engine will automatically reload changes to your Velocimacro library files when you make them, so you do not have to dump the servlet engine (or application) or do other tricks to have your Velocimacros reloaded.
> >
> > Here is what a simple set of configuration properties would look like.
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> >     file.resource.loader.path = templates    file.resource.loader.cache = false    velocimacro.library.autoreload = true    
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > Don't keep this on in production.
>
> &#x20;
>
> ### **String Concatenation** <a href="#string-concatenation" id="string-concatenation"></a>
>
> > A common question that developers ask is _How do I do String concatenation? Is there any analogue to the '+' operator in Java?_.
> >
> > To do concatenation of references in VTL, you just have to 'put them together'. The context of where you want to put them together does matter, so we will illustrate with some examples.
> >
> > In the regular 'schmoo' of a template (when you are mixing it in with regular content) :
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> >        #set( $size = "Big" )       #set( $name = "Ben" )      The clock is $size$name.   
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > and the output will render as 'The clock is BigBen'. For more interesting cases, such as when you want to concatenate strings to pass to a method, or to set a new reference, just do
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> >       #set( $size = "Big" )      #set( $name = "Ben" )      #set($clock = "$size$name" )      The clock is $clock.    
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > Which will result in the same output. As a final example, when you want to mix in 'static' strings with your references, you may need to use 'formal references' :
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > ```
> >       #set( $size = "Big" )      #set( $name = "Ben" )      #set($clock = "${size}Tall$name" )      The clock is $clock.    
> > ```
> >
> > ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/void.gif)
> >
> > Now the output is 'The clock is BigTallBen'. The formal notation is needed so the parser knows you mean to use the reference '$size' versus '$sizeTall' which it would if the '{}' weren't there.
>
> &#x20;

&#x20;

&#x20;

## **Feedback** <a href="#feedback" id="feedback"></a>

> If you encounter any mistakes in this manual or have other feedback related to the Velocity User Guide, please email the [Velocity user list](mailto:velocity-user@jakarta.apache.org). Thanks!

&#x20;

&#x20;

© NexPort Solutions 2017. All Rights Reserved.

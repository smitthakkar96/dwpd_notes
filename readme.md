# Dwpd 

## Embedded tag:
The HTML <embed> tag represents a container for external application or interactive content.

example : 
`<embed src="/html/yourfile.mdi" width="250" height="100" />`

### Attributes: 
height, src, type, width

## li tag: 
  - The `<li>` tag defines a list item.
  - The `<li>` tag is used in ordered lists(`<ol>`), unordered lists (`<ul>`), and in menu lists (`<menu>`).

Example: 
``` html
<ol>
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
</ol>
<ul>
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
</ul>
```

## audio and video tag:
used to embedded audio or video content 
``` html
<audio controls>
    <source src="horse.ogg" type="audio/ogg">
    <source src="horse.mp3" type="audio/mpeg">
    Your browser does not support the audio tag.
</audio>
```

### formats supported
MP3, Ogg, Waw
### attributes
autoplay, controls, loop, muted, preload, src

## font tag
The `<font>` tag specifies the font face, font size, and color of text.
Example:
``` html 
<font size="3" color="red">This is some text!</font>
<font size="2" color="blue">This is some text!</font>
<font face="verdana" color="green">This is some text!</font>
```

### attributes:
size, color, face

## tr tag
The <tr> tag defines a row in an HTML table.
Example:
``` html
<table>
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```

## nav tag
The HTML <nav> tag specifies a section that contains only navigation links.
Example:

``` html 
<nav>
  <a href="/html/">HTML</a> |
  <a href="/css/">CSS</a> |
  <a href="/js/">JavaScript</a> |
  <a href="/jquery/">jQuery</a>
</nav>
```

## HTML4 vs HTML5
  - Audio and video were not part of previous HTML version specifications, however, both are the integral part of HTML5 specifications.
  - Vector graphics is also an integral part of HTML5 such as SVG and canvas while vector graphics is possible in HTML with the help of various technologies such as VML, Silver-light, Flash, etc.
  - In HTML, browser cache can be used as temporary storage. In case of HTML5, application cache, web SQL database, and web storage is used.
  - HTML doesn’t allows JavaScript to run in web browser, it runs in same thread as browser interface. HTML5 allows JavaScript to run in background that is possible because of JS Web worker API in HTML5.
  - HTML works smoothly with all old browsers while most of the modern web browsers have started supporting HTML5 specifications. These browsers include: Firefox, Mozilla, Chrome, Opera, Safari, etc.

## Inline Styles
Inline styles are the styles written under style attribute of any tag

## CSS2 vs CSS3
  - New selectors. With CSS3 you can select attributes with some fancy symbols (mostly modeled after regex, I believe). There are also new pseudo -classes that allow you to select child/sibling elements (eg :nth-child(even) allows you to select only the even numbered elements, extremely useful for    alternating row colors in a table)
  - Text Effects. Text-shadows and a handy new word-wrapping feature
  - Transforms & Animations. Exactly like it sounds. You can specify timer properties and keyframes to create animations entirely using CSS
  - Media Queries - enhancement of @media rules and "media" HTML markup element.
  - Backgrounds and borders - describes background colors and images and the style of borders.
  - Transitions - defines a property to animate the transitions between pseudo-classes.

## echo vs print
  - print only takes one parameter, while echo can have multiple parameters.
  - print returns a value (1), so can be used as an expression.
  - echo is slightly faster.

Syntax for both

## settype
The settype() function is used to set the type of a variable.
parameters var_name, var_type

``` php 
<?php  
$var1='98';  
$var2='01';  
settype($var1, "integer");  
settype($var2, "integer");  
echo ($var1.'<br>');  
echo ($var2.'<br>');  
echo ($var1+$var2.'<br>');  
?>
```

## define function
The define() function defines a constant.

Constants are much like variables, except for the following differences:

  - A constant's value cannot be changed after it is set
  - Constant names do not need a leading dollar sign ($)
  - Constants can be accessed regardless of scope
  - Constant values can only be strings and numbers

``` php
<?php
define("GREETING","Hello you! How are you today?");
echo constant("GREETING");

const PI = 3.14;
$area = PI * 12;
?>
```

## switch statement in php
``` php 
<?php
$favcolor = "red";

switch ($favcolor) {
    case "red":
        echo "Your favorite color is red!";
        break;
    case "blue":
        echo "Your favorite color is blue!";
        break;
    case "green":
        echo "Your favorite color is green!";
        break;
    default:
        echo "Your favorite color is neither red, blue, nor green!";
}
?>
```

## ternary if in php
`$value = ($condition) ? 'Truthy Value' : 'Falsey Value';`

## pass by reference 
``` php 
<?php
function add_some_extra(&$string)
{
    $string .= 'and something extra.';
}

$str = 'This is a string, ';
add_some_extra($str);
echo $str;    // outputs 'This is a string, and something extra.'
?>
```

## string function
ltrim, rtrim, strlen, strtolower, strtoupper, echo, print, trim

## date function 
Format a local time/date
date ( string $format [, int $timestamp = time() ] )

formats:
  - d - day of Month
  - D - textual representation of date
  - M - short text month
  - m - month in number
  - Y - 4 digit representation of year
  - y - 2 digit representation of year
  - H - 24 hour format
  - h - 12 hour format
  - i - minutes with leading zeros
  - s - seconds 

## textarea
attributes:
  - autofocus
  - cols
  - rows
  - maxlength
  - form
  - placeholder

## Radio button
Radio buttons let a user select ONE of a limited number of choices:

``` html
<form>
  <input type="radio" name="gender" value="male" checked> Male<br>
  <input type="radio" name="gender" value="female"> Female<br>
  <input type="radio" name="gender" value="other"> Other
</form>
```  

## checkbox button
checkbox allows the user to select multiple choices from given list

``` html
<form>
  <input type="checkbox" name="gender" value="male" checked> Male<br>
  <input type="checkbox" name="gender" value="female"> Female<br>
  <input type="checkbox" name="gender" value="other"> Other
</form>
```

## setcookie
used to set cookie
``` php
setcookie($cookie_name, $cookie_value, time() + (86400 * 30), "/"); // 86400 = 1 day
$_COOKIE['cookie_name']
```
## 


## mysql_connect
used to open connection with mysql database

``` php
<?php
// we connect to example.com and port 3307
$link = mysql_connect('example.com:3307', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Could not connect: ' . mysql_error());
}
echo 'Connected successfully';
mysql_close($link);

// we connect to localhost at port 3307
$link = mysql_connect('127.0.0.1:3307', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Could not connect: ' . mysql_error());
}
echo 'Connected successfully';
mysql_close($link);
?>
```
selecting database: `$db = mysql_select_db(DB_NAME, $link) or die("Couldn't select database.");`

## mysql_query

This command is used to execute query against mysql database.

``` php
<?php
$result = mysql_query('SELECT * WHERE 1=1');
if (!$result) {
    die('Invalid query: ' . mysql_error());
}

?>
```
## mysql_num_rows

The mysql_num_rows() is used to get the number of rows in a MySQL result handle.

``` php
<?php  
$con = mysql_connect("localhost", "root", "mypass");  
$selectdb = mysql_select_db("tutorials",$con);  
$result = mysql_query("select * from tutorials");  
$number_of_rows = mysql_num_rows($result);  
echo "Number of rows fetched are : ". $number_of_rows;  
?>
```

## mysql field types

<table class="std_table">
  <thead>
  <tr>
    <th>Data Type Syntax</th>
    <th class="hidden-xs">Maximum Size</th>
    <th>Explanation</th>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td>CHAR(<em>size</em>)</td>
    <td class="hidden-xs">Maximum size of 255 characters.</td>
    <td>Where <strong><em>size</em></strong> is the number of characters to store. Fixed-length strings. Space padded on right to equal <em><strong>size</strong></em> characters.</td>
  </tr>
  <tr>
    <td>VARCHAR(<em>size</em>)</td>
    <td class="hidden-xs">Maximum size of 255 characters.</td>
    <td>Where <strong><em>size</em></strong> is the number of characters to store. Variable-length string.</td>
  </tr>
  <tr>
    <td>TINYTEXT(<em>size</em>)</td>
    <td class="hidden-xs">Maximum size of 255 characters.</td>
    <td>Where <em><strong>size</strong></em> is the number of characters to store.</td>
  </tr>
  <tr>
    <td>TEXT(<em>size</em>)</td>
    <td class="hidden-xs">Maximum size of 65,535 characters.</td>
    <td>Where <em><strong>size</strong></em> is the number of characters to store.</td>
  </tr>
  <tr>
    <td>MEDIUMTEXT(<em>size</em>)</td>
    <td class="hidden-xs">Maximum size of 16,777,215 characters.</td>
    <td>Where <em><strong>size</strong></em> is the number of characters to store.</td>
  </tr>
  <tr>
    <td>LONGTEXT(<em>size</em>)</td>
    <td class="hidden-xs">Maximum size of 4GB or 4,294,967,295 characters.</td>
    <td>Where <em><strong>size</strong></em> is the number of characters to store.</td>
  </tr>
  <tr>
    <td>BINARY(<em>size</em>)</td>
    <td class="hidden-xs">Maximum size of 255 characters.</td>
    <td>Where <strong><em>size</em></strong> is the number of binary characters to store. Fixed-length strings. Space padded on right to equal <em><strong>size</strong></em> characters.<br>
        (Introduced in MySQL 4.1.2)</td>
  </tr>
  <tr>
    <td>VARBINARY(<em>size</em>)</td>
    <td class="hidden-xs">Maximum size of 255 characters.</td>
    <td>Where <strong><em>size</em></strong> is the number of characters to store. Variable-length string.<br>
        (Introduced in MySQL 4.1.2)</td>
  </tr>
  </tbody>
</table>

## What is css?

  - CSS stands for Cascading Style Sheets
  - CSS describes how HTML elements are to be displayed on screen, paper, or in other media
  - CSS saves a lot of work. It can control the layout of multiple web pages all at once
  - External stylesheets are stored in CSS files

Css are of three types:
  - inline
  - extrenal
  - internal

## Marquee
An HTML marquee is a scrolling piece of text displayed either horizontally across or vertically down your webpage depending on the settings. This is created by using HTML <marquees> tag.

``` html
<marquee attribute_name="attribute_value"....more attributes>

One or more lines or text message or image

</marquee>
```
<table class="table table-bordered">
<tbody><tr><th>Attribute</th><th>Description</th></tr>
<tr><td>width</td><td>This specifies the width of the marquee. This can be a value like 10 or 20% etc.</td></tr>
<tr><td>height</td><td>This specifies the height of the marquee. This can be a value like 10 or 20% etc.</td></tr>
<tr><td>direction</td><td>This specifies the direction in which marquee should scroll. This can be a value like <i>up</i>, <i>down</i>, <i>left</i> or <i>right</i>.</td></tr>
<tr><td>behavior</td><td>This specifies the type of scrolling of the marquee. This can have a value like <i>scroll</i>, <i>slide</i> and <i>alternate</i>.</td></tr>
<tr><td>scrolldelay</td><td>This specifies how long to delay between each jump. This will have a value like 10 etc.</td></tr>
<tr><td>scrollamount</td><td>This specifies the speed of marquee text. This can have a value like 10 etc.</td></tr>
<tr><td>loop</td><td>This specifies how many times to loop. The default value is INFINITE, which means that the marquee loops endlessly.</td></tr>
<tr><td>bgcolor</td><td>This specifies background color in terms of color name or color hex value.</td></tr>
<tr><td>hspace</td><td>This specifies horizontal space around the marquee.  This can be a value like 10 or 20% etc.</td></tr>
<tr><td>vspace</td><td>This specifies vertical space around the marquee. This can be a value like 10 or 20% etc.</td></tr>
</tbody></table>

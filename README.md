# Cool-CSS-Optimization-Techniques
Optimize css techniques

CSS optimization and file size reduction techniques that have been using by many web designers/ web developers. That means less characters in a CSS. Here are some cool examples how you can optimize your CSS.
1. Remove the last semicolon

Small but can help to reduce CSS file size.
1
2
3
4
5
6
h2 {
    font-family:verdana;
    padding:0;
    margin:5px 0;
    color:#333  
}
2. Extra zero

Yes this one is also very small.
01
02
03
04
05
06
07
08
09
10
h2 {
   padding: 0.1em;
   margin: 10.0em;
}
 
/* Replace with*/
h2 {
   padding: .1em;
   margin: 10em
}
3. Remove “px”

You can remove “px” from values set to “0px”
01
02
03
04
05
06
07
08
09
10
h2 {
    padding:0px; 
    margin:0px;
}
 
/* Replace with*/
h2 {
   padding:0; 
   margin:0
}
4. Using CSS shorthand

Yes this is a big one, it can make your multi-line properties to one liner
01
02
03
04
05
06
07
08
09
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
/* used for Margin */
  
h1 {margin:5px  10px  5px  10px;}
  
/* instead of */
h1 {margin-top:5px;
    margin-right:10px;
    margin-bottom:5px;
    margin-left:10px;
}
 
/*------------------------------------------------*/
 
/* used for border */
h1 {border:1px solid #CCC }
  
/* instead of */
h1 {border-width:1px;
    border-style:solid;
    border-color:#CCC;
}
 
/*------------------------------------------------*/
 
/* used for font */
h1 {font:italic small-caps bold 12px/160% "Lucida Grande",sans-serif;}
  
/*or with out some optional values*/
  
h1 {font:bold 12px/160% "Lucida Grande",sans-serif}
  
/* instead of */
h1 {font-style:italic;
    font-variant:small-caps;
    font-weight:bold;
    font-size:12px;
    line-height:160%;
    font-family:"Lucida Grande",sans-serif;
}
FOR FULL CSS SHORTHAND GUIDE, PLEASE CHECK OUT THIS ARTICLE.
http://www.mindfreakerstuff.com/2012/12/css3-and-css2-shorthand-guide/
5. Group similar Styles

One of the best Css trick to reduce css file size
Before
1
2
3
h1 { padding:5px 0; font-family:verdana; color:#FF00FF; font-size:16px;}
#block1  h1 {padding:5px 0; font-family:verdana; color:#FF00FF;  font-size:18px;}
#block2  h1 {padding:5px 0; font-family:verdana; color:#FF00FF; font-size:20px;}
After
1
2
3
h1 { padding:5px 0; font-family:verdana; color:#FF00FF; font-size:16px}
#block1  h1 {font-size:18px}
#block2  h1 {font-size:20px}
6. use simple and clean comment

1
2
3
4
5
6
7
/************************************/
/*          header block          */
/************************************/
  
vs
  
/* header block  */
7. Avoid using default values for HTML tags

1
2
3
4
5
6
7
8
/* following are default values for HTML tags for all browser */
h1 {font-weight: bold}
 
p {display:block}
 
p {text-align:left}
 
ul {list-style:disc outside none}
8. Reduce The Number of Line Breaks

01
02
03
04
05
06
07
08
09
10
h2 {
    font-family:verdana;
    padding:0;
    margin:5px 0;
    color:#333;
    text-decoration:underline;  
}
  
/* you can do it like this */
h2 {font-family:verdana;padding:0;margin:5px 0;color:#333;text-decoration:underline;}
9. Use Short Hexadecimal values for color

1
2
3
4
5
color: #ffffff  to  color:#fff
color: #000000  to  color:#000
color: #cccccc  to  color:#ccc
color: #999999  to  color:#999
color: #FF0000  to  color:red
9. Comma separated declarations for similar classes

1
2
3
4
h1, h2, h3, h4, h5, h6 {
    font-family:Helvetica, Verdana, sans-serif;
    color:#FF0000
}
10. Use Short Class and ID Names

checkout google.com and gmail CSS
01
02
03
04
05
06
07
08
09
10
.box-background-gray {
    background-color:#CCC;
    color:#FF0000
}
 
/*replace with*/
.bx-bg-gray {
    background-color:#CCC;
    color:#FF0000
}
11. Avoid using extra tr or ul / ol in class name for td and li

As td and li elements will be always under tr and ul/ol tag.
1
2
3
4
5
6
7
8
9
table tr td { /* properties */}
 
 /*  or  */
 
.todo-list ul li { /* properties */}
 
 /* replace with */
 table td { /* properties */}
.todo-list  li { /* properties */}
12. Use CSS compression tools

some of the popular CSS compression tools. Compression tools will surly reduce file size.
1. cssoptimiser : CSS parser and optimizer
2. Dust-Me Selectors: Firefox add-on that can find unused CSS selectors
3. http://www.cleancss.com/: CSS optimizer
4. YUI Compressor : Java tool to minify Javascript and CSS
5. iceyboard : : CSS optimizer

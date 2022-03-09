# json-to-tree
Convert single level json list that includes a 'parent' property, to a tree (in javascript)


1. Get json from url <http://www.mocky.io/v2/5c3c7ad13100007400a1a401>
1. transfer the json request into tree format
1. generate html tree using ul/ui like the example

![](Aspose.Words.8e417828-8fa7-4243-afbb-3438d4c68358.001.png)

1. style using the following css

```css
\* Remove default bullets *\
ul, #myUL {
   list-style-type: none;
}

\* Remove margins and padding from the parent ul *\
#myUL {
   margin: 0;
   padding: 0;
}

\* Style the caret/arrow *\
.caret {
   cursor: pointer; 
   user-select: none; \* Prevent text selection *\
}

\* Create the caret/arrow with a unicode, and style it *\
.caret::before {
   content: "\25B6";
   color: black;
   display: inline-block;
   margin-right: 6px;
}

\* Rotate the caret/arrow icon when clicked on (using JavaScript) *\
.caret-down::before {
   transform: rotate(90deg); 
}

\* Hide the nested list *\
.nested {
   display: none;
}

\* Show the nested list when the user clicks on the caret/arrow (with JavaScript) *\
.active {
   display: block;
}
```

1. BONUS - Write a function that can access with o(1) to each node in the tree by given **ID**


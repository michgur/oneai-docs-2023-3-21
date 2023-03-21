---
title: "Language Label"
slug: "language-label"
excerpt: "A name of a language."
hidden: false
createdAt: "2022-08-24T07:04:31.676Z"
updatedAt: "2022-11-22T12:29:55.026Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  I'm sorry but I don't speak <span class=\"label_box\">LANGUAGE</span><span class=\"label_text\"> Portuguese.</span>\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 120px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]



### Example Input

```
I'm sorry but I don't speak Portuguese.
```



### Example Output

```json
{
   "type":"name",
   "skill":"names",
   "name":"LANGUAGE",
   "value":"Portuguese language",
   "data":{
      
   },
   "span_text":"Portuguese",
   "span":[
      29,
      39
   ],
   "output_spans":[
      {
         "section":0,
         "start":29,
         "end":39
      }
   ]
}
```
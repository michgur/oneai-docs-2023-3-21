---
title: "GEO Label"
slug: "geo-label"
excerpt: "Countries and States"
hidden: false
createdAt: "2022-08-24T06:54:43.327Z"
updatedAt: "2022-09-18T09:58:21.000Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  I grew up in <span class=\"label_box\">GEO</span><span class=\"label_text\"> Wyoming.</span>\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 120px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]



### Example Input

```
I grew up in Wyoming.
```



### Example Output

```json
{
   "type":"name",
   "skill":"names",
   "name":"GEO",
   "value":"Wyoming",
   "data":{
      "type":"STATE",
      "country":"UNITED STATES"
   },
   "span_text":"Wyoming",
   "span":[
      13,
      20
   ],
   "output_spans":[
      {
         "section":0,
         "start":13,
         "end":20
      }
   ]
}
```



### Additional data

A GEO label can represent a state or a country. If the label represents a state, then the `data` field will be populated also with the country. For example, if the input is 

```
I live in NSW
```



the response will contain:

```json
{
   "type":"name",
   "skill":"names",
   "name":"GEO",
   "value":"New South Wales",
   "data":{
      "type":"STATE",
      "country":"AUSTRALIA"
   },
   "span_text":"NSW",
}
```



Notice also how the `value` of the label became the full unabbreviated name of the state.
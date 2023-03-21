---
title: "Competition Label"
slug: "competition-label"
hidden: false
createdAt: "2022-08-28T09:53:54.195Z"
updatedAt: "2022-08-28T09:53:54.195Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  Agent  2:23<br/>  \nSo when you have maybe 20 to 30 minutes, next week, just for a brief discovery call, and that way, you get a better understanding of our product and you see if it could be a value to you.<br/>\n<br/>\nProspect  3:10  <br/>\nProbably not. <span class=\"label_box\">COMPETITION</span><span class=\"label_text\"> We've got quite a bit in that space in the marketing side, so we might be sat there. </span>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 235px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
Agent  2:23  
So when you have maybe 20 to 30 minutes, next week, just for a brief discovery call, and that way, you get a better understanding of our product and you see if it could be a value to you.

Prospect  3:10  
Probably not. We've got quite a bit in that space in the marketing side, so we might be sat there. 
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "{\n   \"type\":\"sales-insights\",\n   \"skill\":\"sales-insights\",\n   \"name\":\"Competition\",\n   \"value\":\"We've got quite a bit in that space in the marketing side, so we might be sat there.\",\n   \"speaker\":\"Prospect\",\n   \"span_text\":\"We've got quite a bit in that space in the marketing side, so we might be sat there.\",\n   \"span\":[\n      234,\n      318\n   ],\n   \"output_spans\":[\n      {\n         \"section\":1,\n         \"start\":14,\n         \"end\":98\n      }\n   ]\n}",
      "language": "json"
    }
  ]
}
[/block]
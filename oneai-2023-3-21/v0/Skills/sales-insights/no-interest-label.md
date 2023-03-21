---
title: "No Interest Label"
slug: "no-interest-label"
hidden: false
createdAt: "2022-08-24T09:34:38.073Z"
updatedAt: "2022-08-24T09:38:39.082Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  Agent  1:13<br/>  \n Cuz I think our platform could help you guys out over at Giant Games.<br/>\n<br/>\nProspect  1:17  <br/>\n You seem to want to sell me something. So I'm going to say goodbye. <span class=\"label_box\">NO INTEREST</span><span class=\"label_text\"> Don't call again!</span>\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 235px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
Agent  1:13  
Cuz I think our platform could help you guys out over at Giant Games.

Prospect  1:17  
You seem to want to sell me something. So I'm going to say goodbye. Don't call again!
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "{\n   \"type\":\"sales-insights\",\n   \"skill\":\"sales-insights\",\n   \"name\":\"No interest\",\n   \"value\":\"Don't call again!\",\n   \"speaker\":\"Prospect\",\n   \"span_text\":\"Don't call again!\",\n   \"span\":[\n      170,\n      187\n   ],\n   \"output_spans\":[\n      {\n         \"section\":1,\n         \"start\":68,\n         \"end\":85\n      }\n   ]\n}",
      "language": "json"
    }
  ]
}
[/block]
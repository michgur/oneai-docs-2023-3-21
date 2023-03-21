---
title: "Location Label"
slug: "location-label"
excerpt: "Cities, buildings, airports, highways, bridges"
hidden: false
createdAt: "2022-08-24T06:53:05.489Z"
updatedAt: "2022-08-24T08:43:50.788Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  Let's meet in <span class=\"label_box\">LOCATION</span><span class=\"label_text\"> Seattle.</span>\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 120px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
Let's meet in Seattle.
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "{\n   \"type\":\"name\",\n   \"skill\":\"names\",\n   \"name\":\"LOCATION\",\n   \"value\":\"Seattle\",\n   \"data\":{\n      \"type\":\"CITY\"\n   },\n   \"span_text\":\"Seattle\",\n   \"span\":[\n      14,\n      21\n   ],\n   \"output_spans\":[\n      {\n         \"section\":0,\n         \"start\":14,\n         \"end\":21\n      }\n   ]\n}",
      "language": "json"
    }
  ]
}
[/block]
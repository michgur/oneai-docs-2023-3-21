---
title: "POS Label"
slug: "pos-label"
excerpt: "Positive sentiment"
hidden: false
createdAt: "2022-08-24T09:06:47.816Z"
updatedAt: "2022-08-24T09:10:40.410Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  <span class=\"label_box\">POSITIVE</span><span class=\"label_text\"> This is truly an amazing achievement.</span>\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 235px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
This is truly an amazing achievement.
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "{\n   \"type\":\"sentiment\",\n   \"skill\":\"sentiments\",\n   \"value\":\"POS\",\n   \"span_text\":\"This is truly an amazing achievement.\",\n   \"span\":[\n      0,\n      37\n   ],\n   \"output_spans\":[\n      {\n         \"section\":0,\n         \"start\":0,\n         \"end\":37\n      }\n   ]\n}",
      "language": "json"
    }
  ]
}
[/block]
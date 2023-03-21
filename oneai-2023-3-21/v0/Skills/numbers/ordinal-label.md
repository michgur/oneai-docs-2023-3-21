---
title: "Ordinal Label"
slug: "ordinal-label"
excerpt: "Position in a list - “first”, “second”, etc."
hidden: false
createdAt: "2022-08-24T07:46:33.023Z"
updatedAt: "2022-08-24T07:52:15.106Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  You'll be <span class=\"label_box\">ORDINAL</span><span class=\"label_text\"> first</span> to jump and you'll be <span class=\"label_box\">ORDINAL</span><span class=\"label_text\"> second.</span>\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 235px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
You'll be first to jump and you'll be second.
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "[\n   {\n      \"type\":\"number\",\n      \"skill\":\"numbers\",\n      \"name\":\"ORDINAL\",\n      \"value\":\"1\",\n      \"data\":{\n         \"numeric_value\":1\n      },\n      \"span_text\":\"first\",\n      \"span\":[\n         10,\n         15\n      ],\n      \"output_spans\":[\n         {\n            \"section\":0,\n            \"start\":10,\n            \"end\":15\n         }\n      ]\n   },\n   {\n      \"type\":\"number\",\n      \"skill\":\"numbers\",\n      \"name\":\"ORDINAL\",\n      \"value\":\"2\",\n      \"data\":{\n         \"numeric_value\":2\n      },\n      \"span_text\":\"second\",\n      \"span\":[\n         38,\n         44\n      ],\n      \"output_spans\":[\n         {\n            \"section\":0,\n            \"start\":38,\n            \"end\":44\n         }\n      ]\n   }\n]",
      "language": "json"
    }
  ]
}
[/block]
### Additional Data
[block:parameters]
{
  "data": {
    "h-0": "Name",
    "h-1": "Description",
    "h-2": "Example",
    "0-0": "`numeric_value`",
    "0-1": "The numeric value of the number",
    "0-2": "1000"
  },
  "cols": 3,
  "rows": 1
}
[/block]
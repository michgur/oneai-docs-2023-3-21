---
title: "Number Label"
slug: "number-label"
excerpt: "Numerals that do not fall under another type."
hidden: false
createdAt: "2022-08-24T07:50:30.612Z"
updatedAt: "2022-08-24T07:51:52.076Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  I can count to <span class=\"label_box\">NUMBER</span><span class=\"label_text\"> six.</span>\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 235px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
I can count to six.
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "{\n   \"type\":\"number\",\n   \"skill\":\"numbers\",\n   \"name\":\"NUMBER\",\n   \"value\":\"6\",\n   \"data\":{\n      \"numeric_value\":6\n   },\n   \"span_text\":\"six\",\n   \"span\":[\n      15,\n      18\n   ],\n   \"output_spans\":[\n      {\n         \"section\":0,\n         \"start\":15,\n         \"end\":18\n      }\n   ]\n}",
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
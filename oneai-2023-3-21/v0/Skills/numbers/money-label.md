---
title: "Money Label"
slug: "money-label"
excerpt: "Monetary values, including unit."
hidden: false
createdAt: "2022-08-24T07:40:52.279Z"
updatedAt: "2022-08-24T07:41:00.799Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  We made <span class=\"label_box\">MONEY</span><span class=\"label_text\"> a thousand bucks</span> in no time.\t\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 235px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
We made a thousand bucks in no time.
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "{\n   \"type\":\"number\",\n   \"skill\":\"numbers\",\n   \"name\":\"MONEY\",\n   \"value\":\"1,000\",\n   \"data\":{\n      \"numeric_value\":1000\n   },\n   \"span_text\":\"a thousand bucks\",\n   \"span\":[\n      8,\n      24\n   ],\n   \"output_spans\":[\n      {\n         \"section\":0,\n         \"start\":8,\n         \"end\":24\n      }\n   ]\n}",
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
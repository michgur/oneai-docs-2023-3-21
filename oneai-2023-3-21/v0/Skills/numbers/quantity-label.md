---
title: "Quantity Label"
slug: "quantity-label"
excerpt: "Measurements, such as weight or distance."
hidden: false
createdAt: "2022-08-24T07:44:32.380Z"
updatedAt: "2022-08-24T07:44:32.380Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  It's quite hard to run a <span class=\"label_box\">QUANTITY</span><span class=\"label_text\"> ten kilometer</span> run when you have extra <span class=\"label_box\">QUANTITY</span><span class=\"label_text\"> ten kilograms</span> on you.\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 235px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
It's quite hard to run a ten kilometer run when you have extra ten kilograms on you.
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "[\n   {\n      \"type\":\"number\",\n      \"skill\":\"numbers\",\n      \"name\":\"QUANTITY\",\n      \"value\":\"10\",\n      \"data\":{\n         \"numeric_value\":10\n      },\n      \"span_text\":\"ten kilometer\",\n      \"span\":[\n         25,\n         38\n      ],\n      \"output_spans\":[\n         {\n            \"section\":0,\n            \"start\":25,\n            \"end\":38\n         }\n      ]\n   },\n   {\n      \"type\":\"number\",\n      \"skill\":\"numbers\",\n      \"name\":\"QUANTITY\",\n      \"value\":\"10\",\n      \"data\":{\n         \"numeric_value\":10\n      },\n      \"span_text\":\"ten kilograms\",\n      \"span\":[\n         63,\n         76\n      ],\n      \"output_spans\":[\n         {\n            \"section\":0,\n            \"start\":63,\n            \"end\":76\n         }\n      ]\n   }\n]",
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
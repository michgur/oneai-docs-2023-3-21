---
title: "Needs & Features Label"
slug: "needs-and-features-label"
hidden: false
createdAt: "2022-08-24T09:22:54.300Z"
updatedAt: "2022-08-24T09:37:47.609Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  customer:<br/>\n\tYeah, anything. <span class=\"label_box\">NEEDS & FEATURES</span><span class=\"label_text\"> Anything that would prevent her from making costly mistakes would be highly appreciated.</span>\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 235px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
customer:
Yeah, anything. Anything that would prevent her from making costly mistakes would be highly appreciated.
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "{\n   \"type\":\"sales-insights\",\n   \"skill\":\"sales-insights\",\n   \"name\":\"Needs & Features\",\n   \"value\":\"Anything that would prevent her from making costly mistakes would be highly appreciated.\",\n   \"speaker\":\"customer\",\n   \"span_text\":\"Anything that would prevent her from making costly mistakes would be highly appreciated.\",\n   \"span\":[\n      4576,\n      4663\n   ],\n   \"output_spans\":[\n      {\n         \"section\":17,\n         \"start\":16,\n         \"end\":103\n      }\n   ]\n}",
      "language": "json"
    }
  ]
}
[/block]
---
title: "Law Label"
slug: "law-label"
excerpt: "Named documents made into laws."
hidden: false
createdAt: "2022-08-24T07:02:55.580Z"
updatedAt: "2022-08-24T07:03:26.268Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  According to the <span class=\"label_box\">LAW</span><span class=\"label_text\"> fifth amendment</span> you shouldn't do this.\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 120px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
According to the fifth amendment you shouldn't do this.
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "{\n   \"type\":\"name\",\n   \"skill\":\"names\",\n   \"name\":\"LAW\",\n   \"value\":\"Fifth Amendment to the United States Constitution\",\n   \"data\":{\n      \n   },\n   \"span_text\":\"the fifth amendment\",\n   \"span\":[\n      13,\n      32\n   ],\n   \"output_spans\":[\n      {\n         \"section\":0,\n         \"start\":13,\n         \"end\":32\n      }\n   ]\n}",
      "language": "json"
    }
  ]
}
[/block]
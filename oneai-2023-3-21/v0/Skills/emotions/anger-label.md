---
title: "Anger Label"
slug: "anger-label"
hidden: false
createdAt: "2022-08-24T08:06:24.739Z"
updatedAt: "2022-11-13T14:08:34.497Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  <span class=\"label_box\">ANGER</span><span class=\"label_text\"> I am very pissed off about all of this.</span>\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 120px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]



### Example Input

```
I am very pissed off about all of this.
```



### Example Output

```json
{
  "type": "emotion",
  "skill": "emotions",
  "name": "anger",
  "span_text": "I am very pissed off about all of this.",
  "span": [
    0,
    39
  ],
  "output_spans": [
    {
      "section": 0,
      "start": 0,
      "end": 39
    }
  ]
}
```
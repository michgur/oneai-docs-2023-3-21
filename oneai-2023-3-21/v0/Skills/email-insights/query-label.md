---
title: "Query Label"
slug: "query-label"
hidden: false
createdAt: "2022-11-13T14:15:55.824Z"
updatedAt: "2022-11-13T14:15:55.824Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n <span class=\"label_box\">QUERY</span><span class=\"label_text\"> Interested in a walk-through from one of our NLP experts?\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 120px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]



### Example Input

```
Interested in a walk-through from one of our NLP experts?
```



### Example Output

```json
{
  "type": "service-email-insights",
  "skill": "service-email-insights",
  "name": "Request",
  "value": "Feel free to make a free account and explore the calibration capabilities, maybe you can launch a batch in the morning and check the results at lunchtime!",
  "span_text": "Feel free to make a free account and explore the calibration capabilities, maybe you can launch a batch in the morning and check the results at lunchtime!",
  "span": [
    56,
    210
  ],
  "output_spans": [
    {
      "section": 0,
      "start": 56,
      "end": 210
    }
  ]
}
```
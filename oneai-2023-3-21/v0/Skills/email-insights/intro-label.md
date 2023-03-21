---
title: "Intro Label"
slug: "intro-label"
hidden: false
createdAt: "2022-11-13T14:02:05.754Z"
updatedAt: "2022-11-13T14:07:48.476Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n <span class=\"label_box\">INTRO</span><span class=\"label_text\"> Hi George,</p>\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 120px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]



### Example Input

```
Hi George,
```



### Example Output

```json
{
  "type": "service-email-insights",
  "skill": "service-email-insights",
  "name": "Intro",
  "value": "Hi George,",
  "span_text": "Hi George,",
  "span": [
    0,
    10
  ],
  "output_spans": [
    {
      "section": 0,
      "start": 0,
      "end": 10
    }
  ]
}
```
---
title: "Timing & Process Label"
slug: "timing-process-label"
hidden: false
createdAt: "2022-08-24T09:31:26.123Z"
updatedAt: "2022-08-24T09:38:02.031Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  Alex:<br/>\nHey Justin, We'd love to host a Zoom game for your team. Happy to expedite everything for your event on Monday. How many participants and what time are you looking at?<span class=\"label_box\">TIMING & PROCESS</span><span class=\"label_text\"> Let me know if you'd prefer to hop on a quick videochat tomorrow to go over all the logistics.</span>\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 235px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
Alex:
Hey Justin, We'd love to host a Zoom game for your team. Happy to expedite everything for your event on Monday. How many participants and what time are you looking at? Let me know if you'd prefer to hop on a quick videochat tomorrow to go over all the logistics.
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "{\n   \"type\":\"sales-insights\",\n   \"skill\":\"sales-insights\",\n   \"name\":\"Timing & Process\",\n   \"value\":\"Let me know if you'd prefer to hop on a quick videochat tomorrow to go over all the logistics.\",\n   \"speaker\":\"Alex\",\n   \"span_text\":\"Let me know if you'd prefer to hop on a quick videochat tomorrow to go over all the logistics.\",\n   \"span\":[\n      174,\n      268\n   ],\n   \"output_spans\":[\n      {\n         \"section\":0,\n         \"start\":168,\n         \"end\":262\n      }\n   ]\n}",
      "language": "json"
    }
  ]
}
[/block]
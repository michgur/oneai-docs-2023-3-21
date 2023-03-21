---
title: "Person Label"
slug: "person-label"
excerpt: "People, including fictional characters."
hidden: false
createdAt: "2022-08-24T06:41:46.040Z"
updatedAt: "2022-08-24T06:43:58.411Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  Hey <span class=\"label_box\">PERSON</span><span class=\"label_text\"> Francis</span>, my name is <span class=\"label_box\">PERSON</span><span class=\"label_text\"> Garrett</span>, happy to meet you\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 120px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
Hey Francis, my name is Garrett, happy to meet you
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "[\n   {\n      \"type\":\"name\",\n      \"skill\":\"names\",\n      \"name\":\"PERSON\",\n      \"value\":\"Francis\",\n      \"data\":{\n         \n      },\n      \"span_text\":\"Francis\",\n      \"span\":[\n         4,\n         11\n      ],\n      \"output_spans\":[\n         {\n            \"section\":0,\n            \"start\":4,\n            \"end\":11\n         }\n      ]\n   },\n   {\n      \"type\":\"name\",\n      \"skill\":\"names\",\n      \"name\":\"PERSON\",\n      \"value\":\"Garrett\",\n      \"data\":{\n         \n      },\n      \"span_text\":\"Garrett\",\n      \"span\":[\n         24,\n         31\n      ],\n      \"output_spans\":[\n         {\n            \"section\":0,\n            \"start\":24,\n            \"end\":31\n         }\n      ]\n   }\n]",
      "language": "json",
      "name": "JSON"
    }
  ]
}
[/block]
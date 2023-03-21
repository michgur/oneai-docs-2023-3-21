---
title: "Art Label"
slug: "art-label"
excerpt: "Titles of books, movies, songs, etc."
hidden: false
createdAt: "2022-08-24T07:00:09.262Z"
updatedAt: "2022-08-24T08:44:21.292Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  I just saw the <span class=\"label_box\">ART</span><span class=\"label_text\"> Mona Lisa</span> first hand!\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 120px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]
### Example Input

```
I just saw the Mona Lisa first hand!
```

### Example Output
[block:code]
{
  "codes": [
    {
      "code": "{\n   \"type\":\"name\",\n   \"skill\":\"names\",\n   \"name\":\"ART\",\n   \"value\":\"Mona Lisa\",\n   \"data\":{\n      \n   },\n   \"span_text\":\"the Mona Lisa\",\n   \"span\":[\n      16,\n      29\n   ],\n   \"output_spans\":[\n      {\n         \"section\":0,\n         \"start\":16,\n         \"end\":29\n      }\n   ]\n}",
      "language": "json"
    }
  ]
}
[/block]
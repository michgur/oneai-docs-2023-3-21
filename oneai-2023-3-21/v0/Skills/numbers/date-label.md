---
title: "Date Label"
slug: "date-label"
excerpt: "Absolute or relative dates or periods."
hidden: false
createdAt: "2022-08-24T07:19:04.709Z"
updatedAt: "2022-12-25T13:50:04.637Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  I bought this land <span class=\"label_box\">DATE\n  <div class=\"tooltip\">{<br> \n    &nbsp;&nbsp;&nbsp;\"date_time\": \"2012-08-17T00:00\",<br> \n    &nbsp;&nbsp;&nbsp;\"timezone\": \"US/Eastern\",<br>\n    &nbsp;&nbsp;&nbsp;\"precision\": \"DAY\"<br> \n    }</div>\n  </span><span class=\"label_text\"> ten years ago</span>\n  <br>&nbsp;\n  <br>&nbsp;\n  <br>&nbsp;\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 255px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n    border-radius: 3px;\n    padding: 5px 8px;\n  }\n  .tooltip::after {\n  content: \" \";\n  position: absolute;\n  bottom: 100%;  /* At the top of the tooltip */\n  left: 5%;\n  margin-left: -8px;\n  border-width: 8px;\n  border-style: solid;\n  border-color: transparent transparent black transparent;\n}\n</style>"
}
[/block]



### Example Input

```
I bought this land ten years ago
```



### Example Output

```json
{
   "type":"number",
   "skill":"numbers",
   "name":"DATE",
   "value":"2012-08-24",
   "data":{
      "date_time":"2012-08-24T00:00",
      "timezone":null,
      "precision":"DAY"
   },
   "span_text":"ten years ago",
   "span":[
      19,
      32
   ],
   "output_spans":[
      {
         "section":0,
         "start":19,
         "end":32
      }
   ]
}
```



### Additional Data

| Name        | Description                                                         | Example          |
| :---------- | :------------------------------------------------------------------ | :--------------- |
| `value`     | Human readable output according to the precision level              | 2012-08-17 10:00 |
| `date_time` | Machine-readable full date-time string in `yyyy-mm-ddTHH:MM` format | 2012-08-17T10:00 |
| `timezone`  | The indicated timezone, `null` if not present                       | US/Pacific       |
| `precision` | The date/time precision is indicated. One of YEAR, MONTH, DAY, TIME | DAY              |
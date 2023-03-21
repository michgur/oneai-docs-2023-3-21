---
title: "Duration Label"
slug: "duration-label"
excerpt: "Periods of time"
hidden: false
createdAt: "2022-08-24T07:32:19.090Z"
updatedAt: "2022-12-25T13:49:52.423Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n  it's going to take <span class=\"label_box\">DURATION\n  <div class=\"tooltip\">{<br> \n    &nbsp;&nbsp;&nbsp;\"days\": 2,<br> \n    &nbsp;&nbsp;&nbsp;\"days_in_seconds\": 172800,<br>\n    &nbsp;&nbsp;&nbsp;\"months\": 0<br> \n    &nbsp;&nbsp;&nbsp;\"years\": 0<br/>\n    }</div>\n  </span><span class=\"label_text\"> two days</span> to complete.\t\n  <br>&nbsp;<br>&nbsp;\n  <br>&nbsp;\n  <br>&nbsp;\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 235px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  border-radius: 3px;\n    padding: 5px 8px;\n  }\n  .tooltip::after {\n  content: \" \";\n  position: absolute;\n  bottom: 100%;  /* At the top of the tooltip */\n  left: 5%;\n  margin-left: -8px;\n  border-width: 8px;\n  border-style: solid;\n  border-color: transparent transparent black transparent;\n}\n</style>"
}
[/block]



### Example Input

```
it's going to take two days to complete.	
```



### Example Output

```json
{
   "type":"number",
   "skill":"numbers",
   "name":"DURATION",
   "value":"2 Days",
   "data":{
      "days":2,
      "days_in_seconds":172800,
      "months":0,
      "years":0
   },
   "span_text":"two days",
   "span":[
      19,
      27
   ],
   "output_spans":[
      {
         "section":0,
         "start":19,
         "end":27
      }
   ]
}
```



### Additional Data

| Name              | Description                                                        | Example |
| :---------------- | :----------------------------------------------------------------- | :------ |
| `days`            | Days component of the duration, expressed in fractional days value | 2.5     |
| `days_in_seconds` | Duration expressed in whole seconds (e.g 3600 = 1 hour)            | 216000  |
| `months`          | Months component of the duration                                   | 1       |
| `years`           | Years component of the duration                                    | 0       |
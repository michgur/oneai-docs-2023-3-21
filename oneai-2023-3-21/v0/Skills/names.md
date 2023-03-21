---
title: "Names"
slug: "names"
excerpt: "Finds **spans** in the text with names, and **identifies** the name type (person, organization, location etc.)."
hidden: false
createdAt: "2022-08-17T12:27:58.729Z"
updatedAt: "2023-01-06T14:17:02.426Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n<span class=\"label_box\">PERSON</span><span class=\"label_text\"> Michael Jordan</span> \n  played most of his career in\n  <span class=\"label_box\">GEO <div class=\"tooltip\">{\n    <br>&nbsp;&nbsp;\"value\":\"New York City\",<br/>&nbsp;&nbsp;\"type\":\"CITY\"<br/>}</div>\n  </span><span class=\"label_text\"> NYC</span>.\n  <br/>&nbsp;\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(241, 59, 233);\n    color: white;\n    padding: 2px;\n    position: relative;\n    outline-style: none;\">\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 200px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  border-radius: 3px;\n    padding: 5px 8px;\n  }\n  .tooltip::after {\n  content: \" \";\n  position: absolute;\n  bottom: 100%;  /* At the top of the tooltip */\n  left: 5%;\n  margin-left: -8px;\n  border-width: 8px;\n  border-style: solid;\n  border-color: transparent transparent black transparent;\n}\n</style>"
}
[/block]



> 📘 Use Names Skill to extract names from:
> 
> - [Articles](https://studio.oneai.com/?pipeline=80wq6L)
> - [Conversations](https://studio.oneai.com/?pipeline=MF6bTh)

> 👍 Benchmarks
> 
> Coming soon...

## Output labels

Identities:

- [ORG](doc:org-label) - Companies, agencies, institutions, etc.
- [PERSON](doc:person-label) - People, real or fictional characters
- [PRODUCT](doc:product-label) - Products and services

Places:

- [GEO](doc:geo-label) - Countries and States
- [LOCATION](doc:location-label) - Cities, buildings, airports, highways, bridges
- [EVENT](doc:event-label) - Sports events, Named hurricanes, wars, etc.

Others:

- [ART](doc:art-label) - Titles of books, movies, songs, etc.
- [LANGUAGE](doc:language-label) - Language names.
- [LAW](doc:law-label) - Named documents made into laws.

## Parameters

| Name          | Type    | Description                                 | Default |
| :------------ | :------ | :------------------------------------------ | :------ |
| `enrichment`  | boolean | Whether to enrich each label with metadata  | `true`  |

## Example

#### Request

```curl
curl -X POST \
'https://api.oneai.com/api/v0/pipeline' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-H 'api-key: <YOUR-API-KEY-HERE>' \
-d '{
    "input": "My name is Shawn, I live in Chicago in the state of Illinois but I don't speak Portuguese.",
    "steps": [
      {
        "skill": "names"
      }   
    ]
}'
```
```javascript Node.js
const { OneAI } = require("oneai");
const oneai = new OneAI("<YOUR-API-KEY-HERE>");
const text = "My name is Shawn, I live in Chicago in the state of Illinois but I don't speak Portuguese.";
const pipeline = new oneai.Pipeline(
	oneai.skills.names(),
);

pipeline.run(text).then(console.log);
```
```python
import oneai

oneai.api_key = "<YOUR-API-KEY-HERE>"
text = "My name is Shawn, I live in Chicago in the state of Illinois but I don't speak Portuguese."
pipeline = oneai.Pipeline(
  steps = [
		oneai.skills.Names(),
  ]
)

output = pipeline.run(text)
```



#### Response

```json API Response
{
  "input_text": "My name is Shawn, I live in Chicago in the state of Illinois but I don't speak Portuguese.",
  "status": "success",
  "output": [
    {
      "text_generated_by_step_name": "input",
      "text_generated_by_step_id": 0,
      "text": "My name is Shawn, I live in Chicago in the state of Illinois but I don't speak Portuguese.",
      "labels": [
        {
          "type": "name",
          "skill": "names",
          "name": "PERSON",
          "value": "Shawn",
          "data": {},
          "span_text": "Shawn",
          "span": [
            11,
            16
          ],
          "output_spans": [
            {
              "section": 0,
              "start": 11,
              "end": 16
            }
          ]
        },
        {
          "type": "name",
          "skill": "names",
          "name": "LOCATION",
          "value": "Chicago",
          "data": {
            "type": "CITY"
          },
          "span_text": "Chicago",
          "span": [
            28,
            35
          ],
          "output_spans": [
            {
              "section": 0,
              "start": 28,
              "end": 35
            }
          ]
        },
        {
          "type": "name",
          "skill": "names",
          "name": "GEO",
          "value": "Illinois",
          "data": {
            "type": "STATE",
            "country": "UNITED STATES"
          },
          "span_text": "Illinois",
          "span": [
            52,
            60
          ],
          "output_spans": [
            {
              "section": 0,
              "start": 52,
              "end": 60
            }
          ]
        },
        {
          "type": "name",
          "skill": "names",
          "name": "LANGUAGE",
          "value": "Portuguese language",
          "data": {},
          "span_text": "Portuguese",
          "span": [
            79,
            89
          ],
          "output_spans": [
            {
              "section": 0,
              "start": 79,
              "end": 89
            }
          ]
        }
      ]
    }
  ],
  "stats": {
    "concurrency_wait_time": 0,
    "total_running_jobs": 1,
    "total_waiting_jobs": 0
  }
}
```
```json SDKs Response
{
  text: "My name is Shawn, I live in Chicago in the state of Illinois but I don't speak Portuguese.",
  names: [
    {
      type: 'name',
      skill: 'names',
      name: 'PERSON',
      value: 'Shawn',
      data: {},
      span_text: 'Shawn',
      span: [ 11, 16 ],
      output_spans: [ { section: 0, start: 11, end: 16 } ]
    },
    {
      type: 'name',
      skill: 'names',
      name: 'LOCATION',
      value: 'Chicago',
      data: { type: 'CITY' },
      span_text: 'Chicago',
      span: [ 28, 35 ],
      output_spans: [ { section: 0, start: 28, end: 35 } ]
    },
    {
      type: 'name',
      skill: 'names',
      name: 'GEO',
      value: 'Illinois',
      data: { type: 'STATE', country: 'UNITED STATES' },
      span_text: 'Illinois',
      span: [ 52, 60 ],
      output_spans: [ { section: 0, start: 52, end: 60 } ]
    },
    {
      type: 'name',
      skill: 'names',
      name: 'LANGUAGE',
      value: 'Portuguese language',
      data: {},
      span_text: 'Portuguese',
      span: [ 79, 89 ],
      output_spans: [ { section: 0, start: 79, end: 89 } ]
    }
  ]
}
```
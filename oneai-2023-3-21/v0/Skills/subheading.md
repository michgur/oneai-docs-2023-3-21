---
title: "Subheading"
slug: "subheading"
excerpt: "**Generates** an appropriate subheading for the input text."
hidden: false
createdAt: "2022-09-07T08:15:37.962Z"
updatedAt: "2022-12-28T13:26:42.051Z"
---
[block:html]
{
  "html": "<div class=\"example_box\">\n    <span class=\"label_box\">Introduction</span>\n   <br/>\n\tNatural language processing (NLP) is a subfield of linguistics, computer science, and artificial intelligence concerned with the interactions between computers and human language, in particular how to program computers to process and analyze large amounts of natural language data. The goal is a computer capable of \"understanding\" the contents of documents, including the contextual nuances of the language within them.\n   <br/><span class=\"label_box\">The Technology</span>\n   <br/>\n  The technology can then accurately extract information and insights contained in the documents as well as categorize and organize the documents themselves. Challenges in natural language processing frequently involve speech recognition, natural language understanding, and natural language generation.\n</div>\n\n<style>\n  .label_box { \n    box-sizing: border-box;\n    border-width: 0px;\n    border-style: solid;\n    border-bottom-left-radius: 0.25rem;\n    border-top-left-radius: 0.25rem;\n    border-top-right-radius: 0.25rem;\n    background-color: rgb(255, 232, 1);\n    padding: 2px;\n    outline-style: none;\n    color:black>\n  }\n  .label_text {\n    box-sizing: border-box;\n    border-width: 0px 0px 2px;\n    border-style: solid;\n    border-color: rgb(241, 59, 233);\n\t}\n  .example_box {\n    max-width: 40rem;\n    margin: 0 auto;\n    background-color: rgb(243, 245, 249);\n    padding: 18px;\n    line-height: 28px;\n  }\n  .tooltip {\n    color:white;\n    background-color: black;\n    width: 120px;\n    position: absolute;\n        top: 26px;\n        left: 15px;\n  }\n</style>"
}
[/block]



> 📘 Use Subheading Skill to generate subheadings for:
> 
> - Article segments
> - Blog post sections
> - Video segments

> 🚦 [Benchmarks](https://docs.oneai.com/docs/subheadline-benchmarks)
> 
> | [Grade](https://docs.oneai.com/docs/rouge-metrics-for-summary-headline) | [Rouge1](https://docs.oneai.com/docs/rouge-metrics-for-summary-headline) | [RougeL](https://docs.oneai.com/docs/rouge-metrics-for-summary-headline) |                                                                      |
> | :---------------------------------------------------------------------- | :----------------------------------------------------------------------- | :----------------------------------------------------------------------- | :------------------------------------------------------------------- |
> | 🟢A                                                                     | 46.9                                                                     | 46.4                                                                     | [read benchmark](https://docs.oneai.com/docs/subheadline-benchmarks) |

## Parameters

[block:parameters]
{
  "data": {
    "h-0": "Param",
    "h-1": "",
    "h-2": "",
    "0-0": "previous_heading",
    "0-1": "pass the headline of the article or the previous sub-heading.  \nProviding context will improve the quality and consistency of your results.",
    "0-2": "For example, if creating a subheading to a section in text after the previous one had the heading \"introduction\", the next one will be called with:  \n**\"previous_heading\":\"introduction\"**"
  },
  "cols": 3,
  "rows": 1,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]

## Output labels

| Type       | Value                     |
| :--------- | :------------------------ |
| subheading | The generated subheading. |

## Example

### Request

```curl
curl -X POST \
'https://api.oneai.com/api/v0/pipeline' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-H 'api-key: <YOUR-API-KEY-HERE>' \
-d '{
    "input": "Natural language processing (NLP) is a subfield of linguistics, computer science, and artificial intelligence concerned with the interactions between computers and human language, in particular how to program computers to process and analyze large amounts of natural language data. The goal is a computer capable of "understanding" the contents of documents, including the contextual nuances of the language within them. The technology can then accurately extract information and insights contained in the documents as well as categorize and organize the documents themselves. Challenges in natural language processing frequently involve speech recognition, natural language understanding, and natural language generation. Based on long-standing trends in the field, it is possible to extrapolate future directions of NLP. As of 2020, three trends among the topics of the long-standing series of CoNLL Shared Tasks can be observed: Interest on increasingly abstract, \"cognitive\" aspects of natural language, Increasing interest in multilinguality and Elimination of symbolic representations.",
    "input_type": "article",
    "content_type": "application/json",
    "steps": [
      {
        "skill": "subheading"
      }   
    ]
}'
```
```javascript Node.js
const { OneAI } = require("oneai");

const oneai = new OneAI("<YOUR-API-KEY-HERE>");
const text = "Natural language processing (NLP) is a subfield of linguistics, computer science, and artificial intelligence concerned with the interactions between computers and human language, in particular how to program computers to process and analyze large amounts of natural language data. The goal is a computer capable of "understanding" the contents of documents, including the contextual nuances of the language within them. The technology can then accurately extract information and insights contained in the documents as well as categorize and organize the documents themselves. Challenges in natural language processing frequently involve speech recognition, natural language understanding, and natural language generation. Based on long-standing trends in the field, it is possible to extrapolate future directions of NLP. As of 2020, three trends among the topics of the long-standing series of CoNLL Shared Tasks can be observed: Interest on increasingly abstract, "cognitive" aspects of natural language, Increasing interest in multilinguality and Elimination of symbolic representations.";
const pipeline = new oneai.Pipeline(
	oneai.skills.subheading(),
);


pipeline.run(text).then(console.log);
```
```Text Python
import oneai

oneai.api_key = "<YOUR-API-KEY-HERE>"
text = "Natural language processing (NLP) is a subfield of linguistics, computer science, and artificial intelligence concerned with the interactions between computers and human language, in particular how to program computers to process and analyze large amounts of natural language data. The goal is a computer capable of "understanding" the contents of documents, including the contextual nuances of the language within them. The technology can then accurately extract information and insights contained in the documents as well as categorize and organize the documents themselves. Challenges in natural language processing frequently involve speech recognition, natural language understanding, and natural language generation. Based on long-standing trends in the field, it is possible to extrapolate future directions of NLP. As of 2020, three trends among the topics of the long-standing series of CoNLL Shared Tasks can be observed: Interest on increasingly abstract, "cognitive" aspects of natural language, Increasing interest in multilinguality and Elimination of symbolic representations."
pipeline = oneai.Pipeline(
  steps = [
		oneai.skills.Subheading(),
  ]
)


output = pipeline.run(text)
```



### Response

```json JSON Response
{
   "input_text":"Natural language processing (NLP) is a subfield of linguistics, computer science, and artificial intelligence concerned with the interactions between computers and human language, in particular how to program computers to process and analyze large amounts of natural language data. The goal is a computer capable of \"understanding\" the contents of documents, including the contextual nuances of the language within them. The technology can then accurately extract information and insights contained in the documents as well as categorize and organize the documents themselves. Challenges in natural language processing frequently involve speech recognition, natural language understanding, and natural language generation. Based on long-standing trends in the field, it is possible to extrapolate future directions of NLP. As of 2020, three trends among the topics of the long-standing series of CoNLL Shared Tasks can be observed: Interest on increasingly abstract, \"cognitive\" aspects of natural language, Increasing interest in multilinguality and Elimination of symbolic representations.",
   "status":"success",
   "output":[
      {
         "text_generated_by_step_name":"input",
         "text_generated_by_step_id":0,
         "text":"Natural language processing (NLP) is a subfield of linguistics, computer science, and artificial intelligence concerned with the interactions between computers and human language, in particular how to program computers to process and analyze large amounts of natural language data. The goal is a computer capable of \"understanding\" the contents of documents, including the contextual nuances of the language within them. The technology can then accurately extract information and insights contained in the documents as well as categorize and organize the documents themselves. Challenges in natural language processing frequently involve speech recognition, natural language understanding, and natural language generation. Based on long-standing trends in the field, it is possible to extrapolate future directions of NLP. As of 2020, three trends among the topics of the long-standing series of CoNLL Shared Tasks can be observed: Interest on increasingly abstract, \"cognitive\" aspects of natural language, Increasing interest in multilinguality and Elimination of symbolic representations.",
         "labels":[
            {
               "type":"subheading",
               "skill":"subheading",
               "name":"subheading",
               "value":"What is Natural Language Processing?"
            }
         ]
      }
   ],
   "stats":{
      "concurrency_wait_time":0.0,
      "total_running_jobs":1,
      "total_waiting_jobs":0
   }
}
```
```Text SDKs Response
// Coming soon...
```
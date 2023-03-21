---
title: "Languages"
slug: "pdf-skill-give-a-name"
excerpt: "OneAi has the capability to work and process text in many languages, automatically"
hidden: true
createdAt: "2022-12-29T15:45:49.509Z"
updatedAt: "2023-01-05T09:19:51.969Z"
---
Our APIs are capable of processing content in many languages, including (see list at <https://oneai.com/languages>)

To enable language detection, set the`multilingual=true` in the request (add example)

you don't have to specify input language, our AI detects it automatically and processes it

To analyze audio, use the whisper model. Look <https://docs.oneai.com/docs/transcribe-audio>

#### Request

```curl
curl -X POST \
'https://api.oneai.com/api/v0/pipeline' \
-H 'accept: application/json' \
-H 'Content-Type: application/json' \
-H 'api-key: <YOUR-API-KEY-HERE>' \
-d '{
    "input": "Después de prohibir de forma permanente las fiestas y eventos en todos los listados de Airbnb en junio, la compañía está endureciendo su postura contra las fiestas al lanzar nuevas herramientas de detección en los EE. UU. y Canadá.",
    "steps": [
      {
        "skill": "article-topics"
      },   
      "multilingual": true
    ]
}'


```
```javascript Node.js
const { OneAI } = require("oneai");

const oneai = new OneAI("<YOUR_API_KEY>", {
    multilingual: true
});
const text = "Después de prohibir de forma permanente las fiestas y eventos en todos los listados de Airbnb en junio, la compañía está endureciendo su postura contra las fiestas al lanzar nuevas herramientas de detección en los EE. UU. y Canadá.";
const pipeline = new oneai.Pipeline(
	oneai.skills.topics(),
);

pipeline.run(text).then(console.log);
```
```python
import oneai

oneai.api_key = "<YOUR-API-KEY-HERE>"
oneai.multilingual = True
text = "Después de prohibir de forma permanente las fiestas y eventos en todos los listados de Airbnb en junio, la compañía está endureciendo su postura contra las fiestas al lanzar nuevas herramientas de detección en los EE. UU. y Canadá."
pipeline = oneai.Pipeline(
  steps = [
		oneai.skills.Topics(),
  ]
)

output = pipeline.run(text)
```
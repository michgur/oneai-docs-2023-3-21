---
title: "Asynchronous Pipelines"
slug: "asynchronous-pipelines"
excerpt: "The Pipeline API has two methods of invocation: synchronous, and asynchronous."
hidden: false
createdAt: "2022-08-24T08:37:30.864Z"
updatedAt: "2023-01-09T23:26:22.891Z"
---
When the content you wish to process is either located online and requires download, or if it's in a source format that requires text conversion, like an audio file that requires transcription, or a PDF document that requires OCR, then invoking an asynchronous pipeline is the better choice. If you invoke a sync pipeline, you will have to wait for the response for as much time as it takes to process.
[block:code]
{
  "codes": [
    {
      "code": "curl -X POST \\\n'https://api.oneai.com/api/v0/pipeline/async' \\\n-H 'accept: application/json' \\\n-H 'Content-Type: application/json' \\\n-H 'api-key: <YOUR-API-KEY-HERE>' \\\n-d '{\n    \"input\": \"<URL-TO-AUDIO-FILE>\",\n    \"input_type\": \"conversation\",\n\t\t\"content_type\": \"audio/wav\",\n    \"steps\": [\n      {\n        \"skill\": \"transcribe\",\n        \"params\": {\n          \"speaker_detection\": true\n        }\n      },\n      {\n        \"skill\": \"summarize\"\n      }  \n    ]\n}'",
      "language": "curl"
    }
  ]
}
[/block]
The response for an async Pipeline invocation will contain a task ID:
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"status\":\"QUEUED\",\n  \"task_id\":\"075f954c-e1d7-4b80-b24d-e460fd266c2c\"\n}",
      "language": "json"
    }
  ]
}
[/block]
Now you can poll `/async/tasks/075f954c-e1d7-4b80-b24d-e460fd266c2`. Expect the status to be RUNNING as long as the job is still running. You can stop polling once the status changes to either COMPLETED or FAILED. If the status is COMPLETED, you can find the pipeline result in the `result` field, if it is FAILED, you can find the error in the `error` field.
[block:code]
{
  "codes": [
    {
      "code": "curl -X 'GET' \\\n  'https://api.oneai.com/api/v0/pipeline/async/tasks/075f954c-e1d7-4b80-b24d-e460fd266c2c' \\\n  -H 'accept: application/json' \\\n  -H 'api-key: <YOUR-API-KEY-HERE>'\n",
      "language": "curl"
    }
  ]
}
[/block]
Once the status is `COMPLETED`, you can fetch the results of the Pipeline API from the `result` field.
[block:code]
{
  "codes": [
    {
      "code": "{\n   \"result\":{\n      \"input_text\":\"<THE-TEXT-EXTRACTED-FROM-THE-INPUT-FILE>\",\n      \"status\":\"success\",\n      \"error\":null,\n      \"output\":[\n         {\n            \"text_generated_by_step_name\":\"input\",\n            \"text_generated_by_step_id\":0,\n            \"text\":\"<THE-TEXT-EXTRACTED-FROM-THE-INPUT-FILE>\",\n            \"labels\":[\n               {\n                  \"type\":\"detect-language\",\n                  \"skill\":\"detect-language\",\n                  \"name\":\"language\",\n                  \"value\":\"Spanish\",\n                  \"speaker\":null,\n                  \"data\":null,\n                  \"span_text\":null,\n                  \"span\":null,\n                  \"output_spans\":null,\n                  \"origin\":null,\n                  \"input_spans\":null\n               }\n            ]\n         }\n      ],\n      \"stats\":{\n         \"concurrency_wait_time\":0.0,\n         \"total_running_jobs\":1,\n         \"total_waiting_jobs\":0\n      }\n   },\n   \"task_id\":\"075f954c-e1d7-4b80-b24d-e460fd266c2c\",\n   \"status\":\"COMPLETED\",\n   \"completion_time\":\"2022-08-21T09:15:39.040000\",\n   \"creation_time\":\"2022-08-21T09:15:39.007000\"\n}",
      "language": "json",
      "name": "JSON Response"
    }
  ]
}
[/block]
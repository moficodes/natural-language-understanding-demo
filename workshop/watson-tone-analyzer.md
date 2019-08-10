# Watson Tone Analyzer

Select Tone Analyzer from catalog &gt; AI

Give the service a name.

Select Lite

Create service

![](../.gitbook/assets/image%20%286%29.png)

Once the service is created select the manage tab on the left.

![](../.gitbook/assets/image%20%288%29.png)

We will need the API Key and the url in the next step.

You can clear the content of the file or just add it to the end of it.

```javascript
const ToneAnalyzerV3 = require("ibm-watson/tone-analyzer/v3");

const toneAnalyzer = new ToneAnalyzerV3({
  version: "2017-09-21",
  iam_apikey: "your-tone-api-key"
});
```

Don't forget to replace your api key from tone service.

Next set the tone params

```javascript
const text =
  "Team, I know that times are tough! Product " +
  "sales have been disappointing for the past three " +
  "quarters. We have a competitive product, but we " +
  "need to do a better job of selling it!";

const toneParams = {
  tone_input: { text: text },
  content_type: "application/json"
};
```

Finally get the response back and see the output.

```javascript
toneAnalyzer
  .tone(toneParams)
  .then(toneAnalysis => {
    console.log(JSON.stringify(toneAnalysis, null, 2));
  })
  .catch(err => {
    console.log("error:", err);
  });
```

If everything goes well, we should see the following output.

```javascript
{
  "document_tone": {
    "tones": [
      {
        "score": 0.6165,
        "tone_id": "sadness",
        "tone_name": "Sadness"
      },
      {
        "score": 0.829888,
        "tone_id": "analytical",
        "tone_name": "Analytical"
      }
    ]
  },
  "sentences_tone": [
    {
      "sentence_id": 0,
      "text": "Team, I know that times are tough!",
      "tones": [
        {
          "score": 0.801827,
          "tone_id": "analytical",
          "tone_name": "Analytical"
        }
      ]
    },
    {
      "sentence_id": 1,
      "text": "Product sales have been disappointing for the pastthree quarters.",
      "tones": [
        {
          "score": 0.771241,
          "tone_id": "sadness",
          "tone_name": "Sadness"
        },
        {
          "score": 0.687768,
          "tone_id": "analytical",
          "tone_name": "Analytical"
        }
      ]
    },
    {
      "sentence_id": 2,
      "text": "We have a competitive product, but we need to do abetter job of selling it!",
      "tones": [
        {
          "score": 0.506763,
          "tone_id": "analytical",
          "tone_name": "Analytical"
        }
      ]
    }
  ]
}
```


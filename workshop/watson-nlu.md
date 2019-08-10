# Watson NLU

* Give the service a name.
* Select Lite.
* Click Create.

![](../.gitbook/assets/screen-shot-2019-08-10-at-1.45.11-am.png)

* Once the service is created. From the mage tab we can find the URL and API Key.

![](../.gitbook/assets/image%20%282%29.png)

We will need that in the next stop.

In the next step we will use node one of many supported client libraries to use NLU to gather insight about some text.

In the `index.js` file add the following

```text
const NaturalLanguageUnderstandingV1 = require("ibm-watson/natural-language-understanding/v1");

const naturalLanguageUnderstanding = new NaturalLanguageUnderstandingV1({
  version: "2019-07-12",
  iam_apikey: "your-api-key",
  url: "https://gateway.watsonplatform.net/natural-language-understanding/api"
});
```


# Tone Analyzer

The IBM Watson™ Tone Analyzer service uses linguistic analysis to detect emotional and language tones in written text. The service can analyze tone at both the document and sentence levels. You can use the service to understand how your written communications are perceived and then to improve the tone of your communications. Businesses can use the service to learn the tone of their customers' communications and to respond appropriately to each customer, or to understand and improve their customer conversations in general.

You submit JSON, plain text, or HTML input that contains your written content to the service. The service accepts up to 128 KB of text, which is about 1000 sentences. The service returns JSON results that report the tone of your input. You can use these results to improve the perception and effectiveness of your communications, ensuring that your writing conveys the tone and style that you want for your intended audience. The following diagram shows the basic flow of calls to the service.

![](.gitbook/assets/image%20%282%29.png)

### Tone Analyzer endpoints

The service offers two endpoints:

* **General-purpose endpoint** \(`GET` or `POST /v3/tone`\)

  Use the Tone Analyzer general-purpose endpoint to analyze shorter web data, such as email messages or tweets, or longer documents, such as articles or blog posts. Monitor social media to understand what customers are saying about a brand and to determine whom to target with specific messaging. The endpoint accepts JSON, plain text, or HTML input. For more information about the method and the tones that it returns, see [Using the general-purpose endpoint](https://cloud.ibm.com/docs/services/tone-analyzer?topic=tone-analyzer-utgpe).

  The [general-purpose demo](https://tone-analyzer-demo.ng.bluemix.net/) submits content to the service for analysis. The service returns overall and sentence-level analyses of the tone of the content.

* **Customer-engagement endpoint** \(`POST /v3/tone_chat`\)

  Use the Tone Analyzer customer-engagement endpoint to monitor customer service and support conversations. Escalate customer conversations when they turn sour or find opportunities to improve customer service scripts, dialog strategies, and customer journeys. The endpoint accepts JSON input. For more information about the method and the tones that it returns, see [Using the customer-engagement endpoint](https://cloud.ibm.com/docs/services/tone-analyzer?topic=tone-analyzer-utco).

  The [customer-engagement demo](https://customer-engagement-demo.ng.bluemix.net/) analyzes conversations between customers and customer service agents. The service measures customer satisfaction and concerns, and assesses agent performance, so that you can gauge how the interaction evolves.

For more information about the pricing plans available for the service, see the Tone Analyzer service in the [IBM Cloud Catalog](https://cloud.ibm.com/catalog/services/tone-analyzer).

### Use cases

Some interesting use cases of the service are

* _Social listening and audience monitoring_ - Monitor social media to understand what customers are saying about your brand in real time. For example, you might determine that your customers in Chicago are sad after the Bulls lost or happy during the Taste of Chicago festival. \(General-purpose endpoint\)
* _Personalized marketing_ - Determine whom to target with personalized messaging and when. For example, a travel company might target happy consumers with "treat yourself" messaging, sad consumers with "escape" messaging, and angry consumers with "relax" messaging. \(General-purpose endpoint\)
* _Chat bots_ - Enable an automated agent to detect customer tones and craft suitable responses. For example, you might respond to sadness with "I'm sorry you are upset about this problem" or to satisfaction with "I'm glad you are satisfied with our service." \(Customer-engagement endpoint\)
* _Customer-engagement monitoring and quality assurance_ - Monitor the overall tone of agent and customer communications, detect anomalies, and highlight opportunities to train agents on how to better communicate. \(Customer-engagement endpoint\)

## [Demo](https://tone-analyzer-demo.ng.bluemix.net/)


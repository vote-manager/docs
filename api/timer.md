---
description: >-
  Welcome to the Prohooks API. Schedule webhook requests with custom payload &
  method!
---

# Timer API

{% hint style="info" %}
API Link: https://prohooks.votemanager.xyz
{% endhint %}

### API Methods

{% swagger method="post" path="/new" baseUrl="" summary="Create" %}
{% swagger-description %}
Create a new schedule
{% endswagger-description %}

{% swagger-parameter in="body" name="token" required="true" %}
API token
{% endswagger-parameter %}

{% swagger-parameter in="body" name="url" required="true" %}
Webhook URL to send request to when timer is up
{% endswagger-parameter %}

{% swagger-parameter in="body" name="method" required="true" %}
HTTPS method to use when sending webhook request
{% endswagger-parameter %}

{% swagger-parameter in="body" name="duration" required="true" %}
Duration of the timer
{% endswagger-parameter %}

{% swagger-parameter in="body" name="payload" type="Object" required="false" %}
Data to send in the webhook request
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    error: false,
    message: timer_id,
    scheduled: date
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/status" baseUrl="" summary="Status" %}
{% swagger-description %}
Get the status of a timer
{% endswagger-description %}

{% swagger-parameter in="body" name="key" required="true" %}
API key
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="id" %}
Timer ID
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    error: false,
    message: {
    id: 'sample_id',
    date: 'Wed, 29 Jun 2022 17:12:08 GMT',
    url: 'https://some-url.com',
    method: 'POST',
    payload: {
      some: payload_data
    },
    timeLeft: '1 minute'
  }
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/cancel" baseUrl="" summary="Cancel" %}
{% swagger-description %}
Cancel a timer
{% endswagger-description %}

{% swagger-parameter in="body" name="key" required="true" %}
API key
{% endswagger-parameter %}

{% swagger-parameter in="body" name="id" required="true" %}
ID of the timer to cancel
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    error: false,
    message: "cancelled"
}
```
{% endswagger-response %}
{% endswagger %}

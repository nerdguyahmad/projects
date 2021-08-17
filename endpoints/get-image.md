---
description: Get Information about COVID-19 Cases of the whole world or a specific country
---

# GET /covid

{% api-method method="get" host="https://api.pgamerx.com" path="/v5/covid" %}
{% api-method-summary %}
Covid Data
{% endapi-method-summary %}

{% api-method-description %}
Get Information about COVID-19 using this endpoint
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
API key which you can get from api.pgamerx.com/register
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="country" type="string" required=false %}
Country. Can be left behind so as to get info about the world as a collective group
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Done! Success
{% endapi-method-response-example-description %}

```
{
  "country": {
    "name": "\n  India ",
    "flagImg": "https://www.worldometers.info/img/flags/small/tn_in-flag.gif"
  },
  "cases": {
    "total": "32,239,249 ",
    "recovered": "31,424,473",
    "deaths": "431,900"
  },
  "closedCases": {
    "total": "31,856,373",
    "percentage": {
      "death": "1",
      "discharge": "99"
    }
  }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Some error occurred
{% endapi-method-response-example-description %}

```
Some Internal Error Occured/You are sending an invalid country name
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Your API key is missing
{% endapi-method-response-example-description %}

```
API Key is missing! Kindly get one at api.pgamerx.com/register
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Your api key is incorrect
{% endapi-method-response-example-description %}

```
Forbidden! API Key is incorrect, kindly recheck
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



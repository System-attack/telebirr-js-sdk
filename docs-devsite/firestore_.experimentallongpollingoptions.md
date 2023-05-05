Project: /docs/reference/js/_project.yaml
Book: /docs/reference/_book.yaml
page_type: reference

{% comment %}
DO NOT EDIT THIS FILE!
This is generated by the JS SDK team, and any local changes will be
overwritten. Changes should be made in the source code at
https://github.com/firebase/firebase-js-sdk
{% endcomment %}

# ExperimentalLongPollingOptions interface
Options that configure the SDK’s underlying network transport (WebChannel) when long-polling is used.

Note: This interface is "experimental" and is subject to change.

See `FirestoreSettings.experimentalAutoDetectLongPolling`<!-- -->, `FirestoreSettings.experimentalForceLongPolling`<!-- -->, and `FirestoreSettings.experimentalLongPollingOptions`<!-- -->.

<b>Signature:</b>

```typescript
export declare interface ExperimentalLongPollingOptions 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [timeoutSeconds](./firestore_.experimentallongpollingoptions.md#experimentallongpollingoptionstimeoutseconds) | number | The desired maximum timeout interval, in seconds, to complete a long-polling GET response. Valid values are between 5 and 30, inclusive. Floating point values are allowed and will be rounded to the nearest millisecond.<!-- -->By default, when long-polling is used the "hanging GET" request sent by the client times out after 30 seconds. To request a different timeout from the server, set this setting with the desired timeout.<!-- -->Changing the default timeout may be useful, for example, if the buffering proxy that necessitated enabling long-polling in the first place has a shorter timeout for hanging GET requests, in which case setting the long-polling timeout to a shorter value, such as 25 seconds, may fix prematurely-closed hanging GET requests. For example, see https://github.com/firebase/firebase-js-sdk/issues/6987. |

## ExperimentalLongPollingOptions.timeoutSeconds

The desired maximum timeout interval, in seconds, to complete a long-polling GET response. Valid values are between 5 and 30, inclusive. Floating point values are allowed and will be rounded to the nearest millisecond.

By default, when long-polling is used the "hanging GET" request sent by the client times out after 30 seconds. To request a different timeout from the server, set this setting with the desired timeout.

Changing the default timeout may be useful, for example, if the buffering proxy that necessitated enabling long-polling in the first place has a shorter timeout for hanging GET requests, in which case setting the long-polling timeout to a shorter value, such as 25 seconds, may fix prematurely-closed hanging GET requests. For example, see https://github.com/firebase/firebase-js-sdk/issues/6987.

<b>Signature:</b>

```typescript
timeoutSeconds?: number;
```
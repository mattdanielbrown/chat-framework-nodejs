[Google Chat SDK](../README.md) / [@google/chat-sdk](../modules/google_chat_sdk.md) / [chat\_v1](../modules/google_chat_sdk.chat_v1.md) / Resource$Rooms$Conversations

# Class: Resource$Rooms$Conversations

[@google/chat-sdk](../modules/google_chat_sdk.md).[chat_v1](../modules/google_chat_sdk.chat_v1.md).Resource$Rooms$Conversations

## Table of contents

### Constructors

- [constructor](google_chat_sdk.chat_v1.Resource_Rooms_Conversations.md#constructor)

### Properties

- [context](google_chat_sdk.chat_v1.Resource_Rooms_Conversations.md#context)

### Methods

- [messages](google_chat_sdk.chat_v1.Resource_Rooms_Conversations.md#messages)

## Constructors

### constructor

• **new Resource$Rooms$Conversations**(`context`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `context` | `APIRequestContext` |

#### Defined in

node_modules/@googleapis/chat/build/v1.d.ts:2014

## Properties

### context

• **context**: `APIRequestContext`

#### Defined in

node_modules/@googleapis/chat/build/v1.d.ts:2013

## Methods

### messages

▸ **messages**(`params`, `options`): `GaxiosPromise`<`Readable`\>

Legacy path for creating message. Calling these will result in a BadRequest response.

**`example`**
```js
// Before running the sample:
// - Enable the API at:
//   https://console.developers.google.com/apis/api/chat.googleapis.com
// - Login into gcloud by running:
//   `$ gcloud auth application-default login`
// - Install the npm module by running:
//   `$ npm install googleapis`

const {google} = require('googleapis');
const chat = google.chat('v1');

async function main() {
  const auth = new google.auth.GoogleAuth({
    // Scopes can be specified either as an array or as a single, space-delimited string.
    scopes: [],
  });

  // Acquire an auth client, and bind it to all future calls
  const authClient = await auth.getClient();
  google.options({auth: authClient});

  // Do the magic
  const res = await chat.rooms.conversations.messages({
    // Required. Space resource name, in the form "spaces/x". Example: spaces/AAAAMpdlehY
    parent: 'rooms/my-room/conversations/my-conversation',
    // Optional. Opaque thread identifier string that can be specified to group messages into a single thread. If this is the first message with a given thread identifier, a new thread is created. Subsequent messages with the same thread identifier will be posted into the same thread. This relieves bots and webhooks from having to store the Google Chat thread ID of a thread (created earlier by them) to post further updates to it. Has no effect if thread field, corresponding to an existing thread, is set in message.
    threadKey: 'placeholder-value',

    // Request body metadata
    requestBody: {
      // request body parameters
      // {
      //   "actionResponse": {},
      //   "annotations": [],
      //   "argumentText": "my_argumentText",
      //   "attachment": [],
      //   "cards": [],
      //   "createTime": "my_createTime",
      //   "fallbackText": "my_fallbackText",
      //   "lastUpdateTime": "my_lastUpdateTime",
      //   "name": "my_name",
      //   "previewText": "my_previewText",
      //   "sender": {},
      //   "slashCommand": {},
      //   "space": {},
      //   "text": "my_text",
      //   "thread": {}
      // }
    },
  });
  console.log(res.data);

  // Example response
  // {
  //   "actionResponse": {},
  //   "annotations": [],
  //   "argumentText": "my_argumentText",
  //   "attachment": [],
  //   "cards": [],
  //   "createTime": "my_createTime",
  //   "fallbackText": "my_fallbackText",
  //   "lastUpdateTime": "my_lastUpdateTime",
  //   "name": "my_name",
  //   "previewText": "my_previewText",
  //   "sender": {},
  //   "slashCommand": {},
  //   "space": {},
  //   "text": "my_text",
  //   "thread": {}
  // }
}

main().catch(e => {
  console.error(e);
  throw e;
});

```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `params` | [`Params$Resource$Rooms$Conversations$Messages`](../interfaces/google_chat_sdk.chat_v1.Params_Resource_Rooms_Conversations_Messages.md) | Parameters for request |
| `options` | `StreamMethodOptions` | Optionally override request options, such as `url`, `method`, and `encoding`. |

#### Returns

`GaxiosPromise`<`Readable`\>

A promise if used with async/await, or void if used with a callback.

#### Defined in

node_modules/@googleapis/chat/build/v1.d.ts:2103

▸ **messages**(`params?`, `options?`): `GaxiosPromise`<[`Schema$Message`](../interfaces/google_chat_sdk.chat_v1.Schema_Message.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `params?` | [`Params$Resource$Rooms$Conversations$Messages`](../interfaces/google_chat_sdk.chat_v1.Params_Resource_Rooms_Conversations_Messages.md) |
| `options?` | `MethodOptions` |

#### Returns

`GaxiosPromise`<[`Schema$Message`](../interfaces/google_chat_sdk.chat_v1.Schema_Message.md)\>

#### Defined in

node_modules/@googleapis/chat/build/v1.d.ts:2104

▸ **messages**(`params`, `options`, `callback`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `params` | [`Params$Resource$Rooms$Conversations$Messages`](../interfaces/google_chat_sdk.chat_v1.Params_Resource_Rooms_Conversations_Messages.md) |
| `options` | `StreamMethodOptions` \| `BodyResponseCallback`<`Readable`\> |
| `callback` | `BodyResponseCallback`<`Readable`\> |

#### Returns

`void`

#### Defined in

node_modules/@googleapis/chat/build/v1.d.ts:2105

▸ **messages**(`params`, `options`, `callback`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `params` | [`Params$Resource$Rooms$Conversations$Messages`](../interfaces/google_chat_sdk.chat_v1.Params_Resource_Rooms_Conversations_Messages.md) |
| `options` | `MethodOptions` \| `BodyResponseCallback`<[`Schema$Message`](../interfaces/google_chat_sdk.chat_v1.Schema_Message.md)\> |
| `callback` | `BodyResponseCallback`<[`Schema$Message`](../interfaces/google_chat_sdk.chat_v1.Schema_Message.md)\> |

#### Returns

`void`

#### Defined in

node_modules/@googleapis/chat/build/v1.d.ts:2106

▸ **messages**(`params`, `callback`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `params` | [`Params$Resource$Rooms$Conversations$Messages`](../interfaces/google_chat_sdk.chat_v1.Params_Resource_Rooms_Conversations_Messages.md) |
| `callback` | `BodyResponseCallback`<[`Schema$Message`](../interfaces/google_chat_sdk.chat_v1.Schema_Message.md)\> |

#### Returns

`void`

#### Defined in

node_modules/@googleapis/chat/build/v1.d.ts:2107

▸ **messages**(`callback`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `callback` | `BodyResponseCallback`<[`Schema$Message`](../interfaces/google_chat_sdk.chat_v1.Schema_Message.md)\> |

#### Returns

`void`

#### Defined in

node_modules/@googleapis/chat/build/v1.d.ts:2108
---
title: messages
description: Contains list of messages
---
## Constructor: messages  
[Back to constructors index](index.md)



Contains list of messages

### Attributes:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|total\_count|[int](../types/int.md) | Yes|Approximate total count of found messages|
|messages|Array of [message](../constructors/message.md) | Yes|List of messages|



### Type: [Messages](../types/Messages.md)


### Example:

```
$messages = ['_' => 'messages', 'total_count' => int, 'messages' => [message]];
```  

[PWRTelegram](https://pwrtelegram.xyz) json-encoded version:

```
{"_": "messages", "total_count": int, "messages": [message]}
```


Or, if you're into Lua:  


```
messages={_='messages', total_count=int, messages={message}}

```



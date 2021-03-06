---
title: messages.getChats
description: messages.getChats parameters, return type and example
---
## Method: messages.getChats  
[Back to methods index](index.md)


### Parameters:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|id|Array of [InputChat](../types/InputChat.md) | Yes|


### Return type: [messages\_Chats](../types/messages_Chats.md)

### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
if (isset($token)) { // Login as a bot
    $MadelineProto->bot_login($token);
}
if (isset($number)) { // Login as a user
    $sentCode = $MadelineProto->phone_login($number);
    echo 'Enter the code you received: ';
    $code = '';
    for ($x = 0; $x < $sentCode['type']['length']; $x++) {
        $code .= fgetc(STDIN);
    }
    $MadelineProto->complete_phone_login($code);
}

$messages_Chats = $MadelineProto->messages->getChats(['id' => [InputChat], ]);
```

Or, if you're using the [PWRTelegram HTTP API](https://pwrtelegram.xyz):

### As a bot:

POST/GET to `https://api.pwrtelegram.xyz/botTOKEN/madeline`

Parameters:

* method - messages.getChats
* params - `{"id": [InputChat], }`



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/messages.getChats`

Parameters:

id - Json encoded  array of InputChat



Or, if you're into Lua:

```
messages_Chats = messages.getChats({id={InputChat}, })
```


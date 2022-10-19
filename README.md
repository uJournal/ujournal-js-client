<div align="center">

![GitHub tag (latest SemVer)](https://img.shields.io/github/tag/LemmyNet/ujournal-js-client.svg)
[![GitHub issues](https://img.shields.io/github/issues-raw/LemmyNet/ujournal-js-client.svg)](https://github.com/LemmyNet/ujournal-js-client/issues)
[![License](https://img.shields.io/github/license/LemmyNet/ujournal-js-client.svg)](LICENSE)
![GitHub stars](https://img.shields.io/github/stars/LemmyNet/ujournal-js-client?style=social)
</div>

# ujournal-js-client

A javascript / typescript http and websocket client and type system for [Lemmy](https://github.com/LemmyNet/lemmy).

## Installation

`npm install ujournal-js-client`

## Usage

### Websocket Client

[LemmyWebsocket docs](classes/LemmyWebsocket.html)

```ts
import { Login, LemmyWebsocket } from 'ujournal-js-client';

let client: LemmyWebsocket = new LemmyWebsocket();

let form: Login {
  username_or_email: "my_email@email.tld",
  password: "my_pass",
};

this.ws.send(client.login(form));
```

### HTTP Client

[LemmyHttp docs](classes/LemmyHttp.html)

```ts
import { LemmyHttp } from 'ujournal-js-client';

let baseUrl = 'https://lemmy.ml';
let client: LemmyHttp = new LemmyHttp(baseUrl, headers?);
let jwt = await client.httpLogin(loginForm).jwt;
```

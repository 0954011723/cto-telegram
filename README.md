<h1 align="center">🤖️ chatbot-telegram</h1>
<p  align="center">
  <img alt="Version 1.0.0" src="https://img.shields.io/badge/version-1.0.0-blue.svg?cacheSeconds=2592000" />
  <a href="#" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-green.svg" />
  </a>
  <a href="https://twitter.com/ciyou_lee" target="_blank">
    <img alt="Twitter: Ciyou" src="https://img.shields.io/twitter/follow/ciyou_lee.svg?style=social" />
  </a>
</p>

> Yet another telegram ChatGPT bot which allows you to setup and run your bot with one simple command. PRs and suggestions are welcome. Leave a 🌟 if you find this project helpful.

> ⚠️ Warning: The underlying model is currently `gpt-3.5-turbo`, which is already fine-tuned for conversation **but costs money**. *A new OpenAI account comes with $18 free credit though, which is enough to run this bot for some time.*

> Support for using a reverse proxy to access the origin ChatGPT will be added soon.

<div  align="center">
<video src="https://user-images.githubusercontent.com/13758730/206657062-eec01c2a-0ef8-4605-b0b9-19a48fff236e.mp4"/>
</div>


## 🪄 Features
- [x] Run your ChatGPT telegram bot with single command.
- [x] Support group chat by metioning `@` bot while `bot privacy mode` turned off.
- [x] Reload conversion with `/reload` command.
- [ ] Support group chat with `/chat` command while `bot privacy mode` turned on.
- [ ] Support multiple conversions, unique for each chatID.
- [ ] Support login to OpenAI with password.

## 💿 Installation
1. Make sure you have installed `Deno` already. 

    If you don't, follow this official document to install. https://deno.land/manual@v1.28.3/getting_started/installation#download-and-install

2. Simply `git clone` or download this repo, `cd` into the project folder. 

3. Cache dependencies and check integrity with `lock.json`, *you only need to do this once*.

```
deno cache --lock=lock.json chatbot.ts
```

## 🔮 Usage
1. Complete Telegram bot token and ChatGPT session token in `env.example`.
```
BOT_TOKEN=YOUR_BOT_TOKEN
OPENAI_API_KEY=YOUR_OPENAI_API_KEY
```
To get your session token, see [Get ChatGPT Session Token](#-get-chatgpt-session-token).

2. Rename `env.example` to `.env`

```
mv env.example .env
```<h1 align="center">🤖️ chatbot-telegram</h1>
<p  align="center">
  <img alt="Version 1.0.0" src="https://img.shields.io/badge/version-1.0.0-blue.svg?cacheSeconds=2592000" />
  <a href="#" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-green.svg" />
  </a>
  <a href="https://twitter.com/ciyou_lee" target="_blank">
    <img alt="Twitter: Ciyou" src="https://img.shields.io/twitter/follow/ciyou_lee.svg?style=social" />
  </a>
</p>

> 這是另一個 Telegram ChatGPT 機器人，可以讓您使用一個簡單的命令來設置和運行您的機器人。歡迎提交 PR 和建議。如果您覺得此項目有幫助，請留下一顆 🌟。

> ⚠️ 警告：目前使用的模型是 gpt-3.5-turbo，它已經為對話進行了微調，但是需要支付費用。一個新的 OpenAI 帳戶帶有 $18 免費信用，足以運行此機器人一段時間。

> 很快將添加使用反向代理訪問原始的 ChatGPT 的支持。

<div  align="center">
<video src="https://user-images.githubusercontent.com/13758730/206657062-eec01c2a-0ef8-4605-b0b9-19a48fff236e.mp4"/>
</div>


## 🪄 功能特色
- [x] 透過單一指令運行您的 ChatGPT Telegram 機器人。
- [x] 當 `bot 隱私模式` 關閉時，透過在群組中提及 `@` 機器人來支援群組聊天。
- [x] 使用 `/reload` 指令重新載入轉換。
- [ ] 當 `bot 隱私模式` 開啟時，透過 `/chat` 指令支援群組聊天。
- [ ] 支援多個轉換，每個聊天 ID 唯一。
- [ ] 支援透過密碼登入 OpenAI。

## 💿 安裝
1. 請先確認您已安裝 `Deno`。

    如果您尚未安裝，請參閱官方文件進行安裝。https://deno.land/manual@v1.28.3/getting_started/installation#download-and-install

2. 可以透過 `git clone` 或下載此專案，`cd` 到專案資料夾中。

3. 使用 `lock.json` 緩存相依套件並檢查其完整性，*此步驟僅需進行一次*。

```
deno cache --lock=lock.json chatbot.ts
```

## 🔮 使用方式
1. 在 `env.example` 中完成 Telegram 機器人令牌和 ChatGPT 會話令牌。

```
BOT_TOKEN=YOUR_BOT_TOKEN
OPENAI_API_KEY=YOUR_OPENAI_API_KEY
```

若要取得您的會話令牌，請參閱[取得 ChatGPT 會話令牌](#-取得-chatgpt-會話令牌)。

2. 將 `env.example` 重新命名為 `.env`。

```
mv env.example .env
```

3. 執行 `deno run`，享受吧！

```
deno run chatbot.ts
```

Deno 需要您手動批准檔案系統讀取、環境變數存取和網路存取。您也可以使用以下參數運行，以預設方式授予權限。

```
deno run --allow-read --allow-env --allow-net chatbot.ts
```

## 🔑 取得 OpenAI API 金鑰
1. 在 https://beta.openai.com/signup 上註冊 OpenAI 帳號。

2. 在 https://platform.openai.com/account/api-keys 生成新的 API 金鑰。這是您的 API 金鑰，任何人都可以使用它來存取您的帳戶，這可能會導致意外的收費。請務必保密！

3. 將其貼上到您的 `.env` 檔案中。

## 💌 Credits
- [chatgpt-api](https://github.com/transitive-bullshit/chatgpt-api) 客戶端，用於非官方的 ChatGPT API。
- [授權](https://github.com/transitive-bullshit/chatgpt-api/blob/main/license)
- [node-telegram-bot-api](https://github.com/yagop/node-telegram-bot-api) NodeJS 的 Telegram Bot API。 
- [授權](https://github.com/yagop/node-telegram-bot-api/blob/master/LICENSE.md)
- [Lodash](https://github.com/lodash/lodash) - [授權](https://github.com/lodash/lodash/blob/master/LICENSE)
- 最終程式碼的三分之一和幾乎所有評論都是由 [Github Copilot](https://github.com/features/copilot). 撰寫。距離 AI 自動建立 AI 專案的日子還有多遠呢👀


3. `deno run` and enjoy!

```
deno run chatbot.ts
```

Deno requires you to approve file system reading, enviroment variables access and network access manually.
You can also run with these parammeters to give permission by default.

```
deno run --allow-read --allow-env --allow-net chatbot.ts
```

## 🔑 Get OpenAI API Key
1. Sign up for an OpenAI account at https://beta.openai.com/signup

2. Generate a new API key at https://platform.openai.com/account/api-keys. This is your API key, anyone can use it to access your account which may cause unexpected charges. Keep it secret!

3. Paste it in your `.env` file.

## 💌 Credits
- [chatgpt-api](https://github.com/transitive-bullshit/chatgpt-api) Node.js client for the unofficial ChatGPT API. - [License](https://github.com/transitive-bullshit/chatgpt-api/blob/main/license)
- [node-telegram-bot-api](https://github.com/yagop/node-telegram-bot-api) Telegram Bot API for NodeJS. - [License](https://github.com/yagop/node-telegram-bot-api/blob/master/LICENSE.md)
- [Lodash](https://github.com/lodash/lodash) - [License](https://github.com/lodash/lodash/blob/master/LICENSE)
- One-third of final code & almost all the comments was written by [Github Copilot](https://github.com/features/copilot). How far are we from the day where AI build whole project itself with AI 👀

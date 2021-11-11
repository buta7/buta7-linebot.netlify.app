# buta7-linebot.netlify.app

Netlify Functionを使ったオウム返しのLine Bot

## Set up

```shell
mkdir buta7-linebot.netlify.app
cd buta7-linebot.netlify.app
yarn init
```

netlify.toml

```toml
[build]
  command = "npm run build"
  functions = "dist/api"
```

add module

```shell
yarn add express @line/bot-sdk serverless-http netlify-lambda dotenv
```

.env(説明の手順に従って作成。Netlify側にも必要)

```
CHANNEL_ACCESS_TOKEN=Provider>Channel>Messaging API>Channel access token (long-lived)の値
CHANNEL_SECRET=Provider>Channel>Basic settings>Channel secret
```

## Local test

```shell
yarn run dev
ngrok htt 8080
```
上記を`Provider>Channel>Messaging API>Webhook`に登録して`Veriry`で確認

## Link

* [Netlify FunctionsでLINE BOTを作ってみる \- Qiita](https://qiita.com/n0bisuke/items/55de1cada13a623094b9)

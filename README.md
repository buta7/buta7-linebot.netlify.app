# buta7-linebot.netlify.app


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


## Link

* [Netlify FunctionsでLINE BOTを作ってみる \- Qiita](https://qiita.com/n0bisuke/items/55de1cada13a623094b9)

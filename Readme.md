# Polymer動作サンプル

Polymerの動作サンプル用リポジトリです。Heroku環境、またはローカル環境で動作します。

以下のGitHubリポジトリからフォークして作成しています。

https://github.com/nulltask/heroku-static-provider

## Polymerのインストール

Polymerを使用するためには、以下のbowerコンポーネントが必要となります

- Polymer/polymer
- Polymer/core-elements
- Polymer/paper-elements

※ このリポジトリは、上記内容はbower.jsonに設定済です。

また、HTMLドキュメントからは以下のように使用します。

```
<head>
  <!-- Polyfillのロード -->
  <script src="/components/platform/platform.js"></script>
  <!-- HTMLドキュメント内で使用するWeb Componentsのロード -->
  <link rel="import" href="/elements/my-menu-element.html">
</head>
```

## ローカル環境での起動

    $ npm install
    $ node server

## ページのブラウズ

ローカル環境で起動した場合、以下のURLでアクセス可能です。

```
http://localhost:3000
```

ポート番号は、環境により変化する可能性があります。

--- 

以下、フォーク元のnulltask/heroku-static-providerのReadmeを転載


# Heroku Static Provider

Static site provider for Heroku.


## Installation

You need sign-in or sign-up to Heroku.

    $ git clone https://github.com/nulltask/heroku-static-provider.git my-site
    $ cd my-site
    $ heroku create
    $ git push -u heroku master
    $ heroku open

## Deployment

Add or update files in `/public`.

    $ git add .
    $ git commit -a -m 'some commit message'
    $ git push heroku master
    $ heroku open

## Notes

### Adding Basic Auth

	$ heroku config:set USER=username
	$ heroku config:set PASS=password

### Screencast

  * https://vimeo.com/71315109

## License

MIT

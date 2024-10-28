# Docker + Astro + Wordpressのローカル環境の構築

 - PHP v8.1
 - Mysql v8.0
 - Wordpress v6.6.2
 - Node.js v20.18
 - Astro v4.16

## ディレクトリ構成

```
/
├── .vscode/
├── backend/
│   └── mysql/
│       ├── .data/ /* DBデータディレクトリ */
│       └── my.conf
├── frontend/
│   ├── astro/
│   └── Dockerfile
└── docker-compose.yml
```

## コマンド操作

dockerコンテナ起動
```
docker compose up -d
```

### Astro起動

Astroコンテナログイン
```
docker compose exec astro sh
```
`exit`でコンテナログアウト
```
/app # exit
```
Astroローカル起動
```
npm run dev
```

## バックエンドの構築

### DB（mysql）コンテナの構築

### Wordpressコンテナの構築

### Wordpressのインストール

### WordpressをヘッドレスCMS化（REST API化）

## フロントエンドの構築

### Nodeコンテナの構築

### Astroのインストール
```
docker compose exec astro sh
```
```
npm create astro@latest

Need to install the following packages:
create-astro@4.10.0
Ok to proceed? (y) y


 astro   Launch sequence initiated.

   dir   Where should we create your new project?
         .

  tmpl   How would you like to start your new project?
         Include sample files

    ts   Do you plan to write TypeScript?
         Yes

   use   How strict should TypeScript be?
         Strict

  deps   Install dependencies?
         Yes

   git   Initialize a new git repository?
         No
      ◼  Sounds good! You can always run git init manually.

      ✔  Project initialized!
         ■ Template copied
         ■ TypeScript customized
         ■ Dependencies installed
```

### AstorからAPIデータを取得


```
docker-compose down --rmi all --volumes --remove-orphans
```
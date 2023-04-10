# condition-records

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

ディレクトリ構成

ディレクトリ	内容
components	
├ api	axios での ajax 通信、web ストレージへのアクセス
├ atoms	button, input など
├ module	汎用的な関数。
バリデーションや userAgent 判定など
├ molecules	入力フォーム（見出し+パーツ）、スライダー、
カード型 UI など
├ organisms	ログイン、エラー、ローディング、notification など
├ pages	ページのコンテンツ
├ store	ログイン情報、会員情報
└ templates	ページの大枠

README.md

# 目次
- [目次](#目次)
- [コマンド](#コマンド)
- [実行フロー](#実行フロー)
- [実行環境](#実行環境)
- [Nodejsについて](#nodejsについて)
- [import文の注意](#import文の注意)

# コマンド
- 実行
  - `npm run start`

# 実行フロー
- `src/*`内のtypescriptをトランスコンパイルされる。
- `dist/*`内にコンパイル済みのjsが生成される。
- nodejsで`./dist/index.js`が実行される。


# 実行環境
- node: v18.12.1
- typescript: 5.1.3


# Nodejsについて
- Node.jsはGoogleのV8 JavaScriptエンジンを採用しています。
- V8はECMAScript 2015（ES6）の[標準](https://nodejs.org/ja/docs/es6)に従ってJavaScriptのコードを解釈します。


# import文の注意
- `import { User } from "./user/user.js";`
- tsファイルでもimport時は.jsとして読み込む。
- トランスパイルした際にjsが拡張子を判断できないため。
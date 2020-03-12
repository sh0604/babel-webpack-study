# babel / webpack 勉強会

## どういったものか
- さまざまなブラウザ（Chrome, Safari, IE11 etc...）で互換性を持たせるプログラムに変換するツール
- プラグイン作成使用ツール

### babel
- JavaScriptのコード変換ができる(ES6→ES5に変換など)
>const hoge = () => { do something... } → var hoge = function(){ do something... }

### webpack
- モジュールバンドラー（JSとライブラリを読み込んでいるJSを一つのJSファイルにまとめる）

## 完成形の構成
![スクリーンショット 2020-03-11 14 25 03](https://user-images.githubusercontent.com/36327504/76385229-91324a80-63a4-11ea-9d5d-5072b924e955.png)
![スクリーンショット 2020-03-11 14 30 11](https://user-images.githubusercontent.com/36327504/76385609-744a4700-63a5-11ea-891e-43d06c07f206.png)

## 用意するもの
- npm（Node Package Manager）・・・パッケージ管理コマンド  
https://nodejs.org/en/ にて LTSの方をダウンロード → インストール

## プラグイン作成流れ
```
1. プラグインテンプレートダウンロード
https://github.dev.cybozu.co.jp/system-planning/plugin-template 

プロジェクトディレクトリに移動（今回はplugin-template）
$ cd プロジェクトディレクトリ

2. 必要なライブラリをインストール(package.jsonの内容を元にnode modulesに取り込む)
$ npm install

3. プラグインをパッケージング
$ kintone-plugin-packer src

4. プロジェクトディレクトリに作成された秘密鍵の名前変更（webpack.config.jsに記載されたprivateKeyPathを元にplugin.zipを作成するため）
~.ppkを「private.ppk」に変更

5. webpackを使ったplugin.zipの作成(webpack.config.jsの内容を元にpluginを作成)
$ npm run build

6. pluginのアップロード
$ npm start

```

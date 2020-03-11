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
- npm（Node Package Manager）
https://nodejs.org/en/ にて LTSの方をダウンロード → インストール

## 基本設定

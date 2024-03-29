=== WP Facebook Portal ===
Contributors: ryo-nosuke
Donate link: https://github.com/rnsk/wp-facebook-portal
Tags: Facebook, Facebook page, portal, feed
Requires at least: 3.5.1
Tested up to: 6.3
Stable tag: 2.3.3
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Import the posts of Facebook page.


== Description ==

This plug-in is imports into WordPress posts from Facebook page posts.  
The cron function of WordPress is used and it is updated every 10 minutes.

You plurality is Facebook pages can be registered.  

Facebook ページでの投稿を WordPress にインポートするプラグインです。  
WordPress の疑似cron 機能を使い、10分ごとに更新されます。

対象となる Facebook ページは複数指定可能です。  
Facebook ページごとにインポートしたときの投稿カテゴリーをあらかじめ設定できます。  
手動によるインポートにも対応しています。  
※ご利用には Facebook App ID　および App Secret が必要です。

更新が滞っており申し訳ありません。  
暫定的な対応として「Facebook Access Token」を手入力することで使用できるように修正しました。  

使い方は次のとおりです。

1. Facebook developer のグラフAPIエクスプローラにアクセス
2. Facebook アプリを選択し、ページアクセストークンを取得  
    このとき、取得したいページを選択してページ投稿の読み取り権限がついていることを確認してください。
3. 「Generate Access Token」ボタンをクリックする
4. 表示されたアクセストークンをコピーする
5. WP Facebook Portal の設定画面を表示する
6. Facebook Access Token に先ほど生成したアクセストークンをペーストする
7. 「アクセストークンを取得」ボタンをクリックする  
    ここでは、新たに取得するのではなく、ペーストしたアクセストークンを保存します。

これで特定のFacebookページの投稿を読み込むことができます。  
取得したいページを増やす場合は手順「2」で権限を付与してください。  

アクセストークンには期限がありますので、期限が切れたら再度上記のとおり設定することで引き続き利用できます。

== Installation ==

1. Upload `wp-facebook-portal` to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Visit the "FB Portal -> Settings" menu.
4. Setup your Facebook application.


== Frequently asked questions ==

= Where can I get support? =

Please visit the [Support Forum](https://wordpress.org/support/plugin/wp-facebook-portal "Use this for support and feature requests")
for questions, answers, support and feature requests.


== Screenshots ==

1. Facebook APP setting.
2. Add Facebook page id.


== Changelog ==

2.3.3
WordPress 6.3 に対応  
Facebook API v.11.0 に対応  
Facebook Access Token が入力できるよう修正  

2.3.2  
WordPress 4.7.3 に対応  
Facebook API v.2.8 に対応  
APIのバージョン変更に伴う修正
記事自動取得の不具合を修正  
記事リンクの不具合を修正  

2.3.1  
Facebook ページが投稿した記事のみ取得するよう修正  
Facebook API v.2.2 に対応  
WordPress 4.0.1 に対応  
Modified to get only from Facebook page the posts.  
Corresponded to the Facebook API v.2.2  
Corresponded to the WordPress 4.0.1

2.3  
Facebook API v.2.1 に対応  
本文に含まれるURLに自動でリンクを貼る設定項目を追加  
国際化ファイル（POT）追加  
Corresponded to the Facebook API v.2.1  
Added new function: add automatic link by finding URL in the post.  
Added POT files

2.2  
写真投稿の場合、記事へのリンクがエラーになる不具合を修正  
WordPress 4.0 に対応

2.1  
タイムゾーン設定が他プラグインと競合する不具合を修正

2.0  
Facebook API v.2.0 に対応  
添付画像の取り扱い方法を選択できるよう設定項目を追加（アイキャッチ画像／記事に挿入）  
記事に挿入する場合、画像サイズを指定できるよう設定項目を追加  
複数の画像が添付されている投稿も取り込むよう修正（画像は1枚のみ取得）

1.2  
管理画面からプラグインを更新した場合にデータベースが更新されないバグを修正

1.1  
Facebook から読み込んだ投稿に自動で Facebook 記事へのテキストリンクを追加  
（追加の有無は設定画面で変更できます）

1.0  
Facebook での投稿が1行の場合にタイトルが登録されないバグを修正  
Facebook ページの削除後にメッセージが表示されないバグを修正

そのほかWordPressデフォルトの機能を優先して使うことで処理をスムーズに行うようにしました。

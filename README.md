# BitCharDiff
中身はJavaScript, HTML, CSSの練習  
特にp5.jsとか使っちゃう系
一応電子透かしのデモに使用予定
[OooWaterMark](https://github.com/matzTada/OooWaterMark)はこれをベースにGCTCデモ仕様になっている．

<a href="http://www.youtube.com/watch?feature=player_embedded&v=ugwSDbJy7Pc
" target="_blank"><img src="http://img.youtube.com/vi/ugwSDbJy7Pc/0.jpg" 
alt="movie on youtube" width=40% border="10" /></a>  
[movie on youtube](https://www.youtube.com/watch?v=ugwSDbJy7Pc)    

## ざっくりと

* サーバー側
	* 同じホストのJSONファイルを読んでwebsocketを用いてクライアントに送る
	* Node, Express
* クライアント側
	* JSONをwebsocket経由で受信してブラウザ上で表示する
	* JavaScript, HTML

## To Do

* Web serverを立てる
* Websocketとも結合してみる <https://team-lab.github.io/skillup-nodejs/3/1.html>
	* Serure WebSocket(wss)を使うべきなのかも？

## files

* ```/WaterMarkGUI/bin/www``` : server side program mainly for websocket
* ```/WaterMarkGUI/app.js``` : server side program mainly for frontend
* ```/WaterMarkGUI/views/index.ejs``` : client side script
* ```/WaterMarkGui/public/javascripts/chatSketch.js``` : client side program mainly for websocket and processing.js

## Info.

* 複数キャンバスを使うなら[instance mode](https://github.com/processing/p5.js/wiki/p5.js-overview#instantiation--namespace)を使う
	* これも役に立つ <http://www.joemckaystudio.com/multisketches/> 
* ```<div>```はブロック要素（一般的に前後に改行が入る）として，```<span>```はインライン要素（一般的に前後に改行が入らない）として使われる
* [p5.dom library](https://github.com/processing/p5.js/wiki/Beyond-the-canvas)はなんだかんだ重要

### 面白そうなライブラリ

* <https://github.com/bitcraftlab/p5.gui>
* <https://github.com/generative-light/p5.scribble.js>
* <https://github.com/linux-man/p5.tiledmap>7/28/2017 3:54:04 PM 

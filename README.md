# 2016_cinra

自宅学習用に以前作成したソースがあったため、流用しております。  
自動補完されるデータは、一般的に公開されている診療行為（病院を受信した際に受ける診断行為）の情報となります。  
下記サイトからダウンロードも可能。  
http://www.iryohoken.go.jp/shinryohoshu/downloadMenu/


#＜要件＞  
○課題内容  
c) テキストボックスに文字を入力すると自動で単語が補完される、所謂「自動補完（Auto Complete）」の仕組みを作成してください。データは任意のもので、DBを使用する必要はありません。（デザインは問いません）  


#＜実装内容＞
1.診療行為  
[診療行為]テキストボックスに 診療行為をテキスト入力すると、一致する文字を検索し自動補完を行う。  
ex.)「初診」、「在宅」とテキスト入力  
データ：「mstData.js」ファイルの「text」項目  
※1文字だけの入力では、選択肢が多く表示されてしまうため、2文字以上入力された場合に自動補完される。  


2.点数表区分番号  
選択された「診療行為」に紐づくコードが自動入力される。  
データ：「mstData.js」ファイルの「extra」項目  


3.診療項目  
選択された[診療項目]チェックボックスの背景色が変更される。  


4.補足  
入力された文字数をカウントし、規定文字数をオーバーした場合は入力文字数が赤字で表示される。  


#＜実装のポイント＞  
○日本語入力での自動補完  
○２文字以上入力された場合に入力補完  
○選択行に応じてコードを自動入力

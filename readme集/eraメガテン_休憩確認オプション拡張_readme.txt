*******************************************************************************
eraメガテン_休憩確認オプション拡張パッチ
*******************************************************************************

■ 始めに
当パッチはSHOP画面で[休憩]を選択した時の確認有無を設定するオプションに
確認しない+SHOP画面の[休憩]コマンドを[朝まで休憩]コマンドへ変更する機能を追加するパッチです。

■ 内容物
・readme           (当ファイル)
・SHOP_REST.ERB    (一部修正)
・OPTION.ERB       (一部修正)

■ 謝辞
eramaker、Emuera、及びeraMegatenに関わったすべての方々への多大なる謝辞をこの場で申し上げさせて頂きます。
また該当モジュールの制作者様にも重ねて謝辞を申し上げさせて頂きます。
旅人様のreadmeの書き方がとてもすばらしかったためパk..参考にさせていただきました。
制作者: 黒天


■ 目次
・１．導入方法
・２．機能
・３．開発者様へ
・４．ライセンス
・Ｚ．履歴

-------------------------------------------------------------------------------
１．導入方法
-------------------------------------------------------------------------------
■ 対象環境
ver0.290
ver0.290+修正ファイル1
ver0.290+修正ファイル2

■ 導入
下記の通り、ERBフォルダの配下にある
対象フォルダ内に、同封のERBファイルを配置・上書きして下さい。
(元ファイルがある為、上書きを確認されると思います。)
既に当該ファイルを改造されている場合には、差分導入をお願いします。
また環境が違う場合も不具合が発生する恐れがある為、こちらも差分導入をお願いします。

[フォルダ構成図]
+[ERB]
|
+--+[ＳＨＯＰ関連]
|  |
|  +--+[SHOP_REST.ERB]
|
+--+[調教関連]
   |
   +--+[OPTION.ERB]

-------------------------------------------------------------------------------
２．機能
-------------------------------------------------------------------------------
■ 既存の休憩確認オプションに「確認しない+[休憩]を[朝まで休憩]に変更する」
　 選択肢を追加。
　 この選択肢を選択した場合、SHOP画面の[休憩]コマンドが[朝まで休憩]に変更され、
　 [朝まで休憩]を選択すると自動的に次の朝まで休憩します。
　 休憩確認オプションは3つの選択肢がありますが、通常の3つの選択肢から1つ選ぶ
　 選択方式ではなく休憩確認オプションを選択するたびに
　 [確認する]→[確認しない]→[確認しない+朝まで休憩]→[確認する]
　 と選択内容が変化していくようになっていますので、選択内容にご注意ください。

-------------------------------------------------------------------------------
３．開発者様へ
-------------------------------------------------------------------------------
■ 修正工法
本パッチではフラグの追加などは行っておりません。

修正箇所を確認したい場合は、お手数ですが0.290を別の場所へ展開し、
同名ファイルと内容を比較してください。
前の処理に戻したい場合もお手数ですが0.290を別の場所で展開し、
該当箇所の差分を比較して修正してください。


-------------------------------------------------------------------------------
４．ライセンス
-------------------------------------------------------------------------------
ライセンスフリーです。自由に再利用して下さい。

-------------------------------------------------------------------------------
Ｚ．履歴
-------------------------------------------------------------------------------

2011/04/08 新規作成
2011/04/08 オプションのデフォルト値を「確認する」に変更
2011/05/05 オプションに確認しない+[休憩]を[朝まで休憩]に変更する選択肢を追加

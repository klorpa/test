*******************************************************************************
eraメガテン_悪魔全書参照情報切り替えパッチ
*******************************************************************************

■ 始めに
当パッチは悪魔全書を閲覧する際に登録した悪魔情報とオリジナル(CSV)の悪魔情報を
切り替える機能を追加するパッチです。

■ 内容物
・readme               (当ファイル)
・DEVIL_COMPENDIUM.ERB (一部修正)

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
ver0.298+修正ファイル

■ 導入
下記の通り、ERBフォルダの配下にある
対象フォルダ内に、同封のERBファイルを配置・上書きして下さい。
(元ファイルがある為、上書きを確認されると思います。)
既に当該ファイルを改造されている場合には、差分導入をお願いします。
また環境が違う場合も不具合が発生する恐れがある為、こちらも差分導入をお願いします。

[フォルダ構成図]
+[ERB]
|
+--+[女神転生]
   |
   +--+[悪魔合体]
      |
      +--+[DEVIL_COMPENDIUM.ERB]

-------------------------------------------------------------------------------
２．機能
-------------------------------------------------------------------------------
■ 追加機能
・全書登録している悪魔情報の閲覧において登録情報とオリジナル(CSV)情報を
　切り替えて参照できるようにする機能を追加

■ 対処確認状況
0.298+修正ファイル環境でパッチを当てた状態でのeraMegatenの起動確認済
追加機能動作確認済み

-------------------------------------------------------------------------------
３．開発者様へ
-------------------------------------------------------------------------------
■ 修正工法
本パッチではフラグの追加などは行っておりません。

修正箇所についてはお手数ですが0.298+修正ファイル環境を別の場所に展開し、
本パッチに含まれているファイルと同名のファイルと内容を比較して確認してください。
前の処理に戻したい場合もお手数ですが0.298+修正ファイル環境を別の場所に展開し、
同名ファイルの差分を比較し修正してください。

-------------------------------------------------------------------------------
４．ライセンス
-------------------------------------------------------------------------------
ライセンスフリーです。自由に再利用して下さい。

-------------------------------------------------------------------------------
Ｚ．履歴
-------------------------------------------------------------------------------
2011/10/01 新規作成
2011/10/01 コーディングをちょっと変えて、CPD_REGISTRATION.ERBを削除

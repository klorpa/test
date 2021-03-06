********************************************************************************
eraメガテン_デビサバ２パッチ
********************************************************************************

■ 初めに
当パッチはeraメガテンに、デビサバ２のメインシナリオを追加するパッチです。
一部は本体に取り込まれている為、拡張された差分のみ同封されています。


	;-------------------------------------------------
	;◆ver4.00
	;-------------------------------------------------
	・四日目のデータを追加




■ 内容物
・readme                      (当ファイル)

・Chara3004_メグレズ.csv      (一部修正)
・SKILL1015_破壊の星風.ERB    (新規作成)

・REQUEST_30_デビサバ２.ERB   (一部修正)
・REQUEST_30_4_デビサバ２_4日目.ERB     (新規作成)



■ 謝辞
eramaker、Emuera、及びeraMegatenに関わった
すべての方々への多大なる謝辞をこの場で申し上げさせて頂きます。
制作者：旅人


■ 目次
・１．導入方法
・２．機能
・３．開発者様へ

・Ｘ．１ 全体での構成図
・Ｘ．２ 全体での機能
・Ｘ．３ 全体でのパラメータ配分
・Ｘ．４ 全体での開発者向け情報

・Ｙ．ライセンス
・Ｚ．履歴


--------------------------------------------------------------------------------
１．導入方法
--------------------------------------------------------------------------------
■ 対象環境
ver0.300 + 修正6


■ 導入
下記の通り
CSV、およびERBフォルダの全てのファイルを、構成図通りに配置・上書きして下さい。

同封のCSVフォルダとERBフォルダをコピーして、そのまま被せれば導入出来ます。
既に当該ファイルを改造されている場合には、差分導入をお願いします。


【フォルダ構成図】

+[CSV]
|
+--+[悪魔]
   |
   +--+[30_七星(セプテントリオン)]
      |
      +---[Chara3004_メグレズ.csv]


+[ERB]
|
+--+[RPG]
   |
   +--+[スキル関係]
   |  |
   |  +--+[衝撃]
   |     |
   |     +---[SKILL1015_破壊の星風.ERB]
   |
   +--+[依頼]
      |
      +--+[REQUEST_30_デビサバ２]
         |
         +---[REQUEST_30_3_デビサバ２_4日目.ERB]
         +---[REQUEST_30_デビサバ２.ERB]


--------------------------------------------------------------------------------
２．機能
--------------------------------------------------------------------------------
デビサバ２の四日目を追加します。
併せて細かい仕様変更などが入っています。

	;-------------------------------------------------
	;◆追加したもの
	;-------------------------------------------------
	・依頼30「デビサバ２」に四日目を追加

	・スキル衝撃に「破壊の星風」を追加

	;-------------------------------------------------
	;◆更新したもの
	;-------------------------------------------------
	・Chara3004_メグレズ.csv

	;-------------------------------------------------
	;◆競合が起きそうなファイル
	;-------------------------------------------------
	・特になし


--------------------------------------------------------------------------------
３．開発者様へ
--------------------------------------------------------------------------------
開発者向け情報です。

・特になし










--------------------------------------------------------------------------------
Ｘ．１ 全体での構成図
--------------------------------------------------------------------------------
当パッチの過去バージョンを含めた、全体での構成図です。


【フォルダ構成図】

+[CSV]
|
+--+[悪魔]
|  |
|  +--+[17_堕天使]
|  |  |
|  |  +---[Chara1715_ボティス.csv]
|  |
|  +--+[30_七星(セプテントリオン)]
|  |  |
|  |  +---[Chara3001_ドゥベ.csv]
|  |  +---[Chara3002_メラク.csv]
|  |  +---[Chara3003_フェクダ.csv]
|  |  +---[Chara3004_メグレズ.csv]
|  |  +---[Chara3005_アリオト.csv]
|  |  +---[Chara3006_ミザール.csv]
|  |  +---[Chara3007_ベネトナシュ.csv]
|  |
|  +--+[42_超人]
|     |
|     +---[Chara4217_ジプス局員.csv]
|     +---[Chara4218_敵ロナウド.csv]
|
+--+[人間]
   |
   +---[Chara4601_デビサバ２主人公.csv]
   +---[Chara4602_志島大地.csv]
   +---[Chara4603_新田維緒.csv]
   +---[Chara4604_迫真琴.csv]
   +---[Chara4605_九条緋那子.csv]
   +---[Chara4606_伴亜衣梨.csv]
   +---[Chara4607_管野史.csv]
   +---[Chara4608_柳谷乙女.csv]


+[ERB]
|
+--+[RPG]
   |
   +--+[スキル]
   |  |
   |  +--+[打撃]
   |  |  |
   |  |  +---[SKILL237_なぎ払い.ERB]
   |  |  +---[SKILL238_絶妙打.ERB]
   |  |  +---[SKILL239_八相発破.ERB]
   |  |
   |  +--+[火炎]
   |  |  |
   |  |  +---[SKILL735_連星の炎.ERB]
   |  |
   |  +--+[氷結]
   |  |  |
   |  |  +---[SKILL816_周極の巨砲.ERB]
   |  |
   |  +--+[電撃]
   |  |  |
   |  |  +---[SKILL925_暗黒の雷光.ERB]
   |  |
   |  +--+[衝撃]
   |     |
   |     +---[SKILL1015_破壊の星風.ERB]
   |
   |
   +--+[依頼]
      |
      +--+[REQUEST_30_デビサバ２]
         |
         +---[REQUEST_30_デビサバ２.ERB]
         +---[REQUEST_30_1_デビサバ２_1日目.ERB]
         +---[REQUEST_30_2_デビサバ２_2日目.ERB]
         +---[REQUEST_30_3_デビサバ２_3日目.ERB]
         +---[REQUEST_30_4_デビサバ２_4日目.ERB]
         +---[REQUEST_30_ニカイア動画.ERB]


--------------------------------------------------------------------------------
Ｘ．２ 全体での機能
--------------------------------------------------------------------------------
当パッチの過去バージョンを含めた、全体での機能説明です。

	;-------------------------------------------------
	;◆機能概要
	;-------------------------------------------------
	依頼「30」に、デビサバ２のメインシナリオを追加します。


	;-------------------------------------------------
	;◆開始条件
	;-------------------------------------------------
	主人のレベルが30以上で、依頼が発生します。
	その後は依頼画面にて、シナリオが進行します。


	;-------------------------------------------------
	;◆シナリオストップ
	;-------------------------------------------------
	実行可能な全てのシナリオをこなすと、待機命令の依頼が来ます。
	続きのシナリオが作成されるまで、気長にお待ち下さい。

	なお待機命令が出た後は、シナリオが追加されても「追加された」という連絡は来ません。
	依頼のタイトルが変わっていれば、新シナリオが追加されています。
	依頼を選び、シナリオを進めて下さい。


	;-------------------------------------------------
	;◆シナリオについて
	;-------------------------------------------------
	基本は原作に沿う形で進行。
	ただeraMegaten世界の大部分を破壊するのは不味い気がするので、原作の様な大破壊は起きていません。
	各地で消失騒ぎや悪魔騒ぎが起きているぐらい。

	;ジョーとか男連中の扱いに困る…どこで追加すれば良いんだ…


	;-------------------------------------------------
	;◆女性キャラの調教
	;-------------------------------------------------
	女性キャラは加入時、MASTER以外の誰かに凌辱されている事があります。
	"CFLAG:イベント加入"に凌辱の進行度が保存されている為、口上側で利用可能です。
	利用する場合、正確な進行具合は"REQUEST_30_ニカイア動画.ERB"ファイルにて確認出来ます。
	(例えば進行度3なら、該当キャラの進行度3の情景を探せば良い)


--------------------------------------------------------------------------------
Ｘ．３ 全体でのパラメータ配分
--------------------------------------------------------------------------------
当パッチの過去バージョンを含めた、全体でのパラメータの配分説明です。


	;-------------------------------------------------
	;◆人間キャラの仕様
	;-------------------------------------------------
	全キャラが異能者なので、成長させるだけでそれなりにスキルが揃います。
	LV50になる頃には相当な便利スキルが揃っている筈です。

	ただし最上級スキルを覚えるのは、原作での能力特化キャラだけとなっています。
	例えば物魔バランス型だと、メギドとかは習得しない…と言ったバランスです。


	;-------------------------------------------------
	;◆敵の強さ
	;-------------------------------------------------
	基本的にイベント戦闘で進むので、強めに設定してあります。
	負けたらまた戻って対策し、右クリックで文章すっ飛ばして再戦、といった感じです。
	パーティの攻守の属性を偏らせず、多角的に用意しておけば、恐らく初見でも突破出来ます。

	原作通り、耐性を持たないと「かなり強い」と感じる強さで調整しています。


	;-------------------------------------------------
	;◆セプテントリオン（七星）の仕様
	;-------------------------------------------------
	原作に火器が効かないとある為、飛具は無効化。
	それ以外は物理３種と基本の４属性、万能以外は全て無効化で設定。

	どこか懐かしい、SFC時代の様なスタンダードな戦闘を強いられる感じで調整。
	どの七星も一週目は初見殺しだったと思うので、こちらも初見殺しで。



--------------------------------------------------------------------------------
Ｘ．４ 全体での開発者向け情報
--------------------------------------------------------------------------------
全体での開発者向け情報です。
プログラムの制御方法などが記載されています。


	;-------------------------------------------------
	;◆シナリオ制御
	;-------------------------------------------------
	依頼「30」からサブファイル（サブシナリオ）をCALLする形でシナリオを制御。
	これにより、依頼「30」以外を使用しないで済む様になっている。
	サブシナリオは、一日ごとに１ファイル作成する予定。
	つまり８日間で合計８ファイルとなる。


	またイベントが終わる度に依頼「30」の"読み込みフラグ"を初期化している。
	これによりSHOP画面にて新たに依頼が発生した様に、見かけ上演出している。
	（実際は同じ依頼「30」を使い回している。）


	;-------------------------------------------------
	;◆ファイル構成
	;-------------------------------------------------
	"REQUEST_30_デビサバ２.ERB"から、各サブファイルをCALLしている。

	"REQUEST_30_ニカイア動画.ERB"をサブファイルから分離しているのは、
	後で動画を観賞出来る様にしようかなぁとか思ってたり。
	その為ログ表示と調教度の加算処理を分離して実装している。


	;-------------------------------------------------
	;◆フラグ管理
	;-------------------------------------------------
	"REQUEST_30_デビサバ２.ERB"のヘッダに管理方法が記載されている。

	簡単に抜粋すると3桁の数字を保存し、
	「百の桁が日付」
	「十の桁がイベント」
	「一の桁がイベントの詳細（進行度）」
	という形でシナリオ制御に使っている。

	つまり、
	一日に１０を超えるイベントは登録出来ないし、
	一つのイベントに１０を超える途中経過（進行度）は登録出来ない…となる。

	この3桁の数字は、"FLAG:デビサバ２進行度"に保存している。





--------------------------------------------------------------------------------
Ｙ．ライセンス
--------------------------------------------------------------------------------
ライセンスフリーです。自由に再利用して下さい。


--------------------------------------------------------------------------------
Ｚ．履歴
--------------------------------------------------------------------------------

2011/11/27 ver4.0
           四日目を作成完了


2011/10/28 ver3.0
           三日目を作成完了
           だんぼーる作戦はカット。
           悩んだ結果敵の人間勢は、調整のし易さから超人CSVで作成する事で決定。
           味方加入時は人間CSVを別途用意する予定。

           イオの貫通を廃止、代わりに万魔の一撃を追加。
           低レベルで加入させたいという意見があったので、レベル帯を低下させて様子見。


2011/10/10 ver2.0
           二日目を作成完了


2011/09/08 ver1.7
           ファイル構成を見直して、再構築
           （仕様が未確定な男性陣のファイルを除外）
           不要な"#DIM DYNAMIC"を最適化

2011/09/03 ver1.6
           周回用の処理が入っていないバグを修正

2011/09/02 ver1.5
           ジプス局員を人間(0)から超人(43)に種族変更

2011/09/02 ver1.4
           ver1.2修正時のフラグミスを修正

2011/09/02 ver1.3
           ニューゲーム時にフラグの初期化が漏れているバグを修正

2011/09/01 ver1.2
           イオが調教しないとパーティーに入れられない状態だったバグを修正

2011/08/30 ver1.1
           セプテントリオンの種族を19から30に変更

2011/08/26 ver1.0
           一日目を作成完了
           設定関連の記述とかキャラの特徴とか書いてたら、40KB超えてた。
           ちょっとクドい感がある。
           添削すれば結構削れる箇所がありそうだけど、もう上げてしまう。
           二日目以降はもっとマイルドにする予定。

2011/08/23 新規作成



＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝
○はじめに
＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝

	このパッチは、調教でビデオを撮影したとき、キャラごとにその内容（実行したコマンドの履歴）を覚えておいて、あとで参照できるようにするものです
	
	Ver0.293.3用　それ以外でも動作するかもしれませんが知らん

	口上の分岐につかいたいなーというのがきっかけでした。
	現状、撮影した内容は次に撮影が発生するまで特に初期化もされず、誰が写っているのかも記録されず、そのためかビデオの値段を算出するためにしか使われていません。
	せっかく[29 ビデオ鑑賞]ってコマンドがあるのにもったいないなあ
	内容に関する情報をとっておけばいいのになあと思ったわけです。
		嫁と撮ったホームビデオを見ながらちゅっちゅとか
		[淫乱]奴隷とあーでもないこーでもないとＡＶ企画会議＆実践したりとか
		処女喪失ビデオを何度も何度でも見せ付けるとか（※このパッチでは実現できません）
	そういう口上が書きたかったのです
	
	このパッチでもってＡＶ好きの皆さんに喜んでいただけたらなと思います
	もっと嫁なり奴隷なりの痴態を撮ったらいいとおもいます
		×ワグナス！
	
	
	
	現状ではコマンドのみを記録することを想定しています。
	実行時の状況、とりわけ衣装とかマジ重要だろと思いますし、絶頂した！　とか破瓜の血が！　とかも記録したいのですが、気の利いた記録方法も思いつかないのでぶん投げ。
		ハイライトだけ選んで記憶するような処理が簡便に出来たらいいのですが。
		あとeraSQのタイトル自動生成いいですねアレ。全然関係ない話ですけども。

＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝
○変更の及ぶファイル
＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝
	
	\CSV
		Cflag.csv
		TCVAR.csv
		VariableSize.csv
	\ERB
		\調教関連
			\COM
				COMF183_ビデオカメラ.ERB
					@EQUIP_COM183
						ビデオ内容の記憶をFLAGからTCVARに変更
						撮影内容が自慰で、かつバイブなどの派生オナニーだったなら、その旨も記録
			WORK.ERB
				@PRICE_VIDEO
					ビデオ内容の取り出しをFLAGからTCVARに変更
					コマンドとビデオの値段の対応表を表示するように
					処女喪失を撮影したビデオの値段を見た後、フラグを折ることでAbnormalEXPを何度も取れないように
					
				@SELL_VIDEO
					ビデオを保持することにした際に、CFLAGにビデオの内容を記憶する処理を追加
					
	\組み込み関数
		\キャラクタデータ参照／CFLAG
			VIDEO_FUNCS.ERB（新規作成）
				@VIDEO_COM_INCLUDE＿CFLAG
					引数のコマンドが保持しているビデオのどのあたりに写っているかを判定する関数
					詳しくはファイルの中身をご覧ください
				@VIDEO_COM_INCLUDE_TCVAR
					こちらは上のと同じ機能、ただしCFLAGではなくTCVARを見ます
					詳しくはファイルの中身をご覧ください
						TCVARを扱う関数なのでこのフォルダに入れるのは本当はよろしくないのでしょうが
						同じパッチに付属する下部機能なので一箇所にまとめておきたかった

＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝
○新規に確保した（い）CSVの領域
＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝
	
	CFLAG:1500〜1510　ビデオ一本ぶんのコマンド記憶
		;ビデオ撮影用とあるのでいただきます
		できるなら、さらなる用途のため1510〜1539あたりも貰いたいところであります
	TCVAR:110〜120　かつてFLAG:11〜21で保持されていたのをTCVARに移管
		TCVARなので一次的な保存であり、調教終了時にビデオを保存しなければこの内容は捨てられます
		なお、TCVARは105までしか確保されてなかったので121まで伸ばしました
	
＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝
○思い残したこと
＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝

	現状はビデオを何本撮ろうが、最後に一括で全部売るか、残すかを選ぶことしか出来ません。
	本当は「このビデオは売るけどあのビデオは残す」というようにしたいのですが、ビデオＮ本分もの内容→Ｎ＊１０個のコマンドをいちいち記録するのは阿呆のような気がしますし、簡便な処理も思いつかないのでこの問題は放置しています

	「ビデオを残す」ことを選んだ場合、残るのは最後に撮っていたぶんです
	一度の調教で何本も撮ると最新の内容がどんどん上書きされていくのであしからず
	あなたのビデオ記録装置は容量が限られているのです
	
	
＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝
○本パッチの仕様とその使いかた　口上作者向け
＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝
	
	このパッチを導入する事で、[29 ビデオ鑑賞]・調教終了後のビデオ売却or保存時の地の文・口上に更なる分岐が作れます
		もちろん「作れる」というだけで、「作らなくてはならない」というわけではありません。念のため
	
	ここでは具体的なシチュエーションを挙げつつ、本パッチで追加された機能の使い方を示します。
	ご参考までに

-----------------------------------------
ビデオの内容がどのように記録されているか
――ビデオの内容に関係した感想を述べる
-----------------------------------------
	調教終了後に保持を選んだビデオの内容は、CFLAG:1500〜CFLAG:1509にコマンド番号という形で保存されています
	具体的には
	
	愛撫→オナニー→撮影終了というビデオを保存すると
	
	CFLAG:1500		0;愛撫
	CFLAG:1501		6;胸愛撫
	CFLAG:1502		-1;撮影終了、ないし何も写っていない

	という風に記録されます

	ので、
	
		;口上の[29 ビデオ鑑賞]部分において
		IF CFLAG:1500 == 22
			;コマンド番号 22は「会話する」
			PRINTW 「どうしてＡＶって最初はインタビューから入るんでしょうね」
		ENDIF
		
	などと言ったように、ビデオの内容によって分岐を入れることが出来ます
	
	
-------------------------------------------------
このコマンドはビデオの内容に含まれているか？
――ビデオに写っていたのと同じコマンドを実行し、その感想を問う
------------------------------------------------
	あるコマンドが保持しているビデオに入っているかどうかは、@VIDEO_COM_INCLUDEで判定できます
	VIDEO_COM_INCLUDE（キャラクタ番号,コマンド番号）は、第一引数のキャラクタがもっているビデオにおいて、第二引数のコマンド番号が含まれていればそれが何シーン目であるかを、含まれていなければ０を返します
		※Ｎシーン目とは、撮影回数がＮ/10であったときの事を指します
	ので、たとえば以下の様な使い方が出来ます
	
	;キス（コマンド番号＝20）において
	IF VIDEO_COM_INCLUDE(TARGET,20) =! 0 && PREVCOM == 29
		;所持ビデオにキスが含まれており、かつ直前の実行コマンドがビデオ鑑賞（コマンド番号＝29）である
		PRINTW 「ビデオを見ていて思ったんですが」
		PRINTW 「傍から見る、とキスしているときって思いのほか間抜けな顔しているものなんですね……」
		PRINTW 「――なんですかその目は。なに唇突き出してるんですか」
		PRINTW 「そういうのは女がするものではないんですか、ほら」
	ENDIF


--------------------------------------------------
今撮っているビデオの内容
――「コレはもう写したから他のを撮りましょう」
--------------------------------------------------
	現在進行形で撮影中のビデオの情報は、ビデオを売るか残すか選択するときまではCFLAGではなく、TCVARに保存されています
	なので、撮影している途中に、今撮っているビデオの内容について言及したい場合は、TCVAR:110から119を参照してください
	これもコマンドが格納されています
	また、今撮影中のビデオにあるコマンドが写っているかどうかは、@VIDEO_COM_INCLUDE_TCVAR()にて確認できます
	使い方は@VIDEO_COM_INCLUDEと同じです

	思わせぶりなサブタイですが！　サンプルは無しだ！　自力救済！


＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝
○更新履歴
＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝＝

11/06/30 新規作成
Emuera 1.808 beta006
・1807+v14までの私家版の更新を取り込み
・ヘッダーファイル（.ERH）実装
　・#DIM (GLOBAL SAVEDATA)　による広域変数の宣言
　・#DEFINE によるDEFINEマクロの定義
・#LOCALSIZE、#LOCALSSIZE、#DIM、DIMSのサイズ指定に定数式を許可。
・プリプロセッサ[IF XXX]、[ELSEIF XXX]、[ELSE]追加
・ARG、ARGSまたはプライベート変数でない変数を関数の引数としたときには引数を省略できないように
　・対応して互換性オプション「ユーザー関数の全ての引数の省略を許可する」追加
・ユーザー関数の文字列型の引数に数値が渡されたとき、自動で文字列型に変換していたのを止める
　・対応して互換性オプション「ユーザー関数の引数に自動的にTOSTRを補完する」追加
・SAVEVAR, LOADVAR, CHKVARDATA, SAVECHARA, LOADCHARA, CHKCHARADATAを関数名として予約
・SKIPDISP命令をSIF文の直後に置くことを可能に
・オプション「セーブデータをバイナリ形式で保存する」追加
AbnormalEXP取得時に記録しステータス画面に表示を行います。
改変、改造、その他、自由にしてもらって結構です。

変更点

CSV
Cflag.csv
1324,AbnormalEXP記録	を追加

ERB
SHOW_STATUS.ERB
521,522行に関数呼び出し追加
1032から1125行に関数追加

ERB\調教関連
SOURCE.ERB
2847行からのAbnormalEXP付与関数にCFLAGへの記録処理を追加

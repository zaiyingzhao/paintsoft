# paintsoft
**ソフトウェアⅡ第3回**

# paint1
簡易ペイントソフトを実装しました。実行は **./paint1 描画範囲の横幅 描画範囲の縦幅**です。
コマンドは6つあり  
- line: 直線を描画 実行方法：**line x1 y1 x2 y2**
- rect: 長方形を描画 実行方法：**rect x0 y0 width height**
- circle: 円を描画 実行方法：**circle x0 y0 r** （ターミナルの性質上正円にはなりません）
- save: 現状のコマンド履歴を保存 実行方法：**save filename**　（filnameを省略するとhistory.txtに読み込まれます）
- undo: 直前の描画コマンドを取り消す
- quit: ペイントソフトを終了する

# paint2

ファイルに保存されたコマンド履歴を読み込み絵を再描画するコマンドloadを実装しました。実行方法は**load filename**  
ただし引数がない場合は必然的にhistory.txtから読み込まれるようにし、引数がファイルが存在しないときのためにenumにINVALIDFILEを追加してエラーを表示できるようにしました。  

# paint3

描画の文字種を変更するコマンドchpenを実装しました。実行方法は**chpen letter (e.g. @)**  
履歴を線型リストに追加し、saveしたときにhistoryにchpenのコマンドも表示されるようにしました。

# paint4（発展課題）

新たなコマンドとして視力チェックのときに用いられるテストコマンド（Cの向きを答えるやつ）visiontestを追加しました。実行は**visiontest size(large, medium, smallのいずれか) direction(right, left, up, downのいずれか)**  
で、入力後対応したサイズと対応した位置に隙間のあるC(ランドルト環)が描画されます。ランドルト環の描画はcircleを応用しました。

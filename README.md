[paint1]

rectとcircleを実装しました。circleは中心からの距離の2乗が(r-1)^2より大きくr^2以下であればプロットするという条件で実装しましたが、課題説明であった通り正円にはなりませんでした。（そこは許容としました）

[paint2]

loadを実装しました。ファイルが存在しないときのためにenumにINVALIDFILEを追加し、エラーを表示できるようにしました。load関数の中でinterpret_command関数を実行するという発想に至るまでに時間を要しました。

[paint3]

chpenを実装しました。履歴を線型リストに追加し、saveしたときにhistoryにchpenのコマンドも表示されるようにしました。

[paint4]

新たなコマンドとして視力チェックのときに用いられるテスト（Cの向きを答えるやつ）visiontestを追加しました。入力は「visiontest size(large, medium, smallのいずれか) direction(right, left, up, downのいずれか)」の形式で行うと、それに対応したサイズと対応した位置に隙間のあるC(ランドルト環というみたいです)が描画されます。ランドルト環の描画はcircleを応用しました。
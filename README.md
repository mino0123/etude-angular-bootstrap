## AngularJSとBootstrapで作ってみたタスクリスト

習作として作ったタスクリスト

[http://mino0123.github.io/etude-angular-bootstrap/](http://mino0123.github.io/etude-angular-bootstrap/)


以下、作成メモ

#### バリデーションは捨てる
例えば、required指定した項目に初期値が無いと入力前からエラーの状態で表示される。
中途半端に使えるところだけAngularのバリデーション使っても
エラー表示のタイミングに一貫性がなくなるだけなので、
全部のバリデーションをAngular任せにできないようなら捨てる。


#### リスト要素が持つ関数での要素の判別
最初は要素番号を関数に渡そうとしたけど、やり方がわからなかったので
関数内でArray#indexOfで自要素の番号を取得しなおした。


#### リスト要素からのリスト操作
内側のコントローラに外側のコントローラのスコープが持つプロパティが渡るが、
外スコープのプロパティに対して再代入できない。
なので内部から外部のスコープが持つプロパティを変更するには破壊的な変更をする手段か、
もとのプロパティ自体をオブジェクトにする必要がある。
(配列要素の削除でちょっと困った)


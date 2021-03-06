## ピニャータをたたいてみよう

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
このステップでは、ピニャータがクリックされるたびに音をだし、たたいた数をカウントするようにピニャータをコーディングします。
</div>
<div>
![ピニャータが10回クリックされるアニメーション画像。 10回のあと, コスチュームはわれたものにかわり、変数（へんすう）がきえます。](images/break-pinata.gif){:width="300px"}
</div>
</div>

--- task ---

**ピニャータ**のスプライトで**音**タブをクリックしてみよう。**ボヨン**という音をみつけて聞いてみよう。 **再生**ボタンをクリックすると、音が出ます。

![ボヨンの音が表示され再生ボタン (青い円に白い三角) がハイライトされている音タブ](images/play-boing.png)

--- /task ---

Scratchでは、つなげたブロックのグループは **スクリプト**と呼ばれます。 スプライトは複数（ふくすう）のスクリプトを持つことができます。

--- task ---

**コード** タブをクリックしてみて。 `イベント`{:class="block3events"}の中から、 `このスプライトが押されたとき`{:class="block3events"} ブロックをスクリプトエリアにドラッグして、新しいスクリプトをはじめよう。

`音`{:class="block3sound"} ブロックメニューで、`__の音を鳴らす`{:class="block3sound"} ブロックを見つけてね。 それを`このスプライトが押されたとき`{:class="block3events"} ブロックの下にドラッグするよ：

![ピニャータのスプライトアイコン](images/pinata-sprite.png)

```blocks3
when this sprite clicked
start sound [Boing v]
```

--- /task ---

--- task ---

**テスト:** ステージの上の**緑の旗** をクリックし、プロジェクトを実行してみよう。 ゆれているピニャータをクリックすると、ボヨンという音がなります。

--- /task ---

`変数`{:class="block3variables"}は、数やテキストを入れておく方法です。 ピニャータがクリックされた回数は、 `たたいた数`{:class="block3variables"}という変数に保存されるため、いつでも使用できます。

--- task ---

`変数`{:class="block3variables"} ブロックメニューから、**変数を作る** ボタンをクリックしよう。

![変数メニューブロックと「変数を作る」ボタン](images/make-variable.png)

新しい変数**たたいた数**を作るよ：

![「新しい変数」ポップアップウィンドウで「新しい変数名」に「たたいた数」と入力](images/new-variable.png)

**注意：** 新しい「たたいた数」という変数（へんすう）がステージの上にあらわれ、 `変数`{:class="block3variables"} ブロックの中で使うことができるようになります。

![ステージ上の変数「たたいた数」](images/variable-stage.png)

![新しい「たたいた数」ブロックを含んだ変数ブロック](images/variable-blocks.png)

--- /task ---

--- task ---

プロジェクトがスタートするたび、 `たたいた数`{:class="block3variables"} の数字は`0`{:class="block3variables"}にリセットされます。

`たたいた数を0にする`{:class="block3variables"} ブロックをスクリプトエリアのはじめのスクリプトにドラッグし、 `コスチュームを__にする`{:class="block3looks"} ブロックと`x座標を(0) 、y座標を (180)にする`{:class="block3motion"} ブロックの間においてね。

コードはこんな感じになるよ：

![ピニャータのスプライトアイコン](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (まるごと v)
+ set [たたいた数 v] to (0)
go to x: (0) y: (180)
point in direction (90)
forever
repeat (10)
turn right (1) degrees
end
repeat (20)
turn left (1) degrees
end
repeat (10)
turn right (1) degrees
end
```

--- /task ---

--- task ---

**ピニャータ** のスプライトがクリックされるたびに、`たたいた数`{:class="block3variables"} の数字がふえるようにします。

**ピニャータ**のスプライトをクリックすると `たたいた数`{:class="block3variables"} が `1`{:class="block3variables"} ずつかわるようにブロックを追加してみよう：

![ピニャータのスプライトアイコン](images/pinata-sprite.png)

```blocks3
when this sprite clicked
start sound [Boing v]
+ change [たたいた数 v] by (1)
```

--- /task ---

--- task ---

**テスト：**プロジェクトをなん回か実行してみよう。 `たたいた数`{:class="block3variables"} が、いつも`0`{:class="block3variables"} からはじまり、**ピニャータ**をクリックするたびに `1`{:class="block3variables"}ずつ数がふえていることをチェックしてね。

![値が「8」となっている変数「たたいた数」が表示されているステージ](images/hits-increase.png)

--- /task ---

ピニャータはわれにくいですが、ずっとつづくわけではありません。 `10 回`{:class="block3variables"}たたくと、われて、あきます。

`もし__なら`{:class="block3control"}ブロックは、**条件**によって決定（けってい）するときに使います。

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
私たちは意思決定（いしけってい）をするときはいつも<span style="color: #0faeb0">**条件**</span>を使います。 「えんぴつの芯（しん）がとがっていなければ、けずる」と言います。 おなじように、「もし」ブロックと条件（じょうけん）を使って、ある条件が真（しん）か偽（ぎ）かによって、ちがう処理（しょり）をするコードを書くことができます。
</p>

--- task ---

`制御`{:class="block3looks"} ブロックパレットを開いてみて。 `もし__なら`{:class="block3control"} ブロックをスクリプトエリア にある`このスプライトが押されたとき`{:class="block3events"} の中のスクリプトをかこむようおいてね:

![ピニャータのスプライトアイコン](images/pinata-sprite.png)

```blocks3
when this sprite clicked
+ if <> then
start sound [Boing v]
change [たたいた数 v] by (1)

```

--- /task ---

`もし__なら`{:class="block3control"}ブロックは、なかの六角形（ろくかくけい）のところに条件（じょうけん）を入力することができます。

--- task ---

**ピニャータ**のスプライトは、**`もし`{:class="block3control"}** `たたいた数`{:class="block3variables"} の数字が`10`{:class="block3variables"} `より少ない場合`{:class="block3operators"}音をならし、 変数`たたいた数`{:class="block3variables"}のカウント数をふやします。

まず、六角形のところに`<`{:class="block3operators"}を追加（ついか）するよ：

![ピニャータのスプライトアイコン](images/pinata-sprite.png)

```blocks3
when this sprite clicked
+ if <() < ()> then
start sound [Boing v]
change [たたいた数 v] by (1)

```

--- /task ---

--- task ---

変数（へんすう）`たたいた数`{:class="block3variables"} を`<`{:class="block3operators"}の左にドラッグし、右に「10」と入力して`もし__なら`{:class="block3control"}の条件（じょうけん）を完成させます：

![ピニャータのスプライトアイコン](images/pinata-sprite.png)

```blocks3
when this sprite clicked
+ if <(たたいた数) < (10)> then
start sound [Boing v]
change [たたいた数 v] by (1)

```

--- /task ---

--- task ---

**テスト：**プロジェクトをもういちど実行してみよう。 ピニャータを10回たたいて、音がなることと、変数`たたいた数`{:class="block3variables"} のカウント数がふえることを確認しよう。

ピニャータをもっとたたいてみて。 変数`たたいた数`{:class="block3variables"}は、10より大きくはなりません。なぜかというと、`もし__なら`{:class="block3control"}の条件が「true（真）」ではなくなったため、その中のコードが実行されなくなったのです。

--- /task ---

--- task ---

2つめの`もし__なら`{:class="block3control"} ブロックを、1つめの中に追加（ついか）してみて。 こんどの条件（じょうけん）では、`たたいた数`{:class="block3variables"} `=`{:class="block3operators"} 10 であることをチェックして、「true（しん）」の場合 には、コスチュームを`われた`{:class="block3looks"}にかえるようにするよ：

![ピニャータのスプライトアイコン](images/pinata-sprite.png)

```blocks3
when this sprite clicked
if <(たたいた数) < (10)> then
start sound [Boing v]
change [たたいた数 v] by (1)
+ if <(たたいた数)=(10)> then
switch costume to (われた v)

```

--- /task ---

--- task ---

**テスト：**プロジェクトをなん回か実行してみよう。 **ピニャータ**のスプライトが、「まるごと」のコスチュームからスタートし、`10 回たたいた`{:class="block3variables"}ときに、「われた」のコスチュームにかわることをチェックしてね。

![ピニャータが10回クリックされているアニメーション画像 10回の後われたコスチュームにかわる](images/break-pinata.gif)

--- /task ---

**ピニャータ** のスプライトがわれたとき、そのほかのスプライトにパーティーがはじまったことがつたわるようにします。

Scratchでは、`メッセージを送る`{:class="block3events"} ブロックをつかって、すべてのスプライトが**受け取る**ことができるようにメッセージを**送る**ことができます。

--- task ---

`イベント`{:class="block3events"}から`メッセージを送る`{:class="block3events"} ブロックを追加（ついか）しよう：

![ピニャータのスプライトアイコン](images/pinata-sprite.png)

```blocks3
when this sprite clicked
if <(たたいた数) < (10)> then
start sound [Boing v]
change [たたいた数 v] by (1)
if <(たたいた数)=(10)> then
switch costume to (われた v)
+ broadcast (message1 v)
```

`メッセージ１`{:class="block3events"} をクリックして、 **新しいメッセージ**をえらぶよ。 新しいメッセージの名前は`パーティー`{:class="block3events"}にしてね。

![「新しいメッセージ」が表示されている「メッセージを送る」ブロックのドロップダウンメニュー](images/new-message.png)

![「新しいメッセージ」ボックスがハイライトされ、「パーティー」という文字が入力されている新しいメッセージポップアップウィンドウ](images/party-message.png)

`メッセージを送る`{:class="block3events"} ブロックは、こんなかんじになるよ：

```blocks3
broadcast (パーティー v)
```

--- /task ---

--- save ---

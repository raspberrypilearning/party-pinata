## おやつをいれよう

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
ピニャータには、たくさんのおやつがつめられていて、われはじめると、おやつが出てきます。 このステップでは、色々な国のおやつが、たたくたびにピニャータから落ちてくるようにします。 どんなおやつを知っていますか？
</div>
<div>
![ピニャータが何回もたたかれるアニメーション画像。 毎回4つのおやつがランダムにえらばれて、ランダムな場所に落ちてゆっくり回る](images/spinning-treats.gif){:width="300px"}
</div>
</div>

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Scratchでは、<span style="color: #0faeb0">**コスチューム**</span> は、スプライトの見ためを変える画像です。 **グラフィックデザイナー**は、世界中にいるCode Clubのリーダーに、パーティーでどんなおやつが出るかを聞きました。 彼らがかいたおやつのコスチュームには、あなたがよく知っているのがあるかもしれませんねーまったく新しいおやつもありますよ。      
</p>

--- task ---

スプライトリストで**おやつ** をクリックし、**コスチューム** タブをクリックしてみましょう。

26こも、おやつのコスチュームがありますーぜんぶ使うことができますよ！

![おやつのコレクションとして特別に制作されたおやつ画像](images/treats.png)

--- /task ---

--- task ---

**コード** タブをクリックし、スクリプトを作って、プロジェクトをスタートしたときに、ピニャータの中におやつを`隠す`{:class="block3looks"}ようにしましょう：

![おやつのスプライトアイコン](images/treats-sprite.png)

```blocks3
when flag clicked
hide
go to x: (0) y: (100)
```

--- /task ---

ピニャータがたたかれるたびに、4つのおやつがとび出すようにします。 **おやつ** のスプライトの**クローンを作る**ことによって、たくさんのおやつを作成することができます。

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Scratchでの<span style="color: #0faeb0">**クローン**</span> は、スプライトのコピーです。 クローンは、オリジナルのスプライトと同じコード、コスチューム、音で動きます。      
</p>

--- task ---

**ピニャータ** のスプライトをクリックしましょう。

`繰り返す`{:class="block3control"}ループをいまあるコードにいれるよ。 `4`{:class="block3control"}に回数をかえて、`自分自身のクローンを作る`{:class="block3control"} ブロックを追加しよう。 ドロップダウンを使って`おやつ`{:class="block3control"} のスプライトを選択してね。

![ピニャータのスプライトアイコン](images/pinata-sprite.png)

```blocks3
when this sprite clicked
if <(たたいた数) < (10)> then
start sound [Boing v]
change [たたいた数 v] by (1)
+ repeat (4) // 4にかえる
create clone of (おやつ v) // おやつをえらぶ
end
if <(たたいた数)=(10)> then
switch costume to (われた v)
broadcast (パーティー v)
```

**ヒント：** スクリプトに新しいコードを追加するときには、まずコードエリアのあいている場所をつかって作り、そのあとスクリプトにドラッグします。

![スクリプトにドラッグする前にコード領域で繰り返しとクローンのブロックを組み合わせる](images/code-area.gif)
--- /task ---

--- task ---

**おやつ** のスプライトをクリックしよう。

`クローンされたとき`{:class="block3control"} のブロックで新しいスクリプトを作成するよ。

`見た目`{:class="block3looks"}から、新しいクローンの見ためをコントロールするためにブロックをいくつか追加しましょう：

![おやつのスプライトアイコン](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer // 最背面にかえる
switch costume to (Knafeh v)
```

--- /task ---

--- task ---

ピニャータがたたかれたとき、ランダムにおやつをとり出すことができます。 `乱数`{:class="block3operators"} の演算子（えんざんし）をつかって、`1`{:class="block3operators"} から `26`{:class="block3operators"} までのランダムなコスチュームでクローンが作られるようにしましょう：

![おやつのスプライトアイコン](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer 
+ switch costume to (pick random (1) to (26)) // 26にかえる
```

--- /task ---

--- task ---

ここまでで, **おやつ** のクローンが **ピニャータ** のうしろに出てくるようになったけど、まだピニャータからランダムなところへおちていくようになっていないね。

クローンされた**おやつ**のスプライトがランダムな場所へ `行く`{:class="block3motion"} ようにコードを追加しましょう：

![おやつのスプライトアイコン](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer
switch costume to (pick random (1) to (26))
+ glide (1) secs to (random position v) 
```

--- /task ---

--- task ---

**テスト：** プロジェクトを実行して、ピニャータをたたき、たたくたびに **おやつ** のクローンが4つ出てくることを確認してみよう。 コスチュームはランダムにえらばれ、おやつはランダムな場所に移動（いどう）します。

![ピニャータが3回たたかれるアニメーション画像 毎回ランダムに選ばれた4つのおやつがランダムな場所に落ちていく](images/four-treats.gif)

--- /task ---

--- task ---

**おやつ** のスプライトのクローンが 、ランダムな場所に着いたら`ずっと`{:class="block3control"} `回転する`{:class="block3motion"} ようにアニメーションを追加します。 アニメーションは、小さな動きを使うといいということをおぼていてね。だから角度を`1`{:class="block3motion"}にしておくよ。

![おやつのスプライトアイコン](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer
switch costume to (pick random (1) to (26)
glide (1) secs to (random position v) 
+ forever
turn right (1) degrees
```

--- /task ---

--- task ---

**テスト：** プロジェクトをもういちど実行して、**おやつ** のクローンが回転することをチェックしてみよう。

![ピニャータが何回もたたかれるアニメーション画像 毎回4つのおやつがランダムに選ばれてランダムな場所に落ちた後、ゆっくり回る](images/spinning-treats.gif)

--- /task ---

--- save ---

## スティックをつかってみましょう

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
ピニャータは、ふつう、カラフルな紙がたくさんついた木やボール紙で作ったスティックでたたきます。 このステップでは、コードを追加してピニャータスティックをコントロールし、ピニャータがわれたときに音楽がながれつづけるようにします。 
</div>
<div>
![スティックのスプライトがマウスポインタを追いかけているアニメーション画像](images/follow-stick.gif){:width="300px"}
</div>
</div>

--- task ---

スプライトリストにある **スティック** のスプライトをクリックしよう。 スティックがいつも他のスプライトの前でマウスポインター(もしくはタブレット画面をなぞる指) をおいかけるようにコードを追加（ついか）するよ。

`どこかの場所へ行く`{:class="block3motion"}ブロックをつかうのだけど、ドロップダウンメニューで`マウスポインター`{:class="block3motion"} にかえてね：

![スティックのスプライトアイコン](images/stick-sprite.png)

```blocks3
when flag clicked
forever
go to [front v] layer
go to (mouse-pointer v) // マウスのポインターにかえる
```

--- /task ---

--- task ---

**テスト:** プロジェクトを実行し **スティック**のスプライトが、カーソルや画面をなぞる指をおいかけるか確認してみよう。

![スティックのスプライトがマウスポインタを追いかけているアニメーション画像](images/follow-stick.gif)

--- /task ---

Scratchには、声や動物の鳴き声など、100以上のいろいろな音が用意されています。

また、Scratch では**ループ音**を `ずっと`{:class="block3control"} や `繰り返す`{:class="block3control"} ループを使用することで、ずっとならしつづけることができます。

--- task ---

**音** タブを選択して、 **音を選ぶ** ボタンをクリックしてみよう。

![音のポップアップメニューが表示された音を選ぶアイコン 選択すると、音をえらぶのアイコンが緑の円に白いスピーカーになる](images/sound-icon.png)

--- /task ---

--- task ---

**音を選ぶ**一覧画面から、 **ループ** カテゴリをえらぶよ。

![「ループ」のカテゴリがオレンジ色にハイライトされている音の一覧画面 そのほかのカテゴリは青く表示](images/loops-category.png)

--- /task ---

--- task ---

**選ぶ：** **再生** ボタンの上にカーソルをおくと、ループ音を聞けるよ。 クリックして好きな音を追加してね。

![右上の再生ボタンがハイライトされている「Hip hop」音](images/play-icon.png)

その音が、音のリストに表示されるよ。

![音タブの音リストに表示されている「Hip hop」音](images/added-sound.png)

--- /task ---

--- task ---

**コード**タブをクリック、新しいスクリプトを作成して、`パーティー`{:class="block3events"} メッセージをうけとったときに、 `ずっと`{:class="block3control"}音が鳴るようにするよ：

![スティックのスプライトアイコン.](images/stick-sprite.png)

```blocks3
when I receive [パーティー v]
forever
play sound [Hip Hop v] until done // すきな音をえらぶ
```

--- /task ---

--- task ---

**テスト：** プロジェクトを実行し、ピニャータを10回たたいて、ループ音が流れることを確認してみよう。

--- /task ---

--- save ---

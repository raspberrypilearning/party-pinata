## プロジェクトをアップグレードしましょう

時間があるなら、プロジェクトをアップグレードできます。 あなたはすでに何を追加するかについてのアイデアを持っているかもしれません！

こんなことができます：

+ 動きや、見た目、音のブロックを追加して、メッセージやおやつのアニメーションをもっと複雑にする
+ 好きなおやつの画像を見つけて、**おやつ** のスプライトに追加する
+ ピニャータをたたいたときに出てくるおやつの数を増やす
+ ピニャータを壊すために必要なたたく回数を変えることで、プロジェクトの難易度を変える

--- task ---
### 試してみる
<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 175px; flex-grow: 1">  
背景にもコードを追加できることをご存知ですか？

ピニャータが壊れると、背景はどうなりますか？ どのブロックがこの効果を生み出しますか？ 

[コードを参照](https://scratch.mit.edu/projects/653771814/){:target="_blank"}

</div>
<div class="scratch-preview" style="margin-left: 15px;">
  <iframe allowtransparency="true" width="485" height="402" src="https://scratch.mit.edu/projects/embed/653771814/?autostart=false" frameborder="0"></iframe>
</div>
</div>
--- /task ---

--- task ---

メッセージが定位置に辿り着いたときに、`ずっと`{:class="block3control"} メッセージをアニメーション化しておくコードを追加することができます。 `大きさを変える`{:class="block3looks"} や`色の効果を変える`{:class="block3looks"} ブロックを使い、パーティービートに合わせてメッセージが動いているように見せることもできます：

![メッセージのスプライト](images/message-sprite.png)

```blocks3
when I receive [party v]
show
repeat (20)
change size by (5)
change y by (-10)
end
+ forever
change size by (20) // Positive number to grow
change [color v] effect by (25) // Change colour
wait (0.5) seconds // Try different numbers to match your music
change size by (-20) // Negative number to shrink
```

[コードを参照](https://scratch.mit.edu/projects/656332454/){:target="_blank"}

<div class="scratch-preview" style="margin-left: 15px;">
  <iframe allowtransparency="true" width="485" height="402" src="https://scratch.mit.edu/projects/embed/656332454/?autostart=false" frameborder="0"></iframe>
</div>

--- /task ---

--- collapse ---

---
title: 完成したプロジェクト
---

[完成したプロジェクトはこちら](https://scratch.mit.edu/projects/649873783/){:target="_blank"}で確認できます。

--- /collapse ---

--- task ---

### プロジェクトを保存する

すでにプロジェクトを私たちと共有している場合は、変更を保存するだけで、すばらしいアップグレードが反映されます。

他の人が見ることができるよう、あなたのプロジェクトを ['Party piñata — Community' Scratchコミュニティ](https://scratch.mit.edu/studios/31111242){:target="_blank"}に送るには、 [このフォーム](https://form.raspberrypi.org/f/community-project-submissions){:target="_blank"}を使ってください。

--- /task ---

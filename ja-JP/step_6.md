## メッセージを作りましょう

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
このステップでは、メッセージを作成し、モーション効果とカラー効果を使ってアニメーション化します。 
</div>
<div>
![メッセージが舞い落ちながら、最終的な場所にたどり着くまでに大きさや色が変わっていくアニメーション画像](images/falling-message.gif){:width="300px"}
</div>
</div>

Code Clubに送るバーズデーカードに、どのようなことを書きますか？ 例えば:
+ Code Clubの好きなところ
+ 素晴らしいCode Clubのリーダーについてのメッセージ
+ あなたのコーディングスキルをどのように伸ばしたいかについて

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
最初のCode Clubのプロジェクトは英語で書かれましたが、一年のうちにブラジル語、ポルトガル語、オランダ語、ドイツ語、ノルウェー語、ウクライナ語に翻訳されました。 フランス語、ギリシャ語、スペイン語の翻訳がすぐそれに続き、いまやCode Clubのプロジェクトは <span style="color: #0faeb0">**28言語**</span>に翻訳されています。 素晴らしい翻訳コミュニティーに感謝します。

![さまざまな言語でのハッピーバースデーのイメージ](images/birthday-languages.png)
</p>

--- task ---

スプライトのリストから**メッセージ** のスプライトをクリックし、**コスチューム** タブを選びます。

このコスチュームには「ハッピーバースデイCode Club」と書かれています。 Double click (or tap and hold on a tablet) on the text to select the text editing tool.

![The costume editor with Text tool selected and text highlighted.](images/text-edit.png)

--- /task ---

--- task ---

You can now type your new Code Club birthday message. Press **Enter** on your keyboard to start a new line.

**Tip:** Don't worry if your message is a bit too big for the box as you can resize it later.

![The text editor showing a new message has been typed in place of the old message.](images/new-text.png)

--- /task ---

--- task ---

**Choose:** Click on the **Fill** icon to open the colour drop-down menu. Move the fill sliders to the left or right to select your favourite colour.

![The Fill drop-down menu with sliders for colour, saturation, and brightness. The message has changed from green to purple.](images/font-colour.png)

--- /task ---

--- task ---

**Choose:** Click on the **Font** tool and a drop-down list of fonts will appear. The 'Pixel' font is selected in the starter project, but you can use any of the fonts available.

![The Font drop-down menu showing a choice of nine different fonts. The 'Marker' font has been selected.](images/font-type.png)

--- /task ---

--- task ---

Click on the **Select** tool and eight circles will appear around your message. Use these circles to resize your message by clicking on them and dragging them within the white box.

![The Select tool is highlighted and the message has small circles in each corner and at the central vertical and horizontal borer points so that it can be resized in multiple directions.](images/resize-message.png)

--- /task ---

Your message is ready, now you can add code to hide your message inside the piñata and make your message fall from the piñata after the tenth hit.

--- task ---

Click on the **Code** tab then create a script to `hide`{:class="block3looks"} the message in the piñata when your project starts:

![The Message sprite icon.](images/message-sprite.png)

```blocks3
when flag clicked
hide
set size to (10) % // Change to 10 to start small
go to x: (0) y: (100) // Inside the piñata
```

--- /task ---

--- task ---

Create a new script to start when the `party`{:class="block3events"} message has been received.

Add a `repeat`{:class="block3control"} loop to animate the message. The message will `change size`{:class="block3looks"} to grow and `change y`{:class="block3motion"} position to fall as it animates:

![The Message sprite icon.](images/message-sprite.png)

```blocks3
when I receive [party v]
show
repeat (20) // Change to 20
change size by (5) // Change to 5
change y by (-10) // Change to -10
```

--- /task ---

--- task ---

**Test:** Run your project. Hit the piñata ten times to see the message fall.

![An animated image showing the pinata being hit ten times. Treats appear after each hit and on the tenth hit the pinata breaks and the message falls to the bottom of the screen. It gets bigger as it falls.](images/falling-message.gif)

--- /task ---

--- save ---

# mod.assist.gtav

リンク：https://aikk910.github.io/mod.assist.gtav/

このツールはオープンワールドゲームであるGTA5のMODに関するトラブルを解決するお手伝いをするために作られました。
ChatGPTのような回答をしていますが、回答にAIは全く使用していません。HTMLに書き込まれていることを表示させてるだけです。

まだβ版であり、質問の種類や回答の内容も全くありませんが、私が暇なときに書き足していこうかなと思います。

# 【使い方】
気になる項目を押すだけで回答が表示されます。回答中は他のボタンを押すことができません。
リセットボタンですべて消えます。

ページの下にある【Mode:〇〇】を押すと違った感じのページに切り替わります。機能は下を見てください。

# 【機能】
まずリンクを押して最初に出てくるのは、単に1つの質問に回答するだけのものです。

下の「Mode：Resolved/unresolved」を押すとページが切り替わり、同じような画面が表示されます。ここではMODに関する問題を1つずつ確認していきながら解決していくようなものです。
その回答で解決したら👍を押し、それでも解決しなければ👎を押してください。👍を押すと回答が終了し、👎を押すと新たな回答が表示されます。
情報不足によって途中で解決法が表示されなくなることがありますが、分かり次第追加していこうかなと思ってはいます。
検索欄はそのままです。

# HTMLに追加する（編集する）際のコード一覧

・index.html

_グループを追加する時_

`<div class="question-group">
      <div class="group-header" onclick="toggleGroup(this)">グループ名</div>
      <div class="group-content">
        <button class="question-button" onclick="generateResponse('質問1')">質問2</button>
        <button class="question-button" onclick="generateResponse('質問2')">質問2</button>
      </div>
    </div>`


_回答を追加する時_

`'質問1': '回答1',
'質問2': '回答2',`
※必ず1行で書き、開業する場合は \n と入れることで改行されます。


_回答後に画像ファイルを表示させる時_

`'質問1': 〇〇.png,
'質問2': 〇〇.gif,`
※何も表示させない場合、nullと設定する　（例'質問1': null,


・index2.xml


_グループを追加する時_

`<div class="question-group">
      <div class="group-header" onclick="toggleGroup(this)">グループ1</div>
      <div class="group-content">
        <button class="question-button" onclick="generateResponse('質問1')">質問1</button>
        <button class="question-button" onclick="generateResponse('質問2')">質問2</button>
      </div>
    </div>`


_回答を追加する時_

`'質問1': ['回答例1'],
'質問2': ['回答例2'],`

例
`'ゲームが起動しない': [
      'PCを再起動してみてください。',
      'それでも解決しない場合、ゲームファイルの整合性を確認してください。',
      'まだ解決しない場合、最新のグラフィックドライバをインストールしてください。',
    ],`


 _回答後に画像ファイルを表示する時_

 `'質問1': 〇〇.png,
 '質問2': null,`


 

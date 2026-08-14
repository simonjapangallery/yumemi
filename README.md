# 夢み中ギャラリー 移行プロジェクト 作業記録
（2026年8月13日〜14日）

## 今日やったこと

1. Wixに埋め込んでいた「夢み中」オンラインギャラリー（23作品）を、Wixから独立させてGitHub Pagesで公開する形に移行した
2. QRコード用に、特定の作品だけを直接開けるURL機能（`?piece=作品キー`）をコードに追加した
3. GitHubアカウントを作成し、リポジトリ「yumemi」を作成
4. 23作品×3枚＝69枚の画像をWixからダウンロード・リネームし、GitHub Desktop経由でアップロード
5. GitHub Pagesを有効化し、公開URLを発行・動作確認済み

## 覚えておくべきこと

### 公開URL
**https://simonjapangallery.github.io/yumemi/**

### QRコード用の個別URL（作品キー対応表）

| 作品名 | キー | URL |
|---|---|---|
| ティンカーベル | green | ?piece=green |
| 薄幸 | glass | ?piece=glass |
| 付喪神 | face | ?piece=face |
| 星へ | comet | ?piece=comet |
| 発酵 | ferment | ?piece=ferment |
| フリーホール | freehole | ?piece=freehole |
| 走馬灯 | illumination | ?piece=illumination |
| 白虹 | byakko | ?piece=byakko |
| 二つの月 | twomoons | ?piece=twomoons |
| 夏の夜 | summernight | ?piece=summernight |
| 生命の樹 | treeoflife | ?piece=treeoflife |
| タイムカプセル | timecapsule | ?piece=timecapsule |
| もし | whatif | ?piece=whatif |
| 薄光 | faintlight | ?piece=faintlight |
| 琴線 | kotosen | ?piece=kotosen |
| ミルキーウェイ | milkyway | ?piece=milkyway |
| 幻影 | phantom | ?piece=phantom |
| eyes | eyes | ?piece=eyes |
| 古い鏡 | oldmirror | ?piece=oldmirror |
| 白カビと黒カビ | mold | ?piece=mold |
| アリス | alice | ?piece=alice |
| ネオン | neon | ?piece=neon |
| 膜 | membrane | ?piece=membrane |

各行の「URL」の末尾を `https://simonjapangallery.github.io/yumemi/` の後ろに付ければ完成（例：`https://simonjapangallery.github.io/yumemi/?piece=byakko`）。CanvaのQRコード生成機能にこのURLを入れて作品ごとにQRを作る。

### アカウント・ツール関連
- GitHubアカウント：simonjapangallery（今回新規作成）
- リポジトリ名：yumemi
- ローカル保存先（パソコン内）：`/Users/kanaetsukahara/Documents/GitHub/yumemi`
- GitHub Desktopをインストール済み（今後の更新作業もこのアプリを使う）

### Wixとの関係
- Wix自体は今回解約していない（次回更新は2027年7月、急ぎではない）
- ギャラリー機能だけをWixから切り離せたので、「Wixを続けるかCanvaに戻すか」の判断とは無関係に、ギャラリーの更新・成長を続けられる状態になった

## 新しい作品を追加するときの手順（次回用）

1. 作品キーを決める（例：新作なら"kagerou"など、英数字で）
2. 写真3枚を「キー_1.jpg」「キー_2.jpg」「キー_3.jpg」の名前で用意
3. コード内の `IMAGE_KEYS` 配列にそのキーを追加
4. コード内の `dreams` 配列に、タイトル・日本語ストーリー・英語ストーリー・画像3枚をひとつのオブジェクトとして追加
5. 画像を `images` フォルダに入れる
6. GitHub Desktopで Commit → Push
7. 公開ページで表示確認
8. QRコード用URL（`?piece=キー`）をCanvaでQR化し、実物の横に設置

※③④のコード編集は、今回のファイルの中身を実際に見ながら行う必要があるため、Claudeとの会話で進めるのが安全（他のAIに頼む場合は、コードの中身を都度渡すこと）

## このファイルの保存場所について

このメモ自体は、**GitHubの `yumemi` リポジトリの中に `README.md` として一緒に入れておく**のが一番迷子にならない方法です。理由は、コードと同じ場所にあれば、後で見返すときに「あのメモどこだっけ」とならずに済むためです。

具体的には：
1. このファイルをダウンロード
2. ファイル名を `README.md` に変更（または好きな名前のままでもOK）
3. GitHub Desktopで yumemi フォルダの中にこのファイルを入れる
4. Commit → Push

パソコンのローカルにも念のため、今使っている「作品画像」フォルダなど分かりやすい場所にコピーを置いておくと二重の安心になります。

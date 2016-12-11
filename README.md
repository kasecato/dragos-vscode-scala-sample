## IDE vs. テキスト エディター

　時は 1990 年 1 月，HTTP (1991) も HTML (1993) も標準化の前夜，Web ブラウザ (1993) すら存在しないその時代に，日本最初のインターネット コミュニティである [fj](https://ja.wikipedia.org/wiki/Fj_(%E3%83%8B%E3%83%A5%E3%83%BC%E3%82%B9%E3%82%B0%E3%83%AB%E3%83%BC%E3%83%97)) にて「Emacs」派 VS 「vi」派のエディター論争が勃発しました。エディター論争は vi 派の東工大 [mohta](http://www.geocities.co.jp/Bookend-Soseki/3185/Jokes/articles/420-C.html) 氏による Emacs 批判投稿で溢れ，最終的に mohta 氏がグループ (fj.editor.misc) ごと消去するという「rmgroup 事件」にまで発展したそうです。

　あれから 26 年，HTTP は [HTTP/2](http://summerwind.jp/docs/rfc7540/) となり，HTML は [HTML5.1](https://momdo.github.io/html51/Overview.html) にまでも成長し，Web ブラウザは [2 度にわたる大戦](https://ja.wikipedia.org/wiki/%E3%83%96%E3%83%A9%E3%82%A6%E3%82%B6%E6%88%A6%E4%BA%89) を経て戦後処理という十字架（クロスブラウザのクロスに意味を掛け(ry，プログレッシブ エンハンスメント）を開発者に背負わせました。

　テキスト エディターの進化も他ではありません。日々複雑化するソフトウェア開発とツール群の学習負担に悩まされた (良い意味で) レイジーな開発者は，様々な言語の生態系を統合したリッチな GUI 環境の提供が~~ビジネスになる~~開発者の生産性を高めることに気づき，IDE (Integrated Development Environment: 統合開発環境) という新しい開発ツールを開発しました（開発を開発というトートロジー（恒真式）ジョーク…）。テキスト エディターは IDE の一部機能となる時代が到来したのです。そして 21 世紀， IDE を使った開発経験しかない IDE ネイティブ世代が誕生したのです。IDE ネイティブの登場は時代の必然だったと言えるでしょう。

　IDE と テキスト エディターについて Java Champion の Heinz Kabutz [@heinzkabutz](https://twitter.com/heinzkabutz)(ハインツ・カブーズ) 博士は次のように書きました。筆者も非常に共感するところが多いです。（が，筆者は Emacs も Vim も学生時代しか使っていませんw）

>私がはじめてUNIXマシンでCのプログラミングをした時は、viエディタを使う必要があり、その使い方を習得するのにかなりの時間を要しました。viエディタの学習曲線は、かなりの急勾配と言えるでしょう。いったんコツがわかると急激に理解が進むのですが、最初の段階では非常に苦労をするのです。しかし苦労して身につけた技術は、その後ずっと役立つてくれているので、苦労は十分報われたと言えます。実際この原稿を書くのにもviを使っています。反対にIDEの学習曲線は非常に緩やかです。苦労せずに使い始められるのですが、その後はなかなか上達しないことが多いのです。長い間、基本的な使い方しか知らないという状態が続いてしまいます。 - Heinz Kabutz

　※Heinz Kabutz 博士は IDE のファンです。引用箇所に筆者のバイアスがある可能性があります。


## テキスト エディターと開発者

　プログラマは 1 日最低でも 8 時間以上はエディターと付き合わなければならないのです。これは家族以上の付き合いです。家族であるエディターに不満の一つや二つ持つことは当然のことです。しかし開発者がエディターの不満を解消するための変更をしたいと思ったらそれはビッグ プロジェクトのように感じるでしょう。Emacs の開発について，かつて [Eric Raymond](https://ja.wikipedia.org/wiki/%E3%82%A8%E3%83%AA%E3%83%83%E3%82%AF%E3%83%BB%E3%83%AC%E3%82%A4%E3%83%A2%E3%83%B3%E3%83%89) (エリック・レイモンド) は『[伽藍とバザール](http://cruel.org/freeware/cathedral.html)』で次のように例えました。

>一番だいじなソフト（OS や、Emacs みたいな本当に大規模なツール）は伽藍のように組み立てられなきゃダメで、一人のウィザードか魔術師の小集団が、まったく孤立して慎重に組み立てあげるべきもので、完成するまでベータ版も出さないようでなくちゃダメだと思っていた。 - Eric Raymond

　エディターを開発するということは，一人のウィザードが伽藍のように組み立てるものだとされていた時代を変えたのが，Linux を開発した [Linus Torvalds](https://ja.wikipedia.org/wiki/%E3%83%AA%E3%83%BC%E3%83%8A%E3%82%B9%E3%83%BB%E3%83%88%E3%83%BC%E3%83%90%E3%83%AB%E3%82%BA) (リーナス・トーバルズ) でした。

>だからリーヌス・トーヴァルズの開発スタイル――はやめにしょっちゅうリリース、任せられるものはなんでも任して、乱交まがいになんでもオープンにする――には まったく驚かされた。静かで荘厳な伽藍づくりなんかない―― Linux コミュニティはむしろ、いろんな作業やアプローチが渦を巻く、でかい騒がしいバザールに似ているみたいだった（これをまさに象徴しているのが Linux のアーカイブサイトで、ここはどこのだれからでもソフトを受け入れてしまう）。そしてそこから一貫した安定なシステムが出てくる なんて、奇跡がいくつも続かなければ不可能に思えた。 - Eric Raymond


## 言語サーバー プロトコル

　Rosetta Code には [351](https://www.rosettacode.org/wiki/Hello_world/Text) ものプログラム言語で Hello World が刻まれています。プログラミング言語が 351 以上もある 21 世紀に，言語サポート機能を様々なプラットフォームとエディターでサポート・保守し続けることは後世に多大な技術的負債を残すことになるでしょう。

　そこで，2016 年に Microsoft の Dirk Bäumer (https://github.com/dbaeumer) 博士は[言語サーバ プロトコル (Language Server Protocol)](https://github.com/Microsoft/language-server-protocol) を GitHub で公開しました。

　言語サーバ プロトコルとは，入力補完や構文エラーを検出する言語サーバ側と，ソースコード上に入力補完や構文エラーを表示するテキスト エディター (クライアント) 側とのプロトコルを標準化したものです。つまり言語サーバ プロトコルを一度実装してしまえば，どのエディターでも言語サポート機能が使えるようになる ~~Write once, run anywhere~~ という構想です。

[!Language Server Protocol](img/interaction-diagram.png)
　
　先の大戦を経験した Web 界隈の開発者は「また Microsoft 独自の仕様か」と眉をひそめるでしょうが，すでに [Go，Rust，Scala など 19 の言語がすでに実装](https://github.com/Microsoft/language-server-protocol/wiki/Protocol-Implementations)されています。IDE でも Red Hat が Eclipse Che に採用しているとおり，実績がすでにあります。筆者の邪推ですが，VS Code の開発者には GoF の 1 人で，Eclipse と JUnit を開発したあの [Erich Gamma](https://ja.wikipedia.org/wiki/%E3%82%A8%E3%83%BC%E3%83%AA%E3%83%92%E3%83%BB%E3%82%AC%E3%83%B3%E3%83%9E) (エリック・ガンマ) 博士がいます。Eclipse Che が 言語サーバー プロトコルを支持したのは，何かヨーロッパのコミュニティのつながりがあるのかもしれません。


## モダンな言語サポートの今

　プログラミング言語 Scala はオブジェクト指向言語 (OOP: Object-Oriented Programming) と関数型言語 (FP: Functinal Programming) の特徴を合せ持つ代表的なモダンなハイブリッド言語の一つです。IDE が全盛期の 21 世紀以降に登場したモダンな言語はテキスト エディターでも使うことができるのでしょうか？答えは ~~Yes, we can~~ YES です。Scala 言語は [Emacs](https://www.gnu.org/software/emacs/), [Vim](http://www.vim.org/), [Atom](https://atom.io/) や [Sublime](https://www.sublimetext.com/)　といった多くの開発者と環境に鍛えられた素晴らしい歴史的でモダンなテキスト エディターの選択肢があります。もちろん [Scala IDE for Eclipse](http://scala-ide.org/) や [IntelliJ IDEA](https://www.jetbrains.com/idea/) といった素晴らしい IDE もあり，IDE を Vim ライク，Emacs ライクに操作することもできます。

　しかしよく考えると，Scala のベースとなっている Java (JDK 1.0) がリリースされたのは 1996 年 1 月 23 日のことです。1996 年当時の開発者はどのようにして Java を開発していたのでしょうか？入力補完やコンパイルはどのようにしていたのでしょうか？~~それは Visual J++ を使っていたのです。~~


## Visual Studio Code

　Visual Studio (VS) といえば，Microsoft が Windows で展開する IDE が最も有名で，特に Web アプリケーションの開発者にとっては多くの文脈で「VS = Windows にロックインされたクローズドな Web 開発環境」というネガティブな意味を持ってたように筆者は感じていました。Apple が macOS でしか Xcode が使えないように，Microsoft も Windows でしか VS を使うことができないのは，OS ベンダーとして (当時は) 当然の戦略だった思います。

　しかしご存知の通り，Microsoft は今や Linux Foundation のメンバーであり，[GitHub で最も OSS へのコミッターが多い組織](https://gist.github.com/alysonla/e14c01ec7a0d2823e7317f7b58b22926#file-orgs-most-contributors-sql)にまで変わりました。

　そして 2015 年 4 月 29 日，macOS，Linux，Windows のマルチ・プラットフォームで動作するテキスト エディター [Visual Studio Code](https://code.visualstudio.com/) (VS Code) (Version 1.0.0) をリリースします。VS Code は GitHub 社が開発した Atom と同じ Electron をベースとしたテキスト エディターですが，エディター部分は Eric Gamma 博士が開発した Monaco (Visual Studio Online) であり，[Rebuid.fm #90](https://rebuild.fm/90/) で Tatsuhiko Miyagawa 氏が評価したとおり「ネイティブ感が凄い」です。


## ENSIME

　テキスト エディター向けの Scala 言語サポート サーバーに [ENSIME](https://ensime.github.io/) があります。ENSIME は scalac と javac の抽象構文木 (AST: Abstract Syntax Tree) を理解します。[Emacs，Vim，Atom，Sublime をサポート](https://ensime.github.io/editors/)しており，Emacs についてはデバッガー，REPL (Read-Eval-Print Loop) や Java までもサポートしますが，残念ながら[ENSIME 本家の VS Code は開発中](https://github.com/ensime/ensime-vscode)です。

　筆者は本家 ENSIME VS Code のニワカ コミッターであり，[入力補完機能の追加に挑戦](https://github.com/hedefalk/ensime-vscode/pull/1)しましたが，ENSIME 言語サーバー プロトコルと VS Code エディターのクライアントの[方言問題](http://stackoverflow.com/questions/39149525/how-do-i-best-resolve-an-offset-position-into-a-line-col-position-in-a-vscode-d)により，議論の結果 ENSIME サーバー側の機能追加でカバーしようという結論で頓挫しています。

　
## Scala language server for VS Code

　ENSIME 自体は独自の言語サーバー プロトコルであり，Microsoft が提唱するすべての言語サーバーの仕様を共通化するプロトコルではありません。ENSIME の言語サーバープロトコルを，共通の言語サーバー プロトコルにラッピングしたプロジェクトが「[Scala langage server for VS Code](https://github.com/dragos/dragos-vscode-scala)」(プロジェクト名は dragos-vscode-scala) です。筆者も本拡張機能のコミッターで sbt コマンド サポートを Erich Gamma 博士の [vscode-npm-scripts](https://github.com/Microsoft/vscode-npm-scripts) を~~パクって~~参考にして追加しています。

　開発者の [Iulian Dragos](http://iulidragos.com/about/) 博士はスイス連邦工科大学ローザンヌ校 (EPFL) で Scala の父である Martin Odersky 指導教官の元 PhD を取得し，その後 Scala IDE の開発に従事しています。Scala と Scala IDE の開発者が VS Code の Scala 言語サポート拡張機能の開発に着手したのです！

　VS Code の Scala 言語サポートは今回紹介する「[Dragos 版](https://github.com/dragos/dragos-vscode-scala)」とは別に「[ENSIME 本家版](https://github.com/ensime/ensime-vscode)」が存在します。両者の違いは，Dragos 版が言語サーバー プロトコルに準拠しており，ENSIME 本家版は準拠していないということです。ENSIME 本家版は ENSIME Atom 版の開発者 [Viktor Hedefalk](https://github.com/hedefalk) 氏によって支えられており，Atom の Coffee Script の構成で移植しようとしているため，言語サーバー プロトコルには準拠していません。両者の開発状況ですが，両者ともに拡張機能を [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/) で正式公開するには至っていません (11/26 2016 現在)。

　本稿で紹介する VS Code で Scala をサポートする方法は非常に面倒で，言語サポート機能も限定的で，動作不具合もあります。ただ，この面倒な環境を作ってしまえば今日から Scala 言語サポート機能の開発者になれるのです。


## Scala 環境構築

ツール    | バージョン  | 説明
---------|-----------|------
[JRE](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html)      | >= 8u111  | Java 言語サポート
[sbt](http://www.scala-sbt.org/index.html)      | >= 0.13   | ビルド ツール
[ENSIME](https://ensime.github.io/build_tools/sbt/)   | >= 1.11.3 | Scala 言語サーバー
[VS Code](https://code.visualstudio.com/)  | >= 1.7.2  | テキスト エディター 
[Git](https://git-scm.com/)  | >= 2.10.2  | バージョン コントロール システム
[Scala language server for VS Code](https://github.com/dragos/dragos-vscode-scala) | >= 0.0.4 | VS Code Scala 言語サポート拡張機能
[Node.js](https://nodejs.org/ja/) | >= 6.9.1 | VS Code 拡張機能ビルド
[vsce](https://code.visualstudio.com/docs/tools/vscecli) | >= 1.17.0 | VS Code 拡張機能公開 ツール


* JRE をインストーラからインストールしてください
  * [Java SE Runtime Environment 8](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html)

* VS Code をインストーラからインストールしてください
  * [Visual Studio Code](https://code.visualstudio.com/)

* Git をインストーラからインストールしてください
  * [Git](https://git-scm.com/)

* Scala language server for VS Code のソースコードを Git で clone してください

```bash
cd ~
mkdir VSCode
cd VSCode
git clone https://github.com/dragos/dragos-vscode-scala.git 
```

* sbt を brew コマンドでインストールしてください

```bash
brew install sbt
```

* ENSIME を sbt の設定ファイルに記述してください
  * `~/.sbt/0.13/plugins/plugins.sbt` ファイルに以下を追加します

```sbt
addSbtPlugin("org.ensime" % "sbt-ensime" % "1.12.4")
addSbtPlugin("io.get-coursier" % "sbt-coursier" % "1.0.0-M15")
```

* Scala 言語サーバーを sbt でビルドしてください

```bash
cd ~/VSCode/dragos-vscode-scala
sbt publishExtension
```
* Node.js をインストーラからインストールしてください
  * [Node.js](https://nodejs.org/ja/)

* npm で拡張機能のパッケージを取得してください

```bash
cd scala
npm install
```

* npm スクリプトで拡張機能をビルドしてください

```bash
npm run compile
```

* npm で vsce をインストールしてください
```bash
npm install -g vsce
```

* vsce で拡張機能をパッケージ化 (VSIX ファイル生成) してください
```bash
vsce package
```

* VS Code に VSIX をインストールしてください
  * `Cmd+Shift+P` (コマンド パレットを開きます)
  * `Extensions: Install from VSIX...`
  * `ensime-scala-0.0.4.vsix` ファイルを選択してください


## はじめてのScala プロジェクト

```bash
.
├── .ensime
├── .ensime_cache
├── src
│   ├── main
│   │   └── scala
│   │       └── StarWars.scala
│   └── test
│       └── scala
└── build.sbt
```

ツール           | 説明
----------------|-----------
.ensime         | build.sbt を ENSIME 用に変換した設定ファイルです。`sbt ensimeConfig` コマンドで出力します 
build.sbt       | プロジェクトのビルド設定を記述します
StarWars.scala  | ソースコードです


* Scala の開発プロジェクト `build.sbt` を作成します
```sbt
name := "starwars"
version := "1.0"
scalaVersion in ThisBuild := "2.12.0"
```

* .ensime ファイルを作成します

```bash
sbt ensimeConfig
```

* Scala で Hello Yoda を書きます

```scala
object StarWars extends App {
  println("Not if anything to say about it I have");
}
```

* 実行します（コンパイルも実行されます）

```bash
sbt run
Not if anything to say about it I have
```


## VS Code Scala まとめ

* Scala と Scala IDE の開発者である Iulian Dragos 博士が開発中です
* VS Code Market Place ではまだ未公開のため，ソースコードからビルドする必要があります
* Microsoft は言語サーバーの標準化を推進しています
* 言語サーバー プロトコルはすでに [Go, Rust, Scala](https://github.com/Microsoft/language-server-protocol/wiki/Protocol-Implementations) などイケてる言語でも実績があります
* 誰でも言語サポート機能を開発できる時代が来ました！


## 参考ノート

* ばるぼら,『教科書には載らないニッポンのインターネットの歴史教科書』, p.26
* Heinz Kabutz, 「IDEを知る」, http://プログラマが知るべき97のこと.com/%E3%82%A8%E3%83%83%E3%82%BB%E3%82%A4/IDE%E3%82%92%E7%9F%A5%E3%82%8B
* Microsoft GitHub, "Language Server Protocol", https://github.com/Microsoft/language-server-protocol
* ENSIME, https://ensime.github.io/
* Dragos, "About", http://iulidragos.com/about/


---
title: "GitHub 認定資格 GAになったので GitHub Actions Certificateを取得してみた。"
emoji: "🐙"
type: "idea" # tech: 技術記事 / idea: アイデア
topics: ["github", "CI", "Certifications"]
published: false
---

# GitHub Certificationsとは

![cert](/images/certificate.png)

2024年1月8日にポストされたGitHubの公式ブログの記事に ["GitHub Certifications are generally available"](https://github.blog/2024-01-08-github-certifications-are-generally-available/)という題名で以下４つの資格が一般公開されたことが報告されました。

記事によるとGitHubは、GitHub Foundation、GitHub Actions、GitHub Advanced Security、およびGitHub Administrationに関する4つの新しい認定プログラムを開始しました。これらの認定は、技術者がGitHubを使用して開発プロセスを改善するための知識と技術を証明する手段を提供します。
各資格は、GitHubの使用方法に関する包括的な理解を深めることを目的としており、詳細な学習パスと試験を通じて専門知識を評価するそうです。

# GitHub Actions Certification取得の動機

一言でいうと何となくです。今年(2024年)も始まったばかりで、
何となく充実した１年にするために、申込みをしました。
また、仕事でもGitHubは利用していますし、Application Developerとして、Fundationはなんか基本今更わかっているという資格をもらってもあまり自慢できなさそうと思い、
一番利用頻度が高いGitHub Actionsにしようと考えました。

私がこの資格を取得したタイミングで、この試験のための学習コンテンツや試験そのものに対する日本語のサポートはありませんでしたが、
せっかくバイリンガルだし、日本語がサポートされるまでに一足先にとってみるのもいいかもしれないとも思いました。

もし取得を考えられている方にこの記事が目に止まり少しでも参考になれば幸いです。

# シラバス

まずは、[このレポジトリ](https://github.com/LadyKerr/github-certification-guide?tab=readme-ov-file)を見ると全て認定資格に関するカリキュラムを参照することができます。
詳しい内容はここでは省略しますが、大きなくくりで以下のような分類で試験が構成されます。

```
Domain 1: Author and maintain workflows
Domain 2: Consume workflows
Domain 3: Author and maintain actions
Domain 4: Manage GitHub Actions for the enterprise
```

1, 2では基本的にRepositoryにGitHub Actionsを利用してworkflowを作成して実際に走らせるまでの基本的な知識を問います。
3では、どのように自分のアイディアをもとに作成したAcitonを展開するか、
4では、どちらかというとGitHubの管理者目線でGitHub Actionsに関する機能の制限やそれらに関わる設定の可否、方法を問います。
いつも使ってるからそんなに新たに学ぶこと無いかなと思っていましたが、案外しらない構文や機能、制約がたくさんあり、
実用的に役にたつ勉強となりました。
特に、いつもCI/CD用にworkflowを走らせるためのトリガーイベントは`pull_request`または`push`ばかりでしたが、
`workflow_dispatch`、`workflow_run`、`workflow_call`など便利なトリガーイベントの利用方法などなど。
また、outputの設定やconfigurationのスコープなど
細かいことについては意外と初耳な内容が個人的にはありました。

# Learning Path

おそらくこの章が一番読まれる方にとって一番興味があるのではないかと思います。

1. Microsoft Learning Path: GitHub Actions

まず、シラバスにあるとおり、GitHub ActionsのMicrosoft Learning Pathを一通りやってみました。
[こちら](https://learn.microsoft.com/en-us/collections/n5p4a5z7keznp5)からアクセスできます。
モジュールと言われる小さなコース５つで構成され、それぞれのモジュールは説明分を読む -> GitHubのレポジトリを使ってハンズオンエクササイズ
-> 最後に確認テストを行うという構成になっています。
それぞれの説明分は基本的な知識のみで、「詳しくはこちらのドキュメントを参照」というような感じでGitHub公式ドキュメントへのリンクが複数あります。
私はめんどくさがりなので、そのようなリンクはクリックせず、ハンズオンエクササイズと確認テストだけサクッと済ませました。

2. `12zamu/github-certification-preparation-guide`レポジトリ

なんとなくMicrosoft Learning Pathだけでは不安で、かといってすべてのドキュメントを読み込む気にもならず、
いくつかのブログを読んで、他の方どのような勉強されて資格を取得されたのか調査すると、いくつか有用なレポジトリをみつけました。
そのひとつが `12zamu/github-certification-preparation-guide`レポジトリです。
特に[このページ](https://github.com/12zamu/github-certification-preparation-guide/blob/main/content/exams/github-actions.md)で自分で知識の確認テストができます。
本番のテストは選択式でしたが、こちらで自分の知識をチェックすることができます。
私は答えられなかったものは繰り返し確認して刷り込んでおきました。

3. ghcertified.com

こちらはOpenSourceのサイトでPractice Testが受けられることを発見しました。
レポジトリは[こちら](https://github.com/FidelusAleksander/ghcertified)にから確認でき、テスト問題を募っています。
GitHub Actions意外の練習問題もあり、最後にどこを間違ったのか、正解はなにかを総復習することができます。

![image](/images/github.png)

こちらもすべて正解できるまで２，３度練習して、間違ったところを中心に最後の仕上げで公式ドキュメントを読みました。

# 試験の感想

試験はテストセンターまで赴いて受験しました。全部で76問で120分です。ゆっくり解いても20分ほど余りました。
ゆっくり復習して、悩ましい場合は精一杯脳みそを回転させなにか思い出せないか四苦八苦して、無事時間内に回答を終えました。
終了後すぐに正答率および試験の合否がすぐに表示されるので、後腐れなく試験会場を去ることができます。
勉強時間の割に、現状比較的レアで誰もが知っているGitHubに関する資格が取れるので、おすすめです。

# （おまけ）実務で有用そうか。。？

有用だと思いました。少なくとも私は実務で利用しているGitHub Actionsの記述や連携方式を改善できると勉強しながら感じました。
ContextやEnvironment Variableの種類や、outputの活用など、「あ、これを使えばもっとうまく書けそうかも。。？」と感じることがあり、
実際役にたちました。

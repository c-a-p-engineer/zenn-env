# Zenn環境
[Zenn](https://zenn.dev/) のコンテンツ作成用、Docker環境

# Requirement
* [docker](https://www.docker.com/)

# Usage

起動
```bash
docker-compose up
```
http://localhost:8000
<br><br>
記事の作成
```bash
docker exec -it zenn-env_zenn_1 zenn new:article
```
<br>

[Zennのスラッグ（slug）とは](https://zenn.dev/zenn/articles/what-is-slug)<br>

記事の中身 ``` ./articles/{slug}.md```
```
---
title: "" # 記事のタイトル
emoji: "😸" # アイキャッチとして使われる絵文字（1文字だけ）
type: "tech" # tech: 技術記事 / idea: アイデア記事
topics: [] # タグ。["markdown", "rust", "aws"]のように指定する
published: true # 公開設定（falseにすると下書き）
---

ここから本文を書く
```

<br>
各種オプションの指定

```
zenn new:article --slug 記事のスラッグ --title タイトル --type idea --emoji ✨ 
```

削除は[ダッシュボード](https://zenn.dev/dashboard)から行います。安全のため、``` articles ```ディレクトリからマークダウンファイルを削除してもzenn.dev上では削除はされません。<br>
[記事の削除](https://zenn.dev/zenn/articles/zenn-cli-guide#%E8%A8%98%E4%BA%8B%E3%81%AE%E5%89%8A%E9%99%A4)

<br>

本の作成
```bash
docker exec -it zenn-env_zenn_1 zenn new:book
# 
# 本のslugを指定する場合は以下のようにします。
# docker exec -it zenn-env_zenn_1 zenn new:book new:book --slug ここにスラッグ
```
削除は[ダッシュボード](https://zenn.dev/dashboard)から行います。安全のため、``` books ```ディレクトリからマークダウンファイルを削除してもzenn.dev上では削除はされません。<br>
[本の削除](https://zenn.dev/zenn/articles/zenn-cli-guide#%E6%9C%AC%E3%81%AE%E5%89%8A%E9%99%A4)

<br>
<br>

プレビュー（docker起動時に自動実行）
```bash
docker exec -it zenn-env_zenn_1 zenn preview
```

削除は[ダッシュボード](https://zenn.dev/dashboard)から行います。安全のため、``` articles ```ディレクトリからマークダウンファイルを削除してもzenn.dev上では削除はされません。<br>
[記事の削除](https://zenn.dev/zenn/articles/zenn-cli-guide#%E8%A8%98%E4%BA%8B%E3%81%AE%E5%89%8A%E9%99%A4)

# Note
* [GitHubリポジトリでZennのコンテンツを管理する](https://zenn.dev/zenn/articles/connect-to-github)
* [Zenn CLIをインストールする](https://zenn.dev/zenn/articles/install-zenn-cli)
* [Zenn CLIを使ってコンテンツを作成する](https://zenn.dev/zenn/articles/zenn-cli-guide)
<br><br>

* [ZennのMarkdown記法](https://zenn.dev/zenn/articles/markdown-guide)
<br><br>

* [Zennのドキュメント用リポジトリ](https://github.com/zenn-dev/zenn-docs)


# Author
* [こぴぺたん](https://twitter.com/c_a_p_engineer)

# License
[MIT license](https://en.wikipedia.org/wiki/MIT_License).

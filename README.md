# Frisco

App promotion themed template for Jekyll. Browse through a [live demo](https://brave-submarine.cloudvent.net/).
Increase the web presence of a App with this configurable theme.

![Frisco template screenshot](images/_screenshot.jpg)

Frisco was made by [CloudCannon](http://cloudcannon.com/), the Cloud CMS for Jekyll.

Find more templates, themes and step-by-step Jekyll tutorials at [CloudCannon Academy](https://learn.cloudcannon.com/).

## Features

* Contact form
* Pre-built pages
* Pre-styled components
* Blog with pagination
* Post category pages
* Disqus comments for posts
* Staff and author system
* Configurable footer
* Optimised for editing in [CloudCannon](http://cloudcannon.com/)
* RSS/Atom feed
* SEO tags
* Google Analytics

## Setup

1. Add your site and author details in `_config.yml`.
2. Add your Google Analytics and Disqus keys to `_config.yml`.
3. Get a workflow going to see your site's output (with [CloudCannon](https://app.cloudcannon.com/) or Jekyll locally).

## Develop

Frisco was built with [Jekyll](http://jekyllrb.com/) version 3.3.1, but should support newer versions as well.

Install the dependencies with [Bundler](http://bundler.io/):

~~~bash
$ bundle install
~~~

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

### 動かない場合

上の'Develop'記載の操作手順で動作しない場合、Rubyのバージョンを確認すると良いかも。
いちおう、3.0.0で動作確認できている。

rubyのバージョンを確認するにはこうする。

~~~bash
// ruby のバージョンを確認
$ ruby -v
ruby 2.6.3p62 (2019-04-16 revision 67580) [universal.arm64e-darwin20]
~~~

rbenv を使えば、ディレクトリごとに使用するrubyのバージョンを指定できる。

Macなら概ね以下の流れ。
1. brewでrbenvをインストール
2. pathを通す（zsh と bashだとやり方違うので注意）
3. 必要なrubyのバージョンを指定してインストール
4. ディレクトリでrubyのバージョンを指定
5. 以下、bundle install〜

~~~bash
// rbenvはインストールできている前提でそれ以降の操作はこんな感じ
// インストール可能なRubyのバージョン一覧の表示
$ rbenv install -l
// 指定したRubyのバージョンをインストール
$ rbenv install 3.0.0
// インストールしたRubyを使用可能な状態にする⇒shimsへの反映
$ rbenv rehash
// カレントディレクトリで使うRubyのバージョンを指定
$ rbenv local 3.0.0
// 再度バージョンを確認
$ ruby -v
ruby 3.0.0p0 (2020-12-25 revision 95aff21468) [arm64-darwin20]
~~~

参考：[https://github.com/rbenv/rbenv#understanding-shims](https://github.com/rbenv/rbenv#understanding-shims)

## Editing

Frisco is already optimised for adding, updating and removing pages, staff, advice, company details and footer elements in CloudCannon.

### Posts

* Add, update or remove a post in the *Posts* collection.
* The **Staff Author** field links to members in the **Staff Members** collection.
* Documentation pages are organised in the navigation by category, with URLs based on the path inside the `_docs` folder.
* Change the defaults when new posts are created in `_posts/_defaults.md`.

### Contact Form

* Preconfigured to work with CloudCannon, but easily changed to another provider (e.g. [FormSpree](https://formspree.io/)).

### Staff

* Reused around the site to save multiple editing locations.

### Footer

* Exposed as a data file to give clients better access.
* Set in the *Data* / *Navigation* section.

### Footer

* Exposed as a data file to give clients better access.
* Set in the *Data* / *Footer* section.

## プロジェクトページの追加

- 既存の.mdファイルを参考に作成する。（ファイル名の先頭は数字以外）
- 並び順（sort_value）は原則5桁固定で3桁目を増やして行く。表示は昇順となる。　例）00000, 00100, 00200
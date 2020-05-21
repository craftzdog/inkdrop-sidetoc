# Inkdrop SideToc Plugin

Provides Side TOC.

![Screenshot](https://raw.githubusercontent.com/basyura/inkdrop-sidetoc/master/images/screenshot.png)

## Features

- Show TOC of headers.
- Highlight current header.
  - Follow cursor movement and scroll
- Toggle side toc pane.
- Jump to header on click.
- Jump to next (or previous) header by key.

## Install

```
ipm install sidetoc
```

## Keybindings

| Command                | Explanation              |
| ---------------------- | ------------------------ |
| sidetoc:sidetoc-toggle | Toggle side toc pane.    |
| sidetoc:jump-next      | Jump to next header.     |
| sidetoc:jump-prev      | Jump to previous header. |

keymap.cson

```cson
'body':
    'ctrl-l': 'sidetoc:sidetoc-toggle'
    'ctrl-n': 'sidetoc:jump-next'
    'ctrl-p': 'sidetoc:jump-prev'
```

## Settings

| key            | default |
| -------------- | ------- |
| highlightColor | #C5EAFB |
| width          | 200     |

config.cson

```cson
sidetoc:
  highlightColor: "#C5EAFB"
  width: 200
```

## Changelog

1.5.0 - 2020/05/09

- Add commands.
  - sidetoc:jump-next
  - sidetoc:jump-prev
- Add cursor style.
- Fix multiple event registration

  1.4.0 - 2020/05/05

- Improved highlight header

  1.3.0 - 2020/04/25

- Fix header regex

  1.2.0 - 2020/04/05

- improved readme

  1.1.0 - 2020/03/29

- improved readme

  1.0.0 - 2020/03/29

- First release!

## ToDo

- [ ] 入力のたびに再描画が走る
  - 保存時に反映するだけにしたいが API が無い？
  - 処理時間は 0 〜 2ms なので問題はなさそう
- [ ] プレビュー時のハイライト表示

### Done

- [x] スクロールバーの動きに追従
- [x] セクションがない場合はサイドバー表示しない
- [x] toggle で非表示にしても min-width が効いていて領域を取っている
- [x] サイドバーの幅指定
- [x] スタイル設定 (config 設定)
- [x] エディタのフォント設定を取得して反映する
- [x] サイドバークリックでジャンプしたい
- [x] カーソルの mouse over でセクションの色を変える
- [x] セクション (`#`) 行を出力する
- [x] カーソルの位置をセクションに合わせる (CPU 使いそう)
- [x] セクション移動 (リンク、ショートカットキー)

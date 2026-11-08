# claude-plugins

Taku Nagai が作ったツールを AI エージェントから使うための Claude Code プラグイン集です。マーケットプレイス名は `takunagai` です。

## 入れ方

```bash
claude plugin marketplace add takunagai/claude-plugins
claude plugin install <プラグイン名>@takunagai
```

1 行で入れる場合（Claude Code 2.1.292 以降）:

```bash
claude plugin install <プラグイン名> --marketplace takunagai/claude-plugins
```

更新と削除:

```bash
claude plugin update <プラグイン名>@takunagai
claude plugin uninstall <プラグイン名>@takunagai
```

SSH 鍵を設定していない環境では、環境変数 `CLAUDE_CODE_PLUGIN_PREFER_HTTPS=1` を付けて実行してください。

## 収録プラグイン

| 名前 | 内容 | ツールのリポジトリ |
| --- | --- | --- |
| `screenshot-masker` | 公開前のスクリーンショットから機密情報を見つけてマスクする手順を、AI エージェントに教えるスキル | [takunagai/screenshot-masker](https://github.com/takunagai/screenshot-masker) |

各プラグインはツール本体を入れません。ツールの導入は各リポジトリの README に従ってください。

## 運用

- プラグインを足す手順: [AGENTS.md](AGENTS.md)
- 公開範囲と名前の決定: [docs/公開と更新の設定.md](docs/公開と更新の設定.md)

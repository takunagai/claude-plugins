# AGENTS.md

Claude Code プラグインのカタログ（マーケットプレイス `takunagai`）。`.claude-plugin/marketplace.json` が本体で、このリポジトリは **public**。

## プラグインを足す手順

1. `.claude-plugin/marketplace.json` の `plugins` に `github` ソースでエントリを足す: `{"name": "<名前>", "source": {"source": "github", "repo": "takunagai/<ツール>"}, "description": "..."}`
2. `name` はツール側 `.claude-plugin/plugin.json` の `name` と一致させる。違うとインストールに失敗する
3. エントリにも `plugin.json` にも `version` を書かない（書くと値を上げるまで利用者に更新が届かない）
4. `claude plugin validate .` を通す
5. `claude plugin marketplace update takunagai` の後、実際に `claude plugin install <名前>@takunagai` で入れて確かめる。validate は `repo` の誤りを見つけない
6. README の収録プラグイン表に行を足す

## 規則

- 公開後は `name`（マーケットプレイス・プラグインとも）を変えない。変えるなら `renames` に追記する（書き換えない）
- 非公開のツールを載せるとリポジトリ名が公開される。載せる前にユーザーに確認する
- `relevance`・`dependencies`・`version` は足さない
- 指示ファイルは `AGENTS.md` を使う（`CLAUDE.md` は作らない）

# mkdocs-prj-templates

## テンプレート
### ドキュメント用リポジトリ向け
ドキュメント用リポジトリなので、ルートディレクトリに必要なファイルを配置し、`docker-compose`で素直に操作するスタイル.

[simple](/simple)

- `mkdocs serve` ... `docker-compose up -d`
- `mkdocs build` ... `docker-compose run --rm mkdocs mkdocs build`

### アプリケーションリポジトリなどドキュメント用途以外のリポジトリに追加する向け
ドキュメント用途以外のリポジトリに追加するため、ファイルが散らからないようにmkdocs.yml以外のファイルをdocsに配置し、`bin/docs-compose`経由でコマンドを操作を行うスタイル.  
`mkdocs-exclude`でビルド時に、Dockerfileやdocker-compose.yamlが含まれないようにしている.

[in-docs](/in-docs)

- `mkdocs serve` ... `bin/docs-compose up -d`
- `mkdocs build` ... `bin/docs-compose run --rm mkdocs mkdocs build`

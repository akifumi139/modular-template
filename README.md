# テンプレートを使った新規プロジェクトの立ち上げ

1. 新しいプロジェクト用のディレクトリを作成し、テンプレートをコピーします。

```sh
git clone --depth=1 git@github.com:akifumi139/modular-template.git your-new-project
cd your-new-project
rm -rf .git README.md
git init
```

2. **VS Codeでこのディレクトリを開き、「Dev Containers: Reopen in Container」を実行します。**

3. 以降はテンプレートプロジェクトと同様にセットアップします。

```sh
composer install
npm install
cp .env.example .env
php artisan key:generate
php artisan migrate
```

---

## 備考

- VSCodeとdevContainer拡張機能は事前にセットアップしておいてください。
- `.env` の内容はプロジェクトごとに調整してください。
- `php artisan serve` でバックエンド、`npm run dev` でフロントエンドの開発サーバーが起動します。
- Dev Containerのカスタマイズは `.devcontainer` ディレクトリ内で行えます。
- その他詳細は [README.md](README.md) や [ドキュメント](https://laravel.com/docs) を参照してください。
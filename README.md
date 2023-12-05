# laravel プロジェクトの作成

## nginxコンテナでbashまたはdockerdesktopのphpコンテナのterminalに入る

```DOS
>docker exec -it php bash
```

## laravelプロジェクトの作成

```Bash
composer create-project laravel/laravel lara6sampleprj "6.*"
```

## storageフォルダのパーミッションの変更
```Bash
chmod -R 777 storage
```

## nginx default.confの修正

```
server {
  listen 80;

  -- root  /var/www/public;
  ++ root  /var/www/lara6sampleprj/public
```

# simple-absensi

## Cara Install di Local

-   Hal yang harus dipersiapkan
    -   git
    -   composer
    -   php v8.1

```sh
# clone terlebih dahulu lewat cli (cmd, bash, atau yg lain)
git clone https://github.com/fayzisme/simple-absensi.git

# masuk ke foldernya
cd simple-absensi

# install semua package
composer install

# pilih salah satu
# 1. windows
copy .env.example .env
# 2. unix (ubuntu, mac os and others)
cp .env.example .env

# setelah itu, setting .env file seperti nama database (DB_DATABASE), username dan passwordnya
# lalu buat database baru dari phpmyadmin atau cli langsung juga bisa dengan nama sesuai DB_DATABASE yang ada di file .env
php artisan key:generate
php artisan migrate
php artisan db:seed
php artisan serve --port=8100

# lalu buka browser dengan url: http://localhost:8100/
```


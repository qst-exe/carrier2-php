# Chapter4

クラスについてです。

実際の仕事で頻繁に活用する部分で、詰まる箇所の多い場所でもあります。

## 困ったときに見るべきサイト

- [PHP入門](https://www.javadrive.jp/php/)
- [PHPマニュアル](https://www.php.net/manual/ja/index.php)

## クラスとは

[クラスの基礎](https://www.php.net/manual/ja/language.oop5.basic.php)

### 課題1

掲示板Appをクラス(Threadクラス)を使って書き換えてください。

```php
<?php

class Thread {
    
    public function getList() {
    
    }
    
    public function post() {
    
    }

    public function delete() {
    
    }
}

```

### 課題2

掲示板Appに複数のスレッドが立てられるようにしてください。スレッドのタイトルはなくても大丈夫です。
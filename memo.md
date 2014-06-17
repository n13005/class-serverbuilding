サーバー構築の講義でやったこと
==================================

## 仮想化環境の構築

## LAMP環境の構築

### Wordpress
<<<<<<< HEAD
#apache2とphp5とmysqlとmysql-serverをインストール
#wordpressをいれる
#### Wordpressチューニング

=======

### Wordpressチューニング
acp
hiphopphp
>>>>>>> 09837bfa1f750075506677a1e2a807e451a7593c
### EC-CUBE

## DNSサーバー

### bind?
udo aptitude install bind9
を最初にする
その後、/etc/bindの中のnamed.conf.default-zones
の中をsudo vi named.conf.default-zones で編集
一番下の zoneを
 "n13005.it-college.local" {
        type master;
        file "/etc/bind/n13005.zone";
};

にする。
 cp db.255　n13005.zoneでコピーして
sudo vi n13005.zoneを編集
;
; BIND reverse data file for broadcast zone
;
$TTL    604800
@       IN      SOA     n13005.it-college.local. root.localhost. (
                              1         ; Serial
                         604800         ; Refresh
                          86400         ; Retry
                        2419200         ; Expire
                         604800 )       ; Negative Cache TTL
;
@       IN      NS      n13005.it-college.local.
        IN      A       10.0.133.237
www     IN      A       10.0.133.237

sudo named-checkzone n13005.it-college.local n13005.zone
をじっこうしてsudo service bind9 restart

dig @localhost n13005.it-college.localでIPアドレスが表示されれば
OK：


## chef
仮想サーバーを使える
## docker

## git

## 試験範囲


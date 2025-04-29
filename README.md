# ZMK Firmware for SEIBOKU（青墨）

このリポジトリでは、[ZMK Firmware](https://zmk.dev/) による [SEIBOKU（青墨）](https://github.com/snize/BOB-PMW3610-SEIBOKU)のファームウェア例を提供します。

Seeed Studio XIAO nRF52840 を採用し、BLE での接続をサポートしていますが有線での接続も可能です。

## ファームウェアの書き込み

1. [Releases](https://github.com/snize/zmk-seiboku-example/releases) から最新のファームウェア `seiboku-seeeduino_xiao_ble-zmk.uf2` をダウンロードしてください。
2. PC と XIAO nRF52840 を USB ケーブルで接続します。
3. XIAO nRF52840 のリセットボタンを素早く2回押してブートローダーモードにします。
4. 各OSに合わせたファイラが開くので、ダウンロードしたファームウェアをドラッグ＆ドロップしてください。
5. 以上でファームウェアの書き込みが完了します。

## BLE 接続

通常のBLEデバイスと同様に、PCやスマートフォンから接続することができます。`SEIBOKU`というデバイス名で検出されます。キーマップに`BT_CLR`をアサインしているので、デバイス側のボタンを押すことでペアリング情報を削除することができます。


## 設定変更

このプロジェクトをフォークして編集してください。

### キーマップの変更

[boards/shields/seiboku/seiboku.keymap](boards/shields/seiboku/seiboku.keymap) を `config/seiboku.conf` にコピーして編集してください。

### 設定の変更

[boards/shields/seiboku/seiboku.conf](boards/shields/seiboku/seiboku.conf) を `config/conf.conf` にコピーして変更したい値のみ残し編集してください。

## ビルド

ビルドはGithub Actionsを利用すると環境構築が不要で簡単に行えます。公式のdevcontainerを利用する事もできます。[ZMK Firmwareをdevcontainerでビルドするときのディレクトリ構成｜snize](https://note.com/snize/n/n10310eaeac22)などを参考にしてみてください。

## 免責事項

このファームウェアは無保証です。自己責任でご利用ください。特にBLE接続のためリチウムイオンポリマー電池を使用する場合は、適切な取り扱いを行ってください。

## ライセンス

このリポジトリはMITライセンスで提供されています。詳細は[LICENSE](LICENSE)を参照してください。
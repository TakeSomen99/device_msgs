# ros2_mypkg
ROS2において、Webカメラを含む外部USBデバイスの製品名をサービス型通信で取得するためのメッセージ定義パッケージです。

![](https://github.com/TakeSomen99/ros2_mypkg/actions/workflows/test.yml/badge.svg)
![CMake](https://img.shields.io/badge/CMake-3.8%2B-blue?logo=cmake)

## 確認済み動作環境
+ Ubuntu 24.04 LTS
+ Raspberry Pi 3B
+ Python 3.10, 3.11, 3.12
+ CMake 3.26, 3.27, 3.28

## 概要
本パッケージでは**引数なし・戻り値が string のみ**という最小設計のサービス型を定義しています。

本パッケージの主な目的として、Raspberry Piを含むUSB付きシングルボードコンピュータに接続されている外部デバイスを、人間が識別しやすい名前で取得することを目的としています。

## 使用例
本パッケージを利用する場合、本パッケージをご自身の開発環境と同じ階層にクローンしてください。
```bash
$ git clone https://github.com/TakeSomen99/device_msgs.git
```
Pythonプロジェクトで利用いただく場合、以下の文を本パッケージを採用したいソースコードに張り付け、インポートしてください。
```python
from device_msgs.srv import Device
```
具体的な使用例は以下のパッケージをご覧ください。
+ https://github.com/TakeSomen99/mypkg

## 注意事項
本パッケージはメッセージ型のみを定義しており、デバイスの検出ロジックやOSでの受け取り処理は含まれておりません。

## ライセンス
- このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
- © 2025 TakeSomen99

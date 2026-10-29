# 第2章 アプリケーションアーキテクチャ

## Q9. レイヤードアーキテクチャ

**問題：** Controller / Service / Repository の役割を説明してください。また、なぜ分離するのか、Controller と Service の責務の境界はどこかも答えてください。

**回答：**

Controller は窓口を担当します。Service は処理を担当します。Repository はデータベースの倉庫番を担当します。

分離する理由は、1つのクラスにまとめると、ルールを変えたいとき（Service の領域）に、窓口（Controller）の部分まで一緒に直すことになって困るからです。

Controller と Service の境界は、チェックまでが Controller、判断からが Service です。

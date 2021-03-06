# UsingPipes

.NET Lab 2018/12 向け。

`C# でパイプ使ってるのが見たいって？`

という話なので作ってみるよ！

## プロジェクト構成

[名前なしパイプサーバー](AnonimousPipeServer/)  
[名前なしパイプクライアント]()  
[名前付きパイプサーバー]()  
[名前付きパイプクライアント]()

[セッション資料下書き]()



## お題目

「C# でパイプ使ってるのが見たいというので作ってみた」

## お品書き

- そもそもパイプって何？
- パイプの種類とできること
- 名前のないパイプ
- 名前のあるパイプ

## そもそもパイプって何？

- プロセス間通信(IPC:Interprocess Communications)の一種。
- アプリケーション同士でデータ共有するための仕組みの総称
- 大半のIPCは同一プロセス内のスレッド間でも利用可能
- エンドポイント同士は同期的ではない
- 通信手段的に同期的な場合も非同期的な場合もある

## 通信における役割

- サーバー(S)
  - 通信を提供する側
  - 事前の準備を行い、接続管理をする
  - 原則接続待ちすることが多い
- クライアント(C)
  - 通信を利用する側
  - 作成済みの機能を利用する

単一プロセス内で利用する場合でも C/S 役が必要

## ほかのプロセス間通信

- Clipboard
- COM
- COM+
- Data Copy
  - *Network DDE*
- DDE
- File Mapping
- *LPC(Local Procedure Call)*
- Mailslots
- Pipe
- RPC(Remote Procedure Call)
- Windows Sockets

*Network DDE* は、インターフェースだけ！  
呼び出すと、`NDDE_NOT_IMPLEMENTED`

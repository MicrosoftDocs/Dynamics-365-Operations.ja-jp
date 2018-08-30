---
title: "オフライン モードの Retail Modern POS (MPOS)"
description: "この記事では、Retail サーバーが利用できない場合に、オフライン モードで Retail Modern POS デバイスを使用する方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 31441
ms.assetid: 219f93a3-6321-46e9-b989-f97072af0bb3
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: f0e5e7131bf5d6f337b2197f2aa56056870b8a95
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="retail-modern-pos-mpos-in-offline-mode"></a>オフライン モードの Retail Modern POS (MPOS)

[!include [banner](../includes/banner.md)]

この記事では、Retail サーバーが利用できない場合に、オフライン モードで Retail Modern POS デバイスを使用する方法について説明します。

Retail サーバーが利用できない場合、Retail Modern POS はオフラインになります。 Retail サーバーとの接続が失われると、販売時点管理 (POS) はオフライン データベースに自動的に接続されます。 オフライン プロファイルでコンフィギュレーションされたタイムアウトの間隔内でデータの要求が成功しない場合、Retail Modern POS は自動的にオフライン データベースに切り替わり、販売トランザクションを続行します。 Retail Modern POS はオフライン プロファイルでコンフィギュレーションされた再接続試行間隔の後に Retail Server への再接続を試みます。 この再接続の試みは、トランザクションの開始時にのみ発生します。

## <a name="determine-the-connection-mode-of-retail-modern-pos"></a>Retail Modern POS の接続モードを決定する
Retail Modern POS のステータス ヘッダーは、現在の接続状態を示します。 

[![接続](./media/connection.png)](./media/connection.png) 

Retail Modern POS の **接続ステータス** ページには、オフライン データベースと同期する前回の試みのステータスが表示されます。 

[![接続ステータス](./media/connection-status.png)](./media/connection-status.png)

## <a name="create-a-button-to-manually-switch-between-online-and-offline-modes"></a>手動でオンラインとオフライン モードを切り替えるためのボタンを作成
Retail Modern POS にオンラインとオフライン モードを手動で切り替えるボタンを追加できます。 **POS 操作 917 – データベース接続ステータス**のボタンを作成します。 接続または切断するには、ボタンをトグルとして切り替えて使用します。

## <a name="operations-that-can-be-completed-when-the-channel-database-is-offline"></a>チャネル データベースがオフラインのときに実行できる操作
チャネル データベースがオフラインときは、次の操作を完了することができます。 **注記:** Commerce Data Exchange: リアルタイム サービスが必要な機能があれば、操作がサポートされていないことを示すエラー メッセージが表示されます。 **ヒント:** オフライン データベースで使用できるデータにのみ、レポートおよびその他の操作が実行されます。

| 操作 ID | 説明                         |
|--------------|-------------------------------------|
| 100          | 製品売上                        |
| 101          | 価格の確認                         |
| 102          | 製品の無効化                        |
| 103          | 製品コメント                     |
| 104          | 価格変更                      |
| 105          | 数量の設定                        |
| 106          | 数量のクリア                      |
| 108          | 製品検索                      |
| 109          | 返品                      |
| 115          | 仕訳帳の表示                        |
| 117          | ロイヤルティ カードの追加                    |
| 123          | 単位の変更              |
| 128          | リストから取引税を上書きする  |
| 130          | リストから明細行の製品税を上書きする |
| 132          | 預金の上書き                    |
| 134          | 所属を追加                     |
| 135          | リストから所属を追加           |
| 200          | 現金で支払う                            |
| 202          | 顧客口座から支払う                |
| 203          | 各種通貨で支払う                        |
| 206          | 現金で即支払う                      |
| 211          | 支払の無効化                        |
| 214          | ギフト カードで支払う                       |
| 300          | 品目割引金額                |
| 301          | 品目割引率               |
| 302          | 合計割引金額               |
| 303          | 合計割引率              |
| 500          | トランザクションの無効化                    |
| 501          | トランザクション コメント                 |
| 503          | トランザクションの中断                 |
| 512          | ギフト カードの発行                     |
| 515          | 注文の取り消し                        |
| 519          | ギフト カードに追加                    |
| 520          | ギフト カード残高                   |
| 602          | 顧客検索                     |
| 603          | 顧客のクリア                      |
| 612          | 顧客の追加                        |
| 622          | 検索                              |
| 623          | 顧客の編集                       |
| 701          | ログオフ                             |
| 703          | レジスターのロック                       |
| 801          | 在庫検索                    |
| 802          | 在庫数                         |
| 917          | データベース接続ステータス          |
| 920          | タイム レコーダー                          |
| 921          | タイム レコーダー エントリの表示             |
| 922          | 製品の詳細表示                |
| 1003         | レポートの表示                        |
| 1052         | 支払/入金申告                  |
| 1200         | 開始金額の申告                |
| 1201         | 釣銭入力                         |
| 1210         | 支払/入金の削除                      |
| 1211         | 金庫保管                           |
| 1212         | 銀行入金                           |

## <a name="operations-that-cant-be-completed-when-the-channel-database-is-offline"></a>チャネル データベースがオフラインのときに実行できない操作
チャネル データベースがオフラインときは、次の操作を完了することができません。

| 操作 ID | 説明       |
|--------------|-------------------|
| 207          | ロイヤルティ カードで支払う  |
| 707          | デバイスのアクティブ化   |
| 708          | デバイスの無効化 |
| 1053         | シフトのブラインド クローズ |
| 1054         | シフトの中断     |
| 1055         | シフトのクローズ       |
| 1056         | X の印刷           |
| 1057         | 再印刷 Z         |







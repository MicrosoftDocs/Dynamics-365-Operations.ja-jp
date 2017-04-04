---
title: "小売チャンネル通信 (Commerce Data Exchange) の定義"
description: "この記事では、Commerce Data Exchange とそのコンポーネントの概要を説明します。 これは、各コンポーネントは、アクションと、チャンネルのMicrosoft Dynamics 365の間でデータを転送に果す役割を説明します。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>小売チャンネル通信 (Commerce Data Exchange) の定義

この記事では、Commerce Data Exchange とそのコンポーネントの概要を説明します。 これは、各コンポーネントは、アクションと、チャンネルのMicrosoft Dynamics 365の間でデータを転送に果す役割を説明します。

<a name="overview"></a>概要
--------

データ交換コマースは、オンライン店舗または実店舗のような作業と、チャンネル365 for Operationsの間でデータを転送するシステムです。 小売チャンネルのデータを格納するデータベースは、データベース365 for Operationsとは別にあります。 チャンネルのデータベースは、小売トランザクションに必要なデータのみ格納します。 マスタ データは、Dynamics 365 for Operationsでコンフィギュレーションしてチャンネルに分割されます。 トランザクション データは(POS) POSシステムのオンラインまたは店舗で作成し、Dynamics 365 for Operationsにアップロードされます。 データ配送は非同期です。 つまり、データを収集してソースでパッケージングするプロセスは、データを取得して適用するプロセスとは別に行われます。 価格および在庫検索などのシナリオの場合、データはリアルタイムに取得する必要があります。 これらのシナリオをサポートするには、データ交換コマースは、アクション、およびチャンネル365 for Operations内リアルタイムの間の通信を可能にするサービスが含まれます。 

[![更新、グラフィック] (。/media/updated、graphic.png) ] (。/media/updated、graphic.png)   

## <a name="async-service"></a>非同期サービス
工程のデータベース365 for OperationsのMicrosoft SQL Serverの変更の追跡がチャンネルに送られなければするデータが変更を決定するのに使用されます。 配分のスケジューリングに基づいて、工程の梱包365 for Operationsは、中心的 (Azureのブロブの保管) にデータが保存されます。 別のバッチ処理は、このデータ パッケージをチャンネルのデータベースに挿入するために Commerce Data Exchange: Async Client ライブラリを使用します。 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>小売用スケジューラ

スケジューラ ジョブとは、データを配送場所へ (から) 配送するためのメカニズムです。 ジョブは、配分するデータを含むテーブルおよびテーブル フィールドを指定するサブジョブで構成されます。 Dynamics 365 for Operationsは、多くの組織の重複の要件を満たすサブジョブ、事前に定義されたスケジューラ ジョブが含まれます。 次のタイプの定義済ジョブが作成されます。

-   **ダウンロード ジョブ** –のダウンロード ジョブは、Dynamics 365 for Operationsのチャンネルのデータベースに変更されたデータを送信します。 レコードへの変更は、SQL Server 変更履歴によって追跡されます。
-   **アップロード ジョブ (Pジョブ) ** –のアップロード ジョブは、データベース365 for Operationsにチャンネルの販売トランザクションを引っ張ります。 P ジョブは、データを漸増的にアップロードします。 P ジョブが実行されると、Async Client ライブラリが場所から既に受け取ったレコードに対するレプリケーション カウンターをチェックします。 レコードは、レプリケーション カウンターが検出された最大値を超える場合のみアップロードされます。 P ジョブは以前にアップロードされたデータを更新しません。

配分のスケジュールを手動でまたはDynamics 365 for Operationsのバッチ ジョブをスケジュールし、データ転送 (実行するのに使用されます。 配送スケジュールには、1 つ以上のチャンネル データ グループと 1 つ以上のスケジューラ ジョブを含めることができます。

## <a name="realtime-service"></a>リアルタイム サービス
データ交換コマース]: リアル タイム サービスはアクションと、チャンネルに365 for Operations内リアルタイムの間の通信を提供する統合サービスです。 リアル タイム サービスは個々のPOSのコンピューターとオンライン店舗をリアルタイムDynamics 365 for Operationsで特定のデータを検索することができます。 ほとんどの主工程が市内。データベースで実行できますが、次のシナリオでは、Dynamics 365 for Operationsに格納されているデータへの直接アクセスを必要とします:

-   ギフトカードを発行および引換えます。
-   ロイヤルティ ポイントを引き換えます。
-   クレジット メモを発行および引換えます。
-   顧客レコードを作成または更新します。
-   販売注文を作成、更新、完了します。
-   発注書または移動オーダーに対する在庫を入荷します。
-   棚卸資産会計を実行します。
-   店舗間から販売トランザクションを取得し、返品トランザクションを完了します。

[![Real-time Service](./media/rts.png)](./media/rts.png) 

定義済リアルタイム サービス プロファイルが作成されます。



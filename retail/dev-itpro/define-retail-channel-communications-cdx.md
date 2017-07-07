---
title: "小売チャンネル通信 (Commerce Data Exchange) の定義"
description: "この記事では、Commerce Data Exchange とそのコンポーネントの概要を説明します。 ここでは、Microsoft Dynamics 365 for Retail と小売チャンネルとの間でのデータの転送で各コンポーネントが果たす役割について説明します。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 68252e52da47b89166627edbf2aa530e762354c6
ms.contentlocale: ja-jp
ms.lasthandoff: 06/20/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>小売チャンネル通信 (Commerce Data Exchange) の定義

[!include[banner](../includes/banner.md)]


この記事では、Commerce Data Exchange とそのコンポーネントの概要を説明します。 ここでは、Microsoft Dynamics 365 for Retail と小売チャンネルとの間でのデータの転送で各コンポーネントが果たす役割について説明します。

<a name="overview"></a>概要
--------

Commerce Data Exchange は、Dynamics 365 for Retail と、オンライン ストア、実際の店舗などの小売チャンネルの間でデータを転送するシステムです。 小売チャンネルのデータを格納するデータベースは、Dynamics 365 for Retail データベースとは別にあります。 チャンネルのデータベースは、小売トランザクションに必要なデータのみ格納します。 マスター データが Dynamics 365 for Retail でコンフィギュレーションされ、チャンネルに配分されます。 トランザクション データは販売時点管理 (POS) システムまたはオンライン店舗で作成され、Dynamics 365 for Retail にアップロードされます。 データ配送は非同期です。 つまり、データを収集してソースでパッケージングするプロセスは、データを取得して適用するプロセスとは別に行われます。 価格および在庫検索などのシナリオの場合、データはリアルタイムに取得する必要があります。 これらのシナリオをサポートするために、Commerce Data Exchange には、Dynamics 365 for Retail とチャンネル間のリアルタイム通信を可能にするサービスが含まれます。 

[![更新済小売グラフィック](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>非同期サービス
Dynamics 365 for Retail データベースの Microsoft SQL Server 変更追跡は、チャンネルに送信する必要のあるデータの変更内容を特定するのに使用されます。 配送スケジュールに基づいて、Dynamics 365 for Retail はそのデータをパッケージングして中央の保存場所 (Azure BLOB ストレージ) に保存します。 別のバッチ処理は、このデータ パッケージをチャンネルのデータベースに挿入するために Commerce Data Exchange: Async Client ライブラリを使用します。 

[![非同期サービス](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>小売用スケジューラ

スケジューラ ジョブとは、データを配送場所へ (から) 配送するためのメカニズムです。 ジョブは、配分するデータを含むテーブルおよびテーブル フィールドを指定するサブジョブで構成されます。 Dynamics 365 for Retail には、ほとんどの組織のレプリケーションの要件を満たすサブジョブと定義済スケジューラ ジョブが含まれます。 次のタイプの定義済ジョブが作成されます。

-   **ダウンロード ジョブ** – ダウンロードのジョブは、変更されたデータを Dynamics 365 for Retail からチャンネルへ送信します。 レコードへの変更は、SQL Server 変更履歴によって追跡されます。
-   **アップロード ジョブ (P ジョブ)** – アップロード ジョブは、チャンネルから Dynamics 365 for Retail データベースに販売トランザクションをプルします。 P ジョブは、データを漸増的にアップロードします。 P ジョブが実行されると、Async Client ライブラリが場所から既に受け取ったレコードに対するレプリケーション カウンターをチェックします。 レコードは、レプリケーション カウンターが検出された最大値を超える場合のみアップロードされます。 P ジョブは以前にアップロードされたデータを更新しません。

配送スケジュールは、手動または Dynamics 365 for Retail でスケジューリングされたバッチ ジョブによるデータ転送の実行に使用されます。 配送スケジュールには、1 つ以上のチャンネル データ グループと 1 つ以上のスケジューラ ジョブを含めることができます。

## <a name="realtime-service"></a>リアルタイム サービス
Commerce Data Exchange: Real-time Service は、Dynamics 365 for Retail と小売チャンネル間のリアルタイム通信を提供する統合サービスです。 リアル タイム サービスにより、個々の POS コンピューターとオンライン ストアが Dynamics 365 for Retail から特定のデータをリアルタイムで取得できるようになります。 ほとんどのキー操作はローカルのチャンネル データベースで実行できますが、次のシナリオは Dynamics 365 for Retail に格納されているデータへの直接アクセスが必要です。

-   ギフトカードを発行および引換えます。
-   ロイヤルティ ポイントを引き換えます。
-   クレジット メモを発行および引換えます。
-   顧客レコードを作成または更新します。
-   販売注文を作成、更新、完了します。
-   発注書または移動オーダーに対する在庫を入荷します。
-   棚卸資産会計を実行します。
-   店舗間から販売トランザクションを取得し、返品トランザクションを完了します。

[![リアルタイム サービス](./media/rts.png)](./media/rts.png) 

定義済の Real-time Service プロファイルが作成されます。





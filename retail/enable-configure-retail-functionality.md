---
title: "新しい小売環境にシード データを初期設定します。"
description: "この記事は、]、Microsoft Dynamics 365の初期化処理の一部として作成されるデータを説明します。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>新しい小売環境にシード データを初期設定します。

この記事は、]、Microsoft Dynamics 365の初期化処理の一部として作成されるデータを説明します。

小売ソリューションが Microsoft Dynamics Lifecycle Services (LCS) によって配置された後、基本的なコンフィギュレーション データを作成するために、小売コンフィギュレーションを初期化する必要があります。 **重要:** 小売コンフィギュレーションを初期化する前に、小売店舗を設定する法人ごとの言語と住所が指定されていることを確認します。 この手順は、小売に使用する法人ごとに完了する必要があります。 小売のコンフィギュレーションを初期化するには、次の手順に従います。

1.  工程のクライアント365 for Operationsを開始します。
2.  [** [小売りとコマース** &gt; **設定されている本部** &gt; **パラメータ** &gt; **パラメータをRetail **します。
3.  **初期化**をクリックします。

初期化によって、次の既定のコンフィギュレーション データを作成します:

-   小売用スケジューラ ジョブとサブジョブ
-   小売チャンネル スキーマ
-   小売配送スケジュール
-   ボタン グリッドと画像、テーマを含む、既定の画面レイアウト
-   タイムゾーン情報
-   販売時点管理 (POS) 操作
-   POS アクセス許可
-   チャンネル レポート
-   属性メタデータ
-   エンティティ検証テンプレート
-   Commerce Data Exchange セッション履歴を削除するバッチ ジョブ

また、記録は、データベース365 for Operationsに支払カードの業界(PCI)に関連する有効になります。 **注記:** 別に小売用スケジューラをコンフィギュレーションできます。 このオプションで、小売用スケジューラのコンフィギュレーションを既定の設定にリセットすることができます。 初期化の完了後に、追加の小売データをコンフィギュレーションする必要があります。 次にいくつか例を挙げます。

-   小売パラメーター
-   小売用スケジューラのパラメーター
-   小売チャンネル
-   レジスターとデバイス
-   品揃え




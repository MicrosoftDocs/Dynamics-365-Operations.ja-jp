---
title: 新しい Retail 環境でのシード データの初期化
description: この記事では、Microsoft Dynamics 365 for Retail の初期化プロセスの一部として作成されるデータについて説明します。
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "327898"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a>新しい Retail 環境でのシード データの初期化

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 for Retail の初期化プロセスの一部として作成されるデータについて説明します。

小売ソリューションが Microsoft Dynamics Lifecycle Services (LCS) によって配置された後、基本的なコンフィギュレーション データを作成するために、小売コンフィギュレーションを初期化する必要があります。

> [!IMPORTANT]
> 小売コンフィギュレーションを初期化する前に、小売店舗を設定する法人ごとの言語と住所が指定されていることを確認します。 この手順は、小売に使用する法人ごとに完了する必要があります。

小売のコンフィギュレーションを初期化するには、次の手順に従います。

1. Dynamics 365 for Retail クライアントを起動します。
2. **小売** &gt; **本社の設定** &gt; **パラメーター** &gt; **小売パラメーター**をクリックします。
3. **初期化**をクリックします。

初期化によって、次の既定のコンフィギュレーション データを作成します:

- 小売用スケジューラ ジョブとサブジョブ
- 小売チャンネル スキーマ
- 小売配送スケジュール
- ボタン グリッドと画像、テーマを含む、既定の画面レイアウト
- タイムゾーン情報
- 販売時点管理 (POS) 操作
- POS アクセス許可
- チャンネル レポート
- 属性メタデータ
- エンティティ検証テンプレート
- Commerce Data Exchange セッション履歴を削除するバッチ ジョブ

また、Payment Card Industry (PCI) に関連付けられるログが Dynamics 365 for Retail データベースに対して有効になります。

> [!NOTE]
> 別々に小売用スケジューラをコンフィギュレーションするオプションがあります。 このオプションで、小売用スケジューラのコンフィギュレーションを既定の設定にリセットすることができます。

初期化の完了後に、追加の小売データをコンフィギュレーションする必要があります。 次にいくつか例を挙げます。

- 小売パラメーター
- 小売用スケジューラのパラメーター
- 小売チャンネル
- レジスターとデバイス
- 品揃え

---
title: 新しい Commerce 環境におけるシード データの初期化
description: この記事では、Dynamics 365 Commerce の初期化プロセスの一部として作成されるデータについて説明します。
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
ms.openlocfilehash: 24d4d49c51738203bb89a9844d57f644b8afd4b7
ms.sourcegitcommit: 0d7b700950b1f95dc030ceab5bbdfd4fe1f79ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284382"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a>新しい Commerce 環境におけるシード データの初期化

[!include [banner](includes/banner.md)]

この記事では、Dynamics 365 Commerce の初期化プロセスの一部として作成されるデータについて説明します。

Commerce ソリューションが Microsoft Dynamics Lifecycle Services (LCS) によって配置された後、基本的なコンフィギュレーション データを作成するために、Commerce コンフィギュレーションを初期化する必要があります。

> [!IMPORTANT]
> Commerce コンフィギュレーションを初期化する前に、店舗を設定する法人ごとの言語と住所が指定されていることを確認します。 この手順は、Commerce 用に使用する法人ごとに完了する必要があります。

コンフィギュレーションを初期化するには、次の手順に従います。

1. Commerce クライアントを起動します。
2. **Retail とコマース** &gt; **バックオフィスの設定** &gt; **パラメーター** &gt; **コマース パラメーター**の順にクリックします。
3. **初期化**をクリックします。

初期化によって、次の既定のコンフィギュレーション データを作成します:

- Commerce 用スケジューラ ジョブとサブジョブ
- コマース チャネル スキーマ
- Commerce 配送スケジュール
- ボタン グリッドと画像、テーマを含む、既定の画面レイアウト
- タイムゾーン情報
- 販売時点管理 (POS) 操作
- POS アクセス許可
- チャンネル レポート
- 属性メタデータ
- エンティティ検証テンプレート
- Commerce Data Exchange セッション履歴を削除するバッチ ジョブ

また、Payment Card Industry (PCI) に関連付けられるログが Commerce データベースに対して有効になります。

> [!NOTE]
> 別々に Commerce 用スケジューラをコンフィギュレーションするオプションがあります。 このオプションで、Commerce 用スケジューラのコンフィギュレーションを既定の設定にリセットすることができます。

初期化の完了後に、追加の Commerce データをコンフィギュレーションする必要があります。 次にいくつか例を挙げます。

- コマース パラメーター
- コマース スケジューラのパラメーター
- Commerce チャネル
- レジスターとデバイス
- 品揃え

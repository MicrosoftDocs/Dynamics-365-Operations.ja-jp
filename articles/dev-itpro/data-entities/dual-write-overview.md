---
title: Finance and Operations と Common Data Service 間のほぼリアル タイム データの統合
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations と Common Data Service 間の統合概要を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797231"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a>Finance and Operations と Common Data Service 間のほぼリアル タイム データの統合

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

現在のデジタル世界では、ビジネス エコシステムが全体として Microsoft Dynamics 365 スイートを使用しています。 人材、顧客、運用、およびインターネット オブ シングス (IoT) デバイスからのデータが 1 つのソースに流れ込むため、デジタル フィードバック ループの営業案件があります。 このエクスペリエンスを実現するには、Dynamics 365 for Finance and Operations と Dynamics 365 for Customer Engagement のアプリケーション間の統合が不可欠です。 Customer Engagement アプリケーションは、Common Data Service の上に構築されています。 Finance and Operations データと Common Data Service 間の統合は、Customer Engagement アプリケーションが Finance and Operations に明確で流ちょうに通信できるようにします。

Finance and Operations と Common Data Service は、デュアル書き込みフレームワークを介して、Finance and Operations と Customer Engagement 間のほぼリアルタイムのデータ同期を提供します。 補充は広く、Finance and Operations の 28 の表面領域にまたがります。 目標は、アプリケーション間でビジネス プロセスを接続するシームレスなデータ フローを通じて、「One Dynamics 365」ユーザー エクスペリエンスを提供することです。

![アーキテクチャの概要図](media/dual-write-overview.jpg)

お客様には、以下のバリュー プロポジションを利用できます。

+ [Common Data Service の組織階層](dual-write-organization.md)
+ [Common Data Service 企業理念](dual-write-company.md)
+ [統合済み顧客マスター](dual-write-customer.md)
+ [統合済み仕入先マスター](dual-write-vendor.md)
+ 統合製品マスター

## <a name="system-requirements"></a>システム要件

同期、双方向、ほぼリアル タイムのデータ フローには、次のバージョンが必要です。

+ Microsoft Dynamics 365 for Finance and Operationsバージョン 10.0.4 (2019 年 7 月) プラットフォーム更新プログラム 28 以降
+ Microsoft Dynamics 365 for Customer Engagement、プラットフォーム バージョン 9.1 (4.2) 以降

## <a name="setup-instructions"></a>設定指示

Finance and Operations と Common Data Service 間の統合を設定するには、次の手順に従います。
    
1. デュアル書き込みシステムの設定については、デュアル書き込みプレビューの発表の[ステップ バイ ステップ ガイド](https://aka.ms/dualwrite-docs) を参照してください。
2. [Finance and Operations、Common Data Service、および Customer Engagement 統合](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer グループから、ソリューションをダウンロードしてインストールします。 パッケージには、次の 5 つのソリューションが含まれています。

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. [初期参照データを同期](dual-write-initial.md) の実行順序に従います。
4. デュアル書き込み同期の問題が発生した場合は、[データ統合のトラブルシューティング ガイド](dual-write-troubleshooting.md) を参照してください。

> [!IMPORTANT]
> デュアル書き込みと[見込み客を現金化](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) を並べて実行できません。 見込み客を現金化するソリューションを実行している場合は、アンインストールする必要があります。 また、見込み客の現金化ソルーションの一部である顧客および仕入先のデュアル書き込みテンプレートを無効にする必要があります。

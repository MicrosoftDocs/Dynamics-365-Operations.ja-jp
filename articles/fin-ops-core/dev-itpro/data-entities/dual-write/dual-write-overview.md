---
title: ほぼリアルタイムの Common Data Service とのデータ統合
description: このトピックでは、Finance and Operations と Common Data Service 間の統合概要を提供します。
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019882"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>ほぼリアルタイムの Common Data Service とのデータ統合

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

現在のデジタル世界では、ビジネス エコシステムが全体として Microsoft Dynamics 365 アプリケーションを使用しています。 人材、顧客、運用、およびインターネット オブ シングス (IoT) デバイスからのデータが 1 つのソースに流れ込むため、デジタル フィードバック ループの営業案件があります。 このエクスペリエンスを実現するには、Finance and Operations アプリとその他の Dynamics 365 アプリケーション間の統合が不可欠です。 一部のアプリケーションは、Common Data Service の上に構築されています。 Finance and Operations アプリ データと Common Data Service 間の統合により、他のアプリケーションが一貫して流ちょうに Finance and Operations と通信できるようになります。

Finance and Operations アプリと Common Data Service は、デュアル書き込みフレームワークを介して、Finance and Operations アプリとその他の Dynamics 365 アプリケーション間のほぼリアルタイムのデータ同期を提供します。 範囲は広く、アプリケーションの 28 の表面領域にまたがります。 目標は、アプリケーション間でビジネス プロセスを接続するシームレスなデータ フローを通じて、「One Dynamics 365」ユーザー エクスペリエンスを提供することです。

![アーキテクチャの概要図](media/dual-write-overview.jpg)

以下のバリュー プロポジションを利用できます。

+ [Common Data Service の組織階層](organization-mapping.md)
+ [Common Data Service 企業理念](company-data.md)
+ [統合済み顧客マスター](customer-mapping.md)
+ [統合された元帳](ledger-mapping.md)
+ [統一された製品経験](product-mapping.md)
+ [統合済み仕入先マスター](vendor-mapping.md)
+ [統合されたサイトおよび倉庫](sites-warehouses-mapping.md)
+ [統合された税マスター](tax-mapping.md)

## <a name="system-requirements"></a>システム要件

同期、双方向、ほぼリアル タイムのデータ フローには、次のバージョンが必要です。

+ Microsoft Dynamics 365 for Finance and Operationsバージョン 10.0.4 (2019 年 7 月) プラットフォーム更新プログラム 28 以降
+ Microsoft Dynamics 365 for Customer Engagement、プラットフォーム バージョン 9.1 (4.2) 以降

## <a name="setup-instructions"></a>設定指示

Finance and Operations アプリと Common Data Service 間の統合を設定するには、次の手順に従います。
    
1. デュアル書き込みシステムの設定については、デュアル書き込みプレビューの発表の[ステップ バイ ステップ ガイド](https://aka.ms/dualwrite-docs) を参照してください。
2. [デュアル書き込みを介して Finance and Operations および CDS/CE の統合](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer グループからソリューションをダウンロードおよびインストールします。 パッケージには、次の 5 つのソリューションが含まれています。

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. [初期参照データを同期](initial-sync.md) の実行順序に従います。
4. デュアル書き込み同期の問題が発生した場合は、[データ統合のトラブルシューティング ガイド](dual-write-troubleshooting.md) を参照してください。

> [!IMPORTANT]
> デュアル書き込みと[見込み客を現金化](../../../../supply-chain/sales-marketing/prospect-to-cash.md) を並べて実行できません。 見込み客を現金化するソリューションを実行している場合は、アンインストールする必要があります。 また、見込み客の現金化ソルーションの一部である顧客および仕入先のデュアル書き込みテンプレートを無効にする必要があります。

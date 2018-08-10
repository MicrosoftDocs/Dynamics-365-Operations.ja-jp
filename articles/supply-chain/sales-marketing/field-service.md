---
title: "Microsoft Dynamics 365 for Field Service との統合"
description: "このトピックでは、Microsoft Dynamics 365 for Field Service との統合の概要を示します。"
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: ja-jp
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Microsoft Dynamics 365 for Field Service との統合

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations は、Finance and Operations および Microsoft Dynamics 365 for Field Service 間の業務プロセスの同期を有効にします。 統合シナリオは、業務プロセスの同期を有効にするため、拡張データ インテグレーター テンプレートおよび Common Data Service (CD) を使用して構成します。

[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/field-service-integration.png)](./media/field-service-integration.png)

Field Service および Finance and Operations の統合の第 1 のフェーズは、Field Service のワーク オーダーおよび契約を Finance and Operations で請求できるようにすることに重点を置いています。 Field Service でサポートされているフローが開始され、ワーク オーダーの情報が Finance and Operations に販売注文として同期されます。 Finance and Operations では、請求書ドキュメントを生成するために販売注文が請求されます。 さらに、Field Service 契約請求書からの情報は Finance and Operations に同期されます。 Microsoft Dynamics 365 データ インテグレーターは、カスタマイズ可能なプロジェクトを使用してデータを同期します。 標準テンプレートを使用してカスタム統合プロジェクトを作成し、追加の標準フィールドとカスタム フィールド、およびエンティティをマップして統合を調整し、特定の要件を満たすことができます。

Field Service および Finance and Operations 統合の第 1 のフェーズは、次の項目の同期を有効にします。

- [製品タイプ情報を含む Field Service の製品への Finance and Operations の製品](field-service-product.md)
- [Finance and Operations の販売注文への Field Service のワーク オーダー](field-service-work-order.md)
- [Finance and Operations の自由書式の請求書への Field Service の契約の請求書](field-service-invoice.md)

Field Service および Finance and Operations 間のワーク オーダーを同期する方法の例を表示するには、短い YouTube ビデオ [Dynamics 365 for Field Service および Finance and Operations 間のワーク オーダーを同期する](https://www.youtube.com/watch?v=hAB4TDVMjxU)をご覧ください。

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations のシステム要件
Field Service 統合は、次のバージョンがサポートされています。

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) またはそれ以降

- Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) は 2018 年 4 月にリリースされ、アプリケーション ビルド番号 8.0.30.8020、プラットフォーム更新プログラム 15 (7.0.4841.35234) となっています。 

## <a name="system-requirements-for-field-service"></a>Field Service のシステム要件
Field Service 統合ソリューションを使用するには、以下のコンポーネントをインストールする必要があります:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 またはそれ以降

- Dynamics 365 for Field Service バージョン 1612 (9.0.1.733) (DB 9.0.1.733) オンラインまたはそれ以降のバージョン。
- Dynamics 365 for Sales バージョン 1.15.0.1 またはそれ以降のバージョンの見込顧客を現金化 (P2C) するソリューション。 このソリューションは、[AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) からダウンロードできます。
- Dynamics 365 バージョン 1.0.0.0 またはそれ以降のバージョンの Field Service 統合ソリューション。 このソリューションは、[AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration) からダウンロードできます。


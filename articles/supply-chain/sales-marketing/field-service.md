---
title: Microsoft Dynamics 365 for Field Service との統合
description: このトピックでは、Microsoft Dynamics 365 for Field Service との統合の概要を提供します。
author: ChristianRytt
manager: AnnBe
ms.date: 02/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: efda4e39f63155785386ecec6d21973e01a0f69f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564026"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Microsoft Dynamics 365 for Field Service との統合

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations は、Finance and Operations および Microsoft Dynamics 365 for Field Service 間の業務プロセスの同期を有効にします。 統合シナリオは、業務プロセスの同期を有効にするため、拡張データ インテグレーター テンプレートおよび Common Data Service (CDS) を使用して構成します。
標準テンプレートを使用してカスタム統合プロジェクトを作成し、追加の標準フィールドとカスタム フィールド、およびエンティティをマップして統合を調整して、特定のビジネス ニーズを満たすことができます。 

Field Service 統合は、既存の見込顧客の現金化機能の上に構築します。

![Finance and Operations および Field Service 間の業務プロセスの同期](./media/field-service-integration.png)

Field Service および Finance and Operations の統合の第 1 のフェーズは、Field Service のワーク オーダーおよび契約を Finance and Operations で請求できるようにすることに重点を置いています。 Field Service でサポートされているフローが開始され、ワーク オーダーの情報が Finance and Operations に販売注文として同期されます。 Finance and Operations では、請求書ドキュメントを生成するために販売注文が請求されます。 さらに、Field Service 契約請求書からの情報は Finance and Operations に同期されます。 Microsoft Dynamics 365 データ インテグレーターは、カスタマイズ可能なプロジェクトを使用してデータを同期します。 標準テンプレートを使用してカスタム統合プロジェクトを作成し、追加の標準フィールドとカスタム フィールド、およびエンティティをマップして統合を調整し、特定の要件を満たすことができます。

Field Service および Finance and Operations 統合の第 1 のフェーズは、次の項目の同期を有効にします。

- [製品タイプ情報を含む Field Service の製品への Finance and Operations の製品](field-service-product.md)
- [Finance and Operations の販売注文への Field Service のワーク オーダー](field-service-work-order.md)
- [Finance and Operations の自由書式の請求書への Field Service の契約の請求書](field-service-invoice.md)

Field Service および Finance and Operations 間のワーク オーダーを同期する方法の例を表示するには、短い YouTube ビデオ [ワーク オーダーを Microsoft Dynamics 365 の統合に同期する方法](https://www.youtube.com/watch?v=46ylO7raZAo) をご覧ください。

## <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>在庫およびプロジェクト情報を含む、Microsoft Dynamics 365 for Field Service との統合

この第 2 のフェーズの追加機能では、フィールド技術者に Finance and Operations からの在庫情報について洞察を与え、在庫レベルを更新し、材料を移動できるようにすることに重点を置いています。 さらに、販売品を設置またはサービスする会社は、プロジェクトからの統合により、販売およびサービスの全プロセスをより適切に管理および可視化することができます。

### <a name="functionality-includes-integration-of"></a>機能には、以下の統合が含まれています:
- 倉庫の情報
- 手持在庫情報
- 在庫移動
- 在庫調整
- Dynamics 365 for Field Service のワーク オーダーと接続した Dynamics 365 for Finance and Operations プロジェクト
- Dynamics 365 for Finance and Operations プロジェクトへのリンクを含む Dynamics 365 for Field Serviceワーク オーダーは、このプロジェクト番号を Dynamics 365 for Finance and Operations 販売注文に適用して、プロジェクトからの請求を可能にします。 

![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Field Service および Finance and Operations 統合の第 2 のフェーズは、次のテンプレートとの同期を有効にします:
- 倉庫 (Finance and Operations から Field Service) - Finance and Operations から Field Service への倉庫 [高度なクエリ] 
- 製品在庫 (Finance and Operations から Field Service) - Finance and Operations から Field Service への在庫レベル情報 [高度なクエリ] 
- 在庫調整 (Field Service から Finance and Operations) - Field Service から Finance and Operations への在庫調整 [高度なクエリ] 
- 在庫移動 (Field Service から Finance and Operations) - Field Service から Finance and Operations への在庫移動 [高度なクエリ] 
- プロジェクト (Finance and Operations から Field Service) - Finance and Operations から Field Service へのプロジェクト リスト [高度なクエリ] 
- プロジェクトのワーク オーダー (Field Service から Finance and Operations) - プロジェクトへのサポートを含む、Finance and Operations の販売注文に対する Field Service のワーク オーダー [高度なクエリ] 
- Field Service 製品と在庫単位 (Finance and Operations から Sales) - Field Service への、在庫単位を含む Finance and Operations の「販売可能なリリース済製品」から Sales 「製品」 

## <a name="system-requirements"></a>システム要件

### <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations のシステム要件
Field Service 統合は、次のバージョンがサポートされています。

- Dynamics 365 for Finance and Operations バージョン 8.1.2 (2018 年 12 月) は、2018 年 12 月にリリースされ、アプリケーション ビルド番号 8.1.195、プラットフォーム更新 22 (7.0.5095) となっています。 

### <a name="system-requirements-for-field-service"></a>Field Service のシステム要件
Field Service 統合ソリューションを使用するには、以下のコンポーネントをインストールする必要があります:

- Field Service for Dynamics 365 (バージョン 8.2.0.286) または、Dynamics 365 9.1.x のそれ以降のバージョン - 2018 年 11 月リリース
- Dynamics 365 バージョン 1.15.0.1 またはそれ以降のバージョンの見込顧客を現金化 (P2C) するソリューション。 このソリューションは、[AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) からダウンロードできます。
- Dynamics 365 の「Field Service 統合、プロジェクトと在庫」ソリューション、バージョン 2.0.0.0 またはそれ以降のバージョン。 このソリューションは、[AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2) からダウンロードできます。

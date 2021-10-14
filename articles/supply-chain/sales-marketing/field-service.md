---
title: Microsoft Dynamics 365 Field Service との統合の概要
description: このトピックでは、Microsoft Dynamics 365 Field Service との統合の概要を提供します。
author: Henrikan
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 23661bca91ccd7b7a04c763e60cfca9a99d62bfa
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566458"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Microsoft Dynamics 365 Field Service との統合の概要

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Supply Chain Management により、Dynamics 365 Supply Chain Management および Dynamics 365 Field Service 間の業務プロセスの同期を有効にします。 統合シナリオは、業務プロセスの同期を有効にするため、拡張データ インテグレーター テンプレートおよび Microsoft Dataverse を使用して構成します。
標準テンプレートを使用してカスタム統合プロジェクトを作成し、追加の標準フィールドとカスタム列、およびテーブルをマップして統合を調整して、特定のビジネス ニーズを満たすことができます。 

Field Service 統合は、既存の見込顧客の現金化機能の上に構築します。

![Supply Chain Management および Field Service 間の業務プロセスの同期。](./media/field-service-integration.png)

Field Service および Supply Chain Management の統合の第 1 のフェーズは、Field Service のワーク オーダーおよび契約を Supply Chain Management で請求できるようにすることに重点を置いています。 Field Service でサポートされているフローが開始され、ワーク オーダーの情報が Supply Chain Management に販売注文として同期されます。 Supply Chain Management では、販売注文は請求書請求書ドキュメントを生成するために請求されます。 さらに、Field Service 契約請求書からの情報は Supply Chain Management に同期されます。 Microsoft Dynamics 365 データ インテグレーターは、カスタマイズ可能なプロジェクトを使用してデータを同期します。 標準テンプレートを使用してカスタム統合プロジェクトを作成し、追加の標準フィールドとカスタム列、およびテーブルをマップして統合を調整し、特定の要件を満たすことができます。

Field Service および Supply Chain Management 統合の第 1 のフェーズは、次の項目の同期を有効にします。

- [Supply Chain Management の製品と Field Service の製品との同期](field-service-product.md)
- [Field Service のワーク オーダーと Supply Chain Management の販売注文との同期](field-service-work-order.md)
- [Field Service の契約の請求書と Supply Chain Management の自由書式の請求書との同期](field-service-invoice.md)

Field Service および Supply Chain Management 間のワーク オーダーを同期する方法の例を表示するには、短い YouTube ビデオ [ワーク オーダーを Microsoft Dynamics 365 の統合に同期する方法](https://www.youtube.com/watch?v=46ylO7raZAo) をご覧ください。

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>在庫およびプロジェクト情報を含む、Field Service との統合

この第 2 のフェーズの追加機能では、フィールド技術者に Supply Chain Management からの在庫情報について洞察を与え、在庫レベルを更新し、材料を移動できるようにすることに重点を置いています。 さらに、販売品を設置またはサービスする会社は、プロジェクトからの統合により、販売およびサービスの全プロセスをより適切に管理および可視化することができます。

### <a name="functionality-includes-integration-of"></a>機能には、以下の統合が含まれています:
- 倉庫の情報
- 手持在庫情報
- 在庫移動
- 在庫調整
- Dynamics 365 Field Service ワーク オーダーに関連付けられた Supply Chain Management のプロジェクト
- Supply Chain Management プロジェクトへのリンクを含む Dynamics 365 Field Service ワーク オーダーは、このプロジェクト番号を販売注文に適用して、プロジェクトからの請求を可能にします。 

![在庫やプロジェクト情報など、Supply Chain Management と Field Service 間のビジネス プロセスを同期します。](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Field Service および Supply Chain Management 統合の第 2 のフェーズは、次のテンプレートとの同期を有効にします:
- 倉庫 (Supply Chain Management から Field Service) - Supply Chain Management の倉庫から Field Service [高度なクエリ] 
- 製品在庫 (Supply Chain Management から Field Service) - Supply Chain Management から Field Service への在庫レベル情報 [高度なクエリ] 
- 在庫調整 (Field Service から Supply Chain Management) - Field Service から Supply Chain Management への在庫調整 [高度なクエリ] 
- 在庫振替 (Field Service から Supply Chain Management) - Field Service から Supply Chain Management への在庫振替 [高度なクエリ] 
- プロジェクト (Supply Chain Management から Field Service) - Supply Chain Management から Field Service へのプロジェクト リスト 
- プロジェクトのワーク オーダー (Field Service から Supply Chain Management) - プロジェクトへのサポートを含む、Supply Chain Management の販売注文に対する Field Service のワーク オーダー [高度なクエリ] 
- Field Service 製品と在庫単位 (Supply Chain Management から Sales) - Field Service への、在庫単位を含む Supply Chain Management の「販売可能なリリース済製品」から Sales 「製品」 

## <a name="system-requirements"></a>システム要件

### <a name="system-requirements-for-supply-chain-management"></a>Supply Chain Management のシステム要件
Field Service 統合は、次のバージョンがサポートされています。

- Dynamics 365 for Finance and Operations バージョン 8.1.2 (2018 年 12 月) は、2018 年 12 月にリリースされ、アプリケーション ビルド番号 8.1.195、プラットフォーム更新 22 (7.0.5095) となっています。 

### <a name="system-requirements-for-field-service"></a>Field Service のシステム要件
Field Service 統合ソリューションを使用するには、以下のコンポーネントをインストールする必要があります:

- Field Service (バージョン 8.2.0.286) または、Dynamics 365 9.1.x のそれ以降のバージョン - 2018 年 11 月リリース
- Dynamics 365 バージョン 1.15.0.1 またはそれ以降のバージョンの見込顧客を現金化 (P2C) するソリューション。 このソリューションは、[AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) からダウンロードできます。
- Dynamics 365 の「Field Service 統合、プロジェクトと在庫」ソリューション、バージョン 2.0.0.0 またはそれ以降のバージョン。 このソリューションは、[AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2) からダウンロードできます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
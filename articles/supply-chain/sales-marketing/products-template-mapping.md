---
title: "Finance and Operations の製品を売上の製品に同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition の製品を Microsoft Dynamics 365 for Sales の製品に同期するときに使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 405a6cf9f3e6cc52925ff7d9f10836196343c36b
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>Finance and Operations の製品を売上の製品に同期

[!include[banner](../includes/banner.md)]

> [!NOTE]
> 見込顧客を現金化するソリューションを使用する前に、[Dynamics 365 データ統合](/common-data-service/entity-reference/dynamics-365-integration) をよく理解しておく必要があります。 

このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition の製品を Microsoft Dynamics 365 for Sales の製品に同期するときに使用されるテンプレートと基本的なタスクについて説明します。

## <a name="template-and-task"></a>テンプレートおよびタスク

次のトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations) から Microsoft Dynamics 365 for Sales (Sales) に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

-   テンプレートの名前: 製品 (Finance and Operations から売上)

-   プロジェクトのタスク名: 製品

製品を同期する前に必要なタスクの同期: なし

## <a name="entity-set"></a>エンティティ セット

| **Finance and Operations** | **CDS** | **販売**  |
|----------------------------|---------|------------|
| 販売可能なリリース済製品 | 品目 | 製品   |

## <a name="entity-flow"></a>エンティティのフロー

製品は Finance and Operations で管理され、売上に同期されます。 Finance and Operations のデータ エンティティ、**販売可能な製品**のみを輸出します。つまり、製品には、販売注文で使用する必要のある情報があります。 [リリースされた製品] ページで [検証] 機能を使用して製品を検証する場合も、同じルールが適用されます。

[製品番号] がキーとして使用されます。これは、製品バリアントが [製品バリアント] ごとの個別の [Product IDs] で CDS と売上に同期されることを意味します。

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

売上では、製品の新しいフィールド、[外部管理] が追加され、特定の製品が外部で維持されていることを示します。 値は、デフォルトでは、売上へのインポート時に [はい] に設定されます。

-   **外部管理が = はい**: 製品が Finance and Operations に由来し、売上では編集できません。

-   **外部で管理 = いいえ**: 製品は売上に直接入力します。

-   **外部で管理を = 空白**: 見込顧客を現金化するソリューションを有効にする前に、製品が販売に存在します。

**外部管理**情報を使用して、[外部で管理された製品] で [見積] と [販売注文] のみが Finance and Operations に確実に同期するようにします。

**外部管理の製品**が、同じ通貨で最初に有効な**価格リスト**に自動的に追加されます。 このリストでは、**名前**がアルファベット順で構成されています。 Finance and Operations の製品販売価格は**価格リスト**の価格として使用されています。 これは、Finance and Operations の**製品の販売通貨**ごとに、売上の**価格リスト**を必要とすることを意味します。 リリースされた販売可能商品の通貨は、製品が輸出される法人の会計通貨に設定されます。

> [!NOTE]
> 製品の同期は、一致する通貨を含む**価格リスト**なしでは成功しません。

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

-   一番最初の同期を実行する前に、Finance and Operation の既存製品に対して [特徴的製品テーブル] を入力する必要があります。 このジョブが完了するまで、既存の製品は同期されません。

    -   Finance and Operations の場合は、[検索] を使用し、[特徴的製品テーブルの設定] を検索します。

    -   [特徴的製品テーブルの設定] をクリックし、ジョブを実行します。 このジョブは、1 回のみ実行する必要があります。

-   **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure** の順に検索できる Finance and Operations で **Unit of measure** (UOM) を販売する上で必要となる **ValueMap** を確認します。

-   **ソース \> CD** の順に移動し、[CDS の組織 ID (Organization_OrganizationId)] を更新します。

    -   テンプレート値のデフォルトは ORG001 です。

-   **CD -\>出力先**の順に移動し、**単位グループ** (**defaultuomscheduleid.name**) の **ValueMap** を更新し、売上の**単位グループ**に一致させます。

    -   テンプレート値のデフォルトは**既定単位**です。

-   **CDS 候補リスト**値を使用し、Finance and Operations の UOM を販売するすべての製品が売上に存在することを確認します。

-   **価格表** が、Finance and Operations の製品販売通貨ごとに売上に存在することを確認します。

-   製品は、ステータスが**ドラフト**または**有効**である売上で作成することができます。 これは、売上にある**売上**の**システム設定**で管理できます。

    -   ドラフト ステータスで作成された製品は、**見積**または**販売注文**に追加する前にアクティブ化する必要があります。

## <a name="template-mapping-in-data-integrator"></a>データ インテグレーターでテンプレートのマッピング

次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。

![データ インテグレーターのテンプレートのマッピング](./media/products-template-mapping-data-integrator-1.png)

![データ インテグレーターの製品のテンプレート マッピング](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>関連トピック

[Finance and Operations で売上勘定を顧客に同期する](accounts-template-mapping.md)

[Finance and Operations の連絡先または顧客への Sales の連絡先の同期](contacts-template-mapping.md)

[販売見積ヘッダーおよび明細行の Sales から Finance and Operations への同期](sales-quotation-template-mapping.md)

[販売注文ヘッダーおよび明細行の Finance and Operations から Sales への同期](sales-order-template-mapping.md)

[売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への同期](sales-invoice-template-mapping.md)



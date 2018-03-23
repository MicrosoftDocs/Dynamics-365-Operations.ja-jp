---
title: "Sales から Finance and Operations の顧客への勘定の直接同期"
description: "このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition に勘定を同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 0d409b3b7f19ca31d9c720bca191f1ddba81caa3
ms.openlocfilehash: 5dede6024dcd7837dd4e94ecca2ccd059b11b5b9
ms.contentlocale: ja-jp
ms.lasthandoff: 03/13/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>Sales から Finance and Operations の顧客への勘定の直接同期

[!include[banner](../includes/banner.md)]

> [!NOTE]
> 見込顧客を現金化するソリューションを使用する前に、[Dynamics 365 データ統合](/common-data-service/entity-reference/dynamics-365-integration) をよく理解しておく必要があります。

このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition に勘定を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。

## <a name="data-flow-in-prospect-to-cash"></a>見込み客の現金化へのデータフロー

見込み客の現金化ソリューションは、Finance and Operations と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。  データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書データの流れを可能にします。 次の図は、Finance and Operations と Sales の間でデータを同期させる方法を示しています。

[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

利用可能なテンプレートにアクセスするには、[PowerApps 管理者センター](https://preview.admin.powerapps.com/dataintegration) を開きます。 **プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。

Sales から Finance and Operations への勘定同期には、以下のテンプレートと基本的なタスクが使用されます。

- **データ統合におけるテンプレートの名前:**  勘定 (Sales からFinance and Operations ) - 直接
- **プロジェクトのタスクの名前:** - 勘定 - 顧客

アカウント/顧客の同期が発生する前に、同期タスクは必要ありません。

## <a name="entity-set"></a>エンティティ セット

| 売上    | Finance and Operations |
|----------|------------------------|
| 口座 | 顧客 V2           |

## <a name="entity-flow"></a>エンティティのフロー

勘定は Sales で管理され、Finance and Operations に顧客として同期されます。 これらの顧客の **外部管理** プロパティを **はい** に設定し、Sales から生成される顧客を追跡します。 請求時に、この情報は、売上に同期される請求書のフィルター処理に使用されます。

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

**勘定番号**フィールドは、**勘定**ページで利用できます。 統合をサポートするため固有なナチュラル キーとなっています。 顧客関係管理 (CRM) ソリューションのナチュラル キー機能は、すでに **勘定番号** フィールドを使用しているが、勘定ごとに一意の **勘定番号** 値を使用していない顧客に影響する可能性があります。 現時点では、統合ソリューションは、このケースをサポートしていません。

新しいアカウントが作成され、**勘定番号**値が存在しない場合、番号順序を使用して自動的に生成されます。 その値は**勘定**で構成され、続いて番号順序が増加し、6 文字の接尾辞が続きます。 次に例を示します: **ACC-01000-BVRCPS**

売上の統合ソリューションが適用されている場合、アップグレード スクリプトにより、売上の既存のアカウントの、**勘定番号**フィールドが設定されます。 **勘定番号** 値がない場合は、前述した番号順序を使用します。

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

- **CustomerGroupId** マッピングは、Finance and Operations で有効な値に更新する必要があります。 既定値を指定するか、値マップを使用して値を設定できます。

    既定のテンプレートの値は **10** です。

- 次のマッピングを追加することによって、Finance and Operations で必要な手動更新の数を減らすことができます。 たとえば、**国/地域**または**市町村**のデフォルト値または値マップを使用できます。

    - **SiteId** – Finance and Operations で見積書および販売注文を生成するにはサイトが必要です。 デフォルトのサイトは、製品から、または注文ヘッダーの顧客から取得できます。

        既定のテンプレートの値は **1** です。

    - **WarehouseId** – Finance and Operations で見積書および販売注文を処理するには倉庫が必要です。 デフォルト倉庫は、製品から、または Finance and Operations の受注ヘッダーの顧客から取得できます。

        既定のテンプレートの値は **13** です。

    - **LanguageId** – Finance and Operations で見積書および販売注文を生成するには言語が必要です。 既定では、顧客からの注文ヘッダの言語が使用されます。

        既定のテンプレートの値は **アメリカ英語** です。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

> [!NOTE]
> [支払条件]、[運賃条件]、[配送条件]、[送付方法]、および [配送モード] フィールドは、既定のマッピングには含まれていません。 これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。

次の図は、データ統合のテンプレート マッピングの例を示しています。 

> [!NOTE]
> マッピングは、Sales から Finance and Operations にどのフィールド情報を同期するかを表示します。

![データ統合のテンプレートのマッピング](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>関連トピック


[見込顧客を現金化](prospect-to-cash.md)

[Sales から Finance and Operations の顧客への勘定の直接同期](accounts-template-mapping-direct.md)

[Sales から Finance and Operations の連絡先または顧客への連絡先の直接同期](contacts-template-mapping-direct.md)

[販売注文ヘッダーおよび明細行の Finance and Operations から Sales への直接同期](sales-order-template-mapping-direct-two-ways.md)

[売上請求書ヘッダーおよび直接明細行の Finance and Operations から Sales への直接同期](sales-invoice-template-mapping-direct.md)



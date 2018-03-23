---
title: "Sales から Finance and Operations の連絡先または顧客への連絡先の直接同期"
description: "このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition に対して、連絡先 (連絡先) と連絡先 (顧客) エンティティを同期するために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: 6269b73dfca46d455784046199463d3f86e653ae
ms.contentlocale: ja-jp
ms.lasthandoff: 03/13/2018

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Sales から Finance and Operations の連絡先または顧客への連絡先の直接同期

[!include[banner](../includes/banner.md)]

> [!NOTE]
> 見込顧客を現金化するソリューションを使用する前に、[Dynamics 365 データ統合](/common-data-service/entity-reference/dynamics-365-integration) をよく理解しておく必要があります。

このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition に対して、連絡先 (連絡先) と連絡先 (顧客) エンティティを直接同期するために使用されるテンプレートと基本的なタスクについて説明します。

## <a name="data-flow-in-prospect-to-cash"></a>見込み客の現金化へのデータフロー

見込み客の現金化ソリューションは、Finance and Operations と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。 データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書データの流れを可能にします。 次の図は、Finance and Operations と Sales の間でデータを同期させる方法を示しています。

[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

利用可能なテンプレートにアクセスするには、[PowerApps 管理者センター](https://preview.admin.powerapps.com/dataintegration) を開きます。 **プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。

Sales から Finance and Operations へ連絡先 (連絡先) エンティティと連絡先 (顧客) エンティティを同期するには、以下のテンプレートと基本的なタスクが使用されます。

- **データ統合でのテンプレートの名前:**

    - 連絡先 (Sales から Finance and Operations) - 直接
    - 連絡先から顧客 (Sales から Finance and Operations) - 直接

- **データ統合プロジェクトのタスク名:**

    - 連絡先
    - ContactToCustomer

連絡先の同期には、まず次の同期タスクが必要です。 勘定 (Sales から Finance and Operations)

## <a name="entity-sets"></a>エンティティ セット

| 売上    | Finance and Operations |
|----------|------------------------|
| 連絡先 | CDS 連絡先           |
| 連絡先 | 顧客 V2           |

## <a name="entity-flow"></a>エンティティのフロー

連絡先は Sales で管理され、Finance and Operations に同期されます。

Sales の連絡先は Finance and Operations の連絡先または顧客になります。 Sales の連絡先を Finance and Operations の連絡先または顧客として同期する必要があるかどうかを判断するために、システムは Sales の連絡先の次のプロパティを調べます。

- **Finance and Operations の顧客への同期:** [有効な顧客] が [はい] に設定されている連絡先
- **Finance and Operations の連絡先との同期:** [有効な顧客] が [いいえ] に設定され、**会社** (親勘定/連絡先) がアカウント (連絡先ではない) を表す連絡先

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

新しい [有効な顧客] フィールドが連絡先に追加されました。 このフィールドは、営業活動を持つ連絡先と営業活動を持たない連絡先を区別するために使用されます。 [有効な顧客] は、関連する見積書、注文、または請求書を持つ連絡先に対してのみ [はい] に設定されます。 これらの連絡先のみが顧客として Finance and Operations に同期されます。

新しい [IsCompanyAnAccount] フィールドが連絡先に追加されました。 このフィールドは、連絡先が**アカウント**タイプの会社 (親勘定/連絡先) にリンクされているかどうかを示します。 この情報は、Finance and Operations の連絡先として同期する必要がある連絡先を識別するために使用されます。

新しい [連絡先番号] フィールドが連絡先に追加され、統合をサポートするための固有のナチュラル キーが保証されます。 新しい連絡先が作成されると、**連絡先番号**値は、番号順序を使用して自動的に生成されます。 値は **CON** で構成され、続いて番号順序が増加し、6 文字の接尾辞が続きます。 次に例を示します: **CON-01000-BVRCPS**

Sales の統合ソリューションが適用されている場合、アップグレード スクリプトは、先に述べた番号順序を使用して、既存の連絡先の [連絡先番号] フィールドを設定します。 また、アップグレード スクリプトでは、営業活動を持っている任意の連絡先の [有効な顧客] フィールドが [はい] に設定されます。

## <a name="in-finance-and-operations"></a>Finance and Operations

[IsContactPersonExternallyMaintained] プロパティを使用し、連絡先をタグ付けします。 このプロパティは、指定された連絡先が外部で管理されていることを示します。 この場合、外部で管理されている連絡先は Sales に保持されます。

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

### <a name="contact-to-customer"></a>連絡先から顧客へ

- **CustomerGroup** は Finance and Operations で必須です。 同期エラーを防ぐために、マッピングで既定値を指定できます。 販売でこのフィールドが空白の場合、既定値が使用されます。

    既定のテンプレートの値は **10** です。

- 次のマッピングを追加することによって、Finance and Operations で必要な手動更新の数を減らすことができます。 たとえば、**国/地域**または**市町村**のデフォルト値または値マップを使用できます。

    - **SiteId** – Finance and Operations の製品に対して既定のサイトを定義することもできます。 Finance and Operations で見積書および販売注文を生成するにはサイトが必要です。

        **SiteId** のテンプレートの値が定義されていません。

    - **WarehouseId** – Finance and Operations の製品に対して既定の倉庫を定義することもできます。 Finance and Operations で見積書および販売注文を生成するには倉庫が必要です。

        **WarehouseId** のテンプレートの値が定義されていません。

    - **LanguageId** – Finance and Operations で見積書および販売注文を生成するには言語が必要です。
    
        既定のテンプレートの値は **アメリカ英語** です。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングの例を示しています。 

> [!NOTE]
> マッピングは、Sales から Finance and Operations にどのフィールド情報を同期するかを表示します。

### <a name="contact-to-contact"></a>連絡先から連絡先へ

![データ インテグレーターのテンプレートのマッピング](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>連絡先から顧客へ

![データ インテグレーターのテンプレートのマッピング](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>関連トピック

[見込顧客を現金化](prospect-to-cash.md)

[Sales から Finance and Operations の顧客への勘定の直接同期](accounts-template-mapping-direct.md)

[Sales 製品への Finance and Operations 製品の直接同期](products-template-mapping-direct.md)

[販売注文ヘッダーおよび明細行の Finance and Operations から Sales への直接同期](sales-order-template-mapping-direct-two-ways.md)

[売上請求書ヘッダーおよび直接明細行の Finance and Operations から Sales への直接同期](sales-invoice-template-mapping-direct.md)




---
title: "売上の連絡先を Finance and Operations の連絡先または顧客に同期させる"
description: "このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition に対して、連絡先 (連絡先) と連絡先 (顧客) を同期するために使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.openlocfilehash: c838fef502f643c764fade9cd79ae770ffc36974
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>売上の連絡先を Finance and Operations の連絡先または顧客に同期させる

[!include[banner](../includes/banner.md)]

> [!NOTE]
> 見込顧客を現金化するソリューションを使用する前に、[Dynamics 365 データ統合](/common-data-service/entity-reference/dynamics-365-integration) をよく理解しておく必要があります。 

このトピックでは、Microsoft Dynamics 365 for Sales (Sales) から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations) に対して、連絡先 (連絡先) エンティティと連絡先 (顧客) を同期するために使用されるテンプレートと基本的なタスクについて説明します。

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

売上から Finance and Operations へ連絡先 (連絡先) と連絡先 (顧客) を同期するには、以下のテンプレートと基本的なタスクが使用されます。

- **テンプレートの名前:**

    - 連絡先 (Sales から Finance and Operations)
    - 連絡先から顧客 (売上から Finance and Operations)

- **プロジェクトのタスク名:**

    - 連絡先
    - ContactToCustomer

連絡先の同期の前に、次の同期タスクが必要です: 勘定 (売上から Finance and Operations)

## <a name="entity-sets"></a>エンティティ セット

| 売上    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| 連絡先 | 連絡 | CDS 連絡先           |
| 連絡先 | アカウント | 顧客 V2           |

## <a name="entity-flow"></a>エンティティのフロー

連絡先は、販売で管理され、一般的なデータ サービス (CDS) および Finance and Operations に同期されます。

売上の連絡先は CD および Finance and Operations の連絡先になる可能性があります。 また、CDS の勘定および Finance and Operations の顧客になることがあります。 CDS と Finance and Operations に同期する上で、連絡先を売上でピックアップする必要があるかどうかを判断するには (例: 売上の連絡先 &gt; CDS の連絡先 &gt; Finance and Operations の連絡先)、システムは売上の連絡先の次のプロパティを検索します。

- **CDS の勘定と Finance and Operations での顧客への同期:** [**有効な顧客**] が [**はい**] に設定されている連絡先
- **CDS の連絡先と Finance and Operations の連絡先との同期:** [**有効な顧客**] が [**いいえ**] に設定され、**会社** (親勘定/連絡先) がアカウント (連絡先ではない) を表す連絡先

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション 

新しい [**有効な顧客**] フィールドが連絡先に追加されました。 このフィールドは、営業活動を持つ連絡先と営業活動を持たない連絡先を区別するために使用されます。 [**有効な顧客**] は、関連する見積書、注文、または請求書を持つ連絡先に対してのみ [**はい**] に設定されます。 これらの連絡先のみが顧客として Finance and Operations に同期されます。

新しい [**IsCompanyAnAccount**] フィールドが連絡先に追加されました。 このフィールドは、連絡先が**アカウント** タイプの会社 (親アカウント/連絡先) にリンクされているかどうかを示すために使用されます。 この情報は、Finance and Operations の連絡先として同期する必要がある連絡先を識別するために使用されます。

新しい [**連絡先番号**] フィールドが連絡先に追加され、統合をサポートするための自然で固有のキーが保証されます。 新しい連絡先が作成されると、**連絡先番号**値は、番号順序を使用して自動的に生成されます。 値は **CON** で構成され、続いて番号順序が増加し、6 文字の接尾辞が続きます。 次に例を示します: **CON-01000-BVRCPS**

売上の統合ソリューションが売上に追加されると、アップグレード スクリプトは、先に説明した番号シーケンスを使用して、既存の連絡先の [**連絡先番号**] フィールドを設定します。 また、アップグレード スクリプトでは、営業活動を持っている任意の連絡先の [**有効な顧客**] フィールドが [**はい**] に設定されます。

## <a name="in-finance-and-operations"></a>Finance and Operations 

[**IsContactPersonExternallyMaintained**] プロパティを使用し、連絡先をタグ付けします。 このプロパティは、指定された連絡先が外部で管理されていることを示します。 この場合、外部で管理されている連絡先は売上に保持されます。

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

### <a name="contact-to-contact"></a>連絡先から連絡先へ

- **ソース&gt; CDS** マッピングの順に **CDS 組織 ID** を更新します。

    - **Organization_OrganizationId [Organization ID]** の既定のテンプレート値は [**ORG001**] です。
    - **PrimaryAccount_Organization_OrganizationId [Organization ID]** の既定のテンプレート値は [**ORG001**] です。

- **住所/国の地域コード** は Finance and Operations では必須です。 同期エラーを回避するために、**CDS &gt; Operations** マッピングで既定値を指定できます。 販売でこのフィールドが空白の場合、既定値が使用されます。 **PrimaryAddressCountryRegionISOCode** の既定のテンプレート値は **USA** です。
- Finance and Operation に次のフィールドの値が存在することを確認します。 この情報が Finance and Operations で必要ではない場合は、**CD&gt; 出力先** マッピングの順にマッピングを削除できます。

    - **Finance and Operations のフィールド名:** 意思決定
    - **マッピング:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>連絡先から顧客へ

- **ソース&gt; CDS** マッピングの順に **CDS 組織 ID** を更新します。 **Organization_OrganizationId [Organization ID]** の既定のテンプレート値は [**ORG001**] です。
- **住所/国の地域コード** は Finance and Operations では必須です。 同期エラーを回避するために、**CDS &gt; 出力先** マッピングの順に既定値を指定できます。 販売でこのフィールドが空白の場合、既定値が使用されます。 **PrimaryAddressCountryRegionISOCode** の既定のテンプレート値は **USA** です。
- **CustomerGroup** は Finance and Operations で必須です。 同期エラーを回避するために、**CDS &gt; 出力先** マッピングの順に既定値を指定できます。 販売でこのフィールドが空白の場合、既定値が使用されます。 **CustomerGroupId** の既定のテンプレート値は **10** です。
- 次のマッピングを **CD&gt;出力先** から追加することによって、Finance and Operations の手動更新の数を減らすことができます。 たとえば、**国/地域**または**市町村**のデフォルト値または値マップを使用できます。

    - **SiteId** - Finance and Operation の製品に対して既定のサイトを定義することもできます。 Finance and Operations で見積書および販売注文を生成するにはサイトが必要です。 **SiteId** のテンプレートの値が定義されていません。
    - **WarehouseId** - Finance and Operation の製品に対して既定の倉庫を定義することもできます。 Finance and Operations で見積書および販売注文を生成するには倉庫が必要です。 **WarehouseId** のテンプレートの値が定義されていません。
    - **LanguageId** – Finance and Operations で見積書および販売注文を生成するには言語が必要です。 **LanguageId** の既定のテンプレート値は **en-us** です。

## <a name="template-mapping-in-data-integrator"></a>データ インテグレーターでテンプレートのマッピング

次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。

### <a name="contact-to-contact"></a>連絡先から連絡先へ

![データ インテグレーターでテンプレートのマッピング](./media/contacts-template-mapping-data-integrator-1.png)

![データ インテグレーターの連絡先のテンプレート マッピング](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>連絡先から顧客へ

![データ インテグレーターでテンプレートのマッピング](./media/contacts-template-mapping-data-integrator-3.png)

![データ インテグレーターの連絡先のテンプレート マッピング](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>関連トピック

[Finance and Operations の製品を売上の製品に同期する](products-template-mapping.md)

[Finance and Operations で売上勘定を顧客に同期する](accounts-template-mapping.md)

[販売見積ヘッダーおよび明細行の Sales から Finance and Operations への同期](sales-quotation-template-mapping.md)

[販売注文ヘッダーおよび明細行の Finance and Operations から Sales への同期](sales-order-template-mapping.md)

[売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への同期](sales-invoice-template-mapping.md)


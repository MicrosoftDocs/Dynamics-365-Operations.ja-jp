---
title: Supply Chain Management の連絡先または顧客への Sales の連絡先の直接同期
description: このトピックでは、Dynamics 365 Sales から Dynamics 365 Supply Chain Management に連絡先 (連絡先) エンティティと連絡先 (顧客) エンティティを同期するために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1a7f66797dea62a22d93ab105722bb26b4cf94e1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210114"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>Supply Chain Management の連絡先または顧客への Sales の連絡先の直接同期

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 見込顧客を現金化するソリューションを使用する前に、[Common Data Service for Apps へデータを統合](https://docs.microsoft.com/powerapps/administrator/data-integrator) をよく理解しておく必要があります。

このトピックでは、Dynamics 365 Sales から Dynamics 365 Supply Chain Management に連絡先 (連絡先) エンティティと連絡先 (顧客) エンティティを直接同期するために使用されるテンプレートと基本的なタスクについて説明します。

## <a name="data-flow-in-prospect-to-cash"></a>見込み客の現金化へのデータフロー

見込み客の現金化ソリューションは、Supply Chain Management と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。 データ統合機能で利用可能な見込み顧客を現金化するテンプレートにより、Supply Chain Management と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れが可能になります。 次の図は、Supply Chain Management と Sales の間でデータを同期させる方法を示しています。

[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

利用可能なテンプレートにアクセスするには、[PowerApps 管理者センター](https://preview.admin.powerapps.com/dataintegration) を開きます。 **プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。

Sales から Supply Chain Management へ連絡先 (連絡先) エンティティと連絡先 (顧客) エンティティを同期するには、以下のテンプレートと基本的なタスクが使用されます。

- **データ統合でのテンプレートの名前**

    - 連絡先 (Sales から Supply Chain Management) - 直接
    - 顧客への連絡先 (Sales から Supply Chain Management) - ダイレクト

- **データ統合プロジェクトのタスク名**

    - 連絡先
    - ContactToCustomer

連絡先の同期には、まず次の同期タスクが必要です。勘定 (Sales から Supply Chain Management)

## <a name="entity-sets"></a>エンティティ セット

| 販売注文    | サプライ チェーン マネジメント |
|----------|------------------------|
| 連絡先 | CDS 連絡先           |
| 連絡先 | 顧客 V2           |

## <a name="entity-flow"></a>エンティティのフロー

連絡先は Sales で管理され、Supply Chain Management に同期されます。

Sales の連絡先は Supply Chain Management の連絡先または顧客になります。 Sales の連絡先を Supply Chain Management の連絡先または顧客として同期する必要があるかどうかを判断するために、システムは Sales の連絡先の次のプロパティを調べます。

- **Supply Chain Management の顧客への同期:** **有効な顧客**が**はい**に設定されている連絡先
- **Supply Chain Management の連絡先との同期:** **有効な顧客**が**いいえ**に設定され、**会社** (親勘定/連絡先) がアカウント (連絡先ではない) を表す連絡先

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

新しい**有効な顧客**フィールドが連絡先に追加されました。 このフィールドは、営業活動を持つ連絡先と営業活動を持たない連絡先を区別するために使用されます。 **有効な顧客**は、関連する見積書、注文、または請求書を持つ連絡先に対してのみ**はい**に設定されます。 これらの連絡先のみが顧客として Supply Chain Management に同期されます。

新しい **IsCompanyAnAccount** フィールドが連絡先に追加されました。 このフィールドは、連絡先が**アカウント**タイプの会社 (親勘定/連絡先) にリンクされているかどうかを示します。 この情報は、Supply Chain Management の連絡先として同期する必要がある連絡先を識別するために使用されます。

新しい**連絡先番号**フィールドが連絡先に追加され、統合をサポートするための固有のナチュラル キーが保証されます。 新しい連絡先が作成されると、**連絡先番号**値は、番号順序を使用して自動的に生成されます。 値は **CON** で構成され、続いて番号順序が増加し、6 文字の接尾辞が続きます。 次に例を示します: **CON-01000-BVRCPS**

Sales の統合ソリューションが適用されている場合、アップグレード スクリプトは、先に述べた番号順序を使用して、既存の連絡先の**連絡先番号**フィールドを設定します。 また、アップグレード スクリプトでは、営業活動を持っている任意の連絡先の**有効な顧客**フィールドが**はい**に設定されます。

## <a name="in-supply-chain-management"></a>Supply Chain Management 内

**IsContactPersonExternallyMaintained** プロパティを使用し、連絡先をタグ付けします。 このプロパティは、指定された連絡先が外部で管理されていることを示します。 この場合、外部で管理されている連絡先は Sales に保持されます。

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

### <a name="contact-to-customer"></a>連絡先から顧客へ

- Supply Chain Management では**顧客グループ**が必要です。 同期エラーを防ぐために、マッピングで既定値を指定できます。 販売でこのフィールドが空白の場合、既定値が使用されます。

    既定のテンプレートの値は **10** です。

- 次のマッピングを追加することによって、Supply Chain Management で必要な手動更新の数を減らすことができます。 たとえば、**国/地域**または**市町村**のデフォルト値または値マップを使用できます。

    - **SiteId** – Supply Chain Management の製品に対して既定のサイトを定義することもできます。 Supply Chain Management で見積書および販売注文を生成するにはサイトが必要です。

        **SiteId** のテンプレートの値が定義されていません。

    - **WarehouseId** – Supply Chain Management の製品に対して既定の倉庫を定義することもできます。 Supply Chain Management で見積書および販売注文を生成するには倉庫が必要です。

        **WarehouseId** のテンプレートの値が定義されていません。

    - **LanguageId** – Supply Chain Management で見積書および販売注文を生成するには言語が必要です。
    
        既定のテンプレートの値は **アメリカ英語** です。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングの例を示しています。 

> [!NOTE]
> マッピングは、Sales から Supply Chain Management にどのフィールド情報を同期するかを表示します。

### <a name="contact-to-contact"></a>連絡先から連絡先へ

![データ インテグレーターのテンプレートのマッピング](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>連絡先から顧客へ

![データ インテグレーターのテンプレートのマッピング](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>関連トピック

[見込顧客を現金化](prospect-to-cash.md)

[Supply Chain Management の顧客への Sales の勘定の直接同期](accounts-template-mapping-direct.md)

[製品を Supply Chain Management から Sales の製品に直接同期する](products-template-mapping-direct.md)

[販売注文の Sales と Supply Chain Management の間の直接同期](sales-order-template-mapping-direct-two-ways.md)

[売上請求書のヘッダーおよび明細行の Supply Chain Management から Sales への直接同期](sales-invoice-template-mapping-direct.md)



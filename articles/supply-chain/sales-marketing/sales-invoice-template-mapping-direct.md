---
title: 売上請求書のヘッダーおよび明細行の Supply Chain Management から Sales への直接同期
description: このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Sales に売上請求書ヘッダーおよび明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 69f497ed8efff9aa18dedbce65d88e3b2d5168a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839032"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Finance and Operations から Sales への請求書ヘッダーおよび明細行の直接同期

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Sales に売上請求書ヘッダーおよび明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。

## <a name="data-flow-in-prospect-to-cash"></a>見込み客の現金化へのデータフロー

見込み客の現金化ソリューションは、Supply Chain Management と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。 データ統合機能で利用可能な見込み顧客を現金化するテンプレートにより、Supply Chain Management と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れが可能になります。 次の図は、Supply Chain Management と Sales の間でデータを同期させる方法を示しています。

[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

利用可能なテンプレートにアクセスするには、[Power Apps 管理者センター](https://preview.admin.powerapps.com/dataintegration)を開きます。 **プロジェクト** を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。

Supply Chain Management から Sales への販売請求書ヘッダーと明細行の同期には、以下のテンプレートと基本的なタスクが使用されます。

- **データ統合における テンプレートの名前:** 売上請求書 (Finance and Operations から Sales) - 直接
- **データ統合プロジェクトのタスク名:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

販売請求書ヘッダーと明細行を同期させるには、次の同期タスクが必要です。

- 製品 (Supply Chain Management から Sales) - 直接
- 勘定 (Sales から Supply Chain Management) - ダイレクト (使用する場合)
- 連絡先 (Sales から Supply Chain Management) - ダイレクト (使用する場合)
- 販売注文ヘッダーおよび明細行 (Supply Chain Management から Sales) - ダイレクト

## <a name="entity-set"></a>エンティティ セット

| サプライ チェーン マネジメント                              | 販売注文          |
|------------------------------------------------------|----------------|
| 外部的に管理された顧客の売上請求書ヘッダー | 請求書       |
| 外部的に管理された顧客の売上請求書明細行   | InvoiceDetails |

## <a name="entity-flow"></a>エンティティのフロー

売上請求書が Supply Chain Management で作成され、Sales に同期されます。

> [!NOTE]
> 現在、売上請求書ヘッダー上の税に関連する費用は、Supply Chain Managements から Sales への同期には含まれていません。 これは Sales がヘッダー レベルでの税金情報をサポートしていないためです。 ただし、同期の明細行レベルでの税に関連する費用が含まれます。

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

- **請求書番号** フィールドが **請求書** エンティティに追加され、ページに表示されます。
- 請求書が Supply Chain Management で作成され、Sales に同期されるため、**販売注文** ページの **請求書の作成** ボタンは非表示になります。 請求書が Supply Chain Management から同期されるため、**請求書** ページは編集できません。
- Supply Chain Management からの関連請求書が Sales に同期されると、**販売注文状態** 値は自動的に **請求済** に変更されます。 さらに、請求書の作成元である販売注文の所有者は、請求書の所有者として割り当てられます。 したがって、販売注文書の所有者は、請求書を表示することができます。

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

売上請求書を同期する前に、システムで以下の設定を更新する必要があります。

### <a name="setup-in-sales"></a>Sales での設定

**設定** > **管理** > **システムの設定** > **Sales** の順に移動し、次の設定を使用することを確認します。

- **システム プライジング計算システムの使用** オプションが、**はい** に設定されている。
- **割引の計算方法** フィールドが、**明細行品目** に設定されている。

### <a name="setup-in-the-data-integration-project"></a>データ統合プロジェクトでの設定

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader タスク

- **InvoiceCountryRegionId** から **BillingAddress\_Country** に必要なマッピングが存在することを確認します。

    テンプレートの値は、複数の国または地域がマップされている値マップです。

- Sales で請求書を作成するには価格リストが必要です。 Sales で通貨ごとに使用される価格リストへの **pricelevelid.name \[価格リスト名\]** の値マップを更新します。 1つの通貨に対する既定の価格リストを使用することができます。 または、複数の通貨で価格リストがある場合、値マップを使用することもできます。

    **pricelevelid.name\[価格リスト名\]** のテンプレート値は、USD = CRM サービス USA (サンプル) のように通貨に基づく値マップです。  
    
#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine タスク

- **測定単位** で必要なマッピングが存在することを確認します。
- Supply Chain Management の **SalesUnitSymbol** に必要な値マップが存在することを確認して下さい。

    **SalesUnitSymbol** から **Quantity\_** UMO に対して値マップを持つテンプレート値が定義されます。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

> [!NOTE]
> **支払条件**、**運賃条件**、**配送条件**、**送付方法**、および **配送モード** フィールドは、既定のマッピングには含まれていません。 これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。

次の図は、データ統合のテンプレート マッピングの例を示しています。 

> [!NOTE]
> マッピングは、Sales から Supply Chain Management にどのフィールド情報を同期するかを表示します。

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![データ統合のテンプレートのマッピング](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![データ統合のテンプレートのマッピング](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>関連トピック

[見込顧客を現金化](prospect-to-cash.md)

[Supply Chain Management の顧客への Sales の勘定の直接同期](accounts-template-mapping-direct.md)

[製品を Supply Chain Management から Sales の製品に直接同期する](products-template-mapping-direct.md)

[Supply Chain Management の連絡先または顧客への Sales の連絡先の直接同期](contacts-template-mapping-direct.md)

[販売注文の Sales と Supply Chain Management の間の直接同期](sales-order-template-mapping-direct-two-ways.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
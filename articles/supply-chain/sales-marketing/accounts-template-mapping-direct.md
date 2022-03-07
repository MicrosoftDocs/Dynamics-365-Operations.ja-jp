---
title: Supply Chain Management の顧客への Sales の勘定の直接同期
description: このトピックでは、Dynamics 365 Sales から Supply Chain Management に勘定を同期するために使用されるテンプレートと基本的なタスクについて説明します。
author: Henrikan
ms.date: 10/25/2018
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
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: b3257f4582ede6cd1be8e593a5ed99f5ffd0ca6f
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063088"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>Supply Chain Management の顧客への Sales の勘定の直接同期

[!include [banner](../includes/banner.md)]



> [!NOTE]
> 見込顧客を現金化するソリューションを使用する前に、[Microsoft Dataverse for Apps へデータを統合](/powerapps/administrator/data-integrator) をよく理解しておく必要があります。

このトピックでは、Dynamics 365 Sales から Dynamics 365 Supply Chain Management に勘定を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。

## <a name="data-flow-in-prospect-to-cash"></a>見込み客の現金化へのデータフロー

見込み客の現金化ソリューションは、Supply Chain Management と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。  データ統合機能で利用可能な見込み顧客を現金化するテンプレートにより、Supply Chain Management と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れが可能になります。 次の図は、Supply Chain Management と Sales の間でデータを同期させる方法を示しています。

[![見込み客の現金化へのデータフロー。](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

利用可能なテンプレートにアクセスするには、[Power Apps 管理者センター](https://preview.admin.powerapps.com/dataintegration)を開きます。 **プロジェクト** を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。

Sales から Supply Chain Management への勘定同期には、以下のテンプレートと基本的なタスクが使用されます。

- **データ統合におけるテンプレートの名前:**  勘定 (Sales から Fin and Ops) - 直接
- **プロジェクトのタスクの名前:** - 勘定 - 顧客

アカウント/顧客の同期が発生する前に、同期タスクは必要ありません。

## <a name="entity-set"></a>エンティティ セット

| 販売注文    | サプライ チェーン マネジメント |
|----------|------------------------|
| アカウント | 顧客 V2           |

## <a name="entity-flow"></a>エンティティのフロー

勘定は Sales で管理され、Supply Chain Management に顧客として同期されます。 これらの顧客の **外部管理** プロパティを **はい** に設定し、Sales から生成される顧客を追跡します。 請求時に、この情報は、売上に同期される請求書のフィルター処理に使用されます。

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

**勘定番号** 列は、**勘定** ページで利用できます。 統合をサポートするため固有なナチュラル キーとなっています。 顧客関係管理 (CRM) ソリューションのナチュラル キー機能は、すでに **勘定番号** 列を使用しているが、勘定ごとに一意の **勘定番号** 値を使用していない顧客に影響する可能性があります。 現時点では、統合ソリューションは、このケースをサポートしていません。

新しいアカウントが作成され、**勘定番号** 値が存在しない場合、番号順序を使用して自動的に生成されます。 その値は **勘定** で構成され、続いて番号順序が増加し、6 文字の接尾辞が続きます。 次に例を示します: **ACC-01000-BVRCPS**

売上の統合ソリューションが適用されている場合、アップグレード スクリプトにより、売上の既存のアカウントの、**勘定番号** 列が設定されます。 **勘定番号** 値がない場合は、前述した番号順序を使用します。

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

- **CustomerGroupId** マッピングは、Supply Chain Management で有効な値に更新する必要があります。 既定値を指定するか、値マップを使用して値を設定できます。

    既定のテンプレートの値は **10** です。

- 次のマッピングを追加することによって、Supply Chain Management で必要な手動更新の数を減らすことができます。 たとえば、**国/地域** または **市町村** のデフォルト値または値マップを使用できます。

    - **SiteId** – Supply Chain Management で見積書および販売注文を生成するにはサイトが必要です。 デフォルトのサイトは、製品から、または注文ヘッダーの顧客から取得できます。

        既定のテンプレートの値は **1** です。

    - **WarehouseId** – Supply Chain Management で見積書および販売注文を処理するには倉庫が必要です。 デフォルト倉庫は、製品から、または Supply Chain Management の受注ヘッダーの顧客から取得できます。

        既定のテンプレートの値は **13** です。

    - **LanguageId** – Supply Chain Management で見積書および販売注文を生成するには言語が必要です。 既定では、顧客からの注文ヘッダの言語が使用されます。

        既定のテンプレートの値は **en-us** です。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

> [!NOTE]
> **支払条件**、**運賃条件**、**配送条件**、**送付方法**、および **配送モード** 列は、既定のマッピングには含まれていません。 これらの列をマップするには、テーブル間で同期される組織内のデータに固有の値マッピングを設定する必要があります。

次の図は、データ統合のテンプレート マッピングの例を示しています。 

> [!NOTE]
> マッピングは、Sales から Supply Chain Management にどの列情報を同期するかを表示します。

![データ統合のテンプレートのマッピング。](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>関連トピック


[見込顧客の現金化](prospect-to-cash.md)

[Supply Chain Management の顧客への Sales の勘定の直接同期](accounts-template-mapping-direct.md)

[Supply Chain Management の連絡先または顧客への Sales の連絡先の直接同期](contacts-template-mapping-direct.md)

[販売注文の Sales と Supply Chain Management の間の直接同期](sales-order-template-mapping-direct-two-ways.md)

[売上請求書のヘッダーおよび明細行の Supply Chain Management から Sales への直接同期](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
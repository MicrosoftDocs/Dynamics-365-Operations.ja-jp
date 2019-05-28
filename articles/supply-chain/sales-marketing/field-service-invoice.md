---
title: Field Service の契約請求書を Finance and Operations の自由書式の請求書に同期します
description: このトピックでは、Microsoft Dynamics 365 for Field Service の契約請求書を Microsoft Dynamics 365 for Finance and Operations の自由書式の請求書に同期するために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560166"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>Field Service の契約の請求書と Finance and Operations の自由書式の請求書との同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Field Service の契約請求書を Microsoft Dynamics 365 for Finance and Operations の自由書式の請求書に同期するために使用されるテンプレートと基本的なタスクについて説明します。

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

次のテンプレートと基本的なタスクは、Field Service の契約請求書と Finance and Operations の自由書式の請求書との同期を実行するために使用されます。

**データ統合でのテンプレートの名前:**

- 契約請求書 (Field Service から Finance and Operations)

**データ統合プロジェクトのタスク名:**

- 請求書ヘッダー
- 請求明細行

契約請求書の同期が処理される前に、次の同期が必要です。

- 勘定 (Sales から Finance and Operations) – 直接

## <a name="entity-set"></a>エンティティ セット

| Field Service  | Finance and Operations                 |
|----------------|----------------------------------------|
| 請求書       | CDS 顧客の自由書式請求書ヘッダー |
| invoicedetails | CDS 顧客の自由書式請求書明細行   |

## <a name="entity-flow"></a>エンティティのフロー

Field Service の契約から作成された請求書は、Common Data Service (CDS) データの統合プロジェクトを通して Finance and Operations に同期することができます。 自由書式の請求書の会計ステータスが**処理中**の場合、これらの請求書の更新は Finance and Operations の自由書式の請求書に同期されます。 自由書式の請求書が Finance and Operations に転記済で、会計ステータスが**完了**に更新されると、Field Service から更新を同期することはできなくなります。

## <a name="field-service-crm-solution"></a>Field Service CRM ソリューション

**契約元の行を有する** フィールドが**請求書**エンティティに追加されました。 このフィールドは、契約書から作成された請求書のみが同期されることを保証するのに役立ちます。 契約書に基づく請求明細行が少なくとも 1 つ含まれている場合、値は **true** です。

**契約元を有する** フィールドが**請求明細行**エンティティに追加されました。 このフィールドは、契約書から作成された請求明細行のみが同期されることを保証するのに役立ちます。 請求明細行が契約書に基づいている場合、値は **true** です。

**請求日** は、Finance and Operations の必須フィールドです。 したがって、このフィールドは同期が発生する前に Field Service に値が必要です。 この要件を満たすためには、次のロジックが追加されます。

- **請求日** フィールドの**請求書**エンティティが空白の場合 (つまり、値が存在しない) 場合、契約に基づく請求明細行が追加された現在の日付が設定されます。
- ユーザーは **請求日** フィールドを変更できます。 ただし、ユーザーが契約に基づいた請求書を保存する際に、**請求日** フィールドの請求書が空白の場合、ユーザーは業務プロセス エラーを受け取ります。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定

### <a name="in-finance-and-operations"></a>Finance and Operations

Field Service の契約請求書から作成された Finance and Operations の自由書式の請求書を区別するために、統合に対して請求書発生元を設定する必要があります。 請求書が**契約請求書統合**タイプの請求書発生元を含んでいる場合、**外部請求書番号** フィールドが**売上請求書**ヘッダーに表示されます。

請求書ヘッダーでの表示に加えて、Field Service 契約請求書から作成された請求書が Finance and Operations から Field Service への販売注文同期の間に除外されることを保証するために**外部請求書番号**情報は使用されます。

1. **売掛金勘定** \> **設定** \> **請求書発生元コード** に移動します。
2. **新規**を選択し、新しい請求書発生元を作成します。
3. **販売元** フィールドに、**FS** のような請求書発生元の名前を入力します。
4. **説明** フィールドに、**Field Service契約請求書**のような説明を入力します。
5. **発生元タイプの割り当て** チェック ボックスを選択します。
6. **請求書発生元** フィールドを**契約請求書統合**に設定します。
7. **保存** を選択します。

### <a name="in-the-data-integration-project"></a>データ統合プロジェクト内

タスク: **請求明細行**  

Finance and Operations フィールド**主勘定表示値**に対する既定の値が、希望する値と一致するように更新されているか確認してください。

既定のテンプレートの値は **401100** です。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示しています。

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a>契約請求書 (Field Service から Finance and Operations): 請求書ヘッダー

[![データ統合のテンプレートのマッピング](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a>契約請求書 (Field Service から Finance and Operations): 請求明細行

[![データ統合のテンプレートのマッピング](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)

---
title: 見越計上の概要
description: この記事は、見越し計上について説明し、その設定方法およびトランザクションの作成方法に関する情報を提供します。
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b97055f7eac12e3e82d028a0097ca926e5c355a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445147"
---
# <a name="accruals-overview"></a>見越計上の概要

[!include [banner](../includes/banner.md)]

この記事は、見越し計上について説明し、その設定方法およびトランザクションの作成方法に関する情報を提供します。

発生主義会計では、見越計上は、支払を受け取ったときではなく獲得した期間に認識された収益を追跡するために、支払ったときではなく経費の発生時に認識された経費 (原価) を追跡するために、使用されます。

## <a name="accrual-schemes"></a>発生主義スキーマ
発生主義スキーマが繰延収益と原価を設定するために使用され、同じ発生主義スキーマが、収益と原価の両方に使用できます。 元帳計上では、原価または収益が適切な期間に認識されるように、仕訳帳明細行の原価または収益を再配分します。 **発生主義スキーマ** ページで、発生主義スキーマが適用される場合に使用する借方勘定と貸方勘定を指定します。

-   **借方** – 定義した主勘定は、仕訳帳伝票の明細行の借方主勘定と置き換えられます。 この勘定は、元帳計上トランザクションに基づく繰延の取消にも使用されます。
-   **貸方** – 定義した主勘定は、仕訳帳伝票の明細行の貸方主勘定と置き換えられます。 この勘定は、元帳計上トランザクションに基づく繰延の取消にも使用されます。

使用する勘定を決定した後、見越計上トランザクションの作成時に伝票番号の作成方法を指定できます。 また、トランザクションの発生頻度、トランザクションの作成回数、およびトランザクションの転記時期を指定できます。 発生主義スキーマの作成後、元帳計上機能を使用して、一部の仕訳帳で発生主義スキーマを使用できます。

## <a name="ledger-accruals"></a>元帳計上
仕訳帳を入力すると、**機能** メニューの **元帳計** をクリックできます。 その後、発生主義スキーマを選択すると、発生主義スキーマによって決定される、その期間にわたって分割される仕訳帳からの基準額が表示されます。 たとえば、1 月に 1 年間全体の従業員の保険料を 12,000 支払う場合、各月の保険料を確認する必要があります。 開始日は選択できます。 また、金額が勘定または相手勘定に基づくかどうかを指定できます。 選択後に、**トランザクション** をクリックして、発生主義スキーマに基づいて作成されたすべてのトランザクションを表示します。 たとえば、1 年間の保険料 12,000 を分割する場合、各月では 1,000 が表示されます。 仕訳帳を転記した後、**伝票トランザクション** 照会ページを使用して、トランザクションを表示できます。 発生主義スキーマが適用できない場合 (たとえば、販売注文請求書または発注請求書が含まれる場合)、前払金額を貸方転記し、経費金額を借方転記できます。 その後、発生主義スキーマの適用時に **相殺** を選択できます。


詳細については、[発生主義スキーマの作成](tasks/create-accrual-schemes.md) および [元帳発生トランザクションの作成](tasks/create-ledger-accrual-transactions.md)を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
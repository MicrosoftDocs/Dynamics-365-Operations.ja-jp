---
title: 運賃の手動調整
description: この手順では、運賃を手動で調整する方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec17fc31df1daed943f9bc3f4cbe25a683c8ac7e
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026317"
---
# <a name="reconcile-freight-manually"></a>運賃の手動調整

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、運賃を手動で調整する方法を示します。 この設定は、通常、配送コーディネーターにより実行されます。 デモ データの会社 USMF でこの手順を使用できます。


## <a name="select-a-load-to-reconcile"></a>積荷を選択して調整します。
1. [配送管理] > [計画] > [積荷計画ワークベンチ] の順に移動します。
2. [出荷と入庫を非表示にする] チェック ボックスをオフにします。 
3. リストで、積荷 ID 00006 を持つ積荷を選択します。

## <a name="create-a-carrier-invoice"></a>運送業者の請求書を作成する
運賃を手動で調整して、配送業者の請求書を自動的に受け取らない場合、運賃請求書に基づいて請求書を作成できます。  
1. [関連情報] をクリックします。
2. [運賃請求書の詳細] をクリックします。
3. [運賃請求書の請求書の生成] をクリックします。
4. [請求書] フィールドに値を入力します。
5. [OK] をクリックします。

## <a name="reconcile-the-invoice"></a>請求書を調整する
配送業者の請求書と運賃請求書を調整する場合、1 行ずつ処理します。  
1. [運賃請求書と請求書の照合] をクリックします。
2. [請求書の詳細] セクションを展開します。
3. [一致しない運賃請求書の詳細] セクションを展開します。
4. 一覧で、選択された行をマークします。
5. [照合] をクリックします。
6. 一致した配送料請求書の詳細セクションを展開します。

## <a name="submit-the-invoice-for-approval"></a>承認のために請求書を送信します
1. 承認のために [送信] をクリックします。
2. ページを閉じます。
3. 承認済みチェック ボックスの非表示を消去します。 
4. 仕入先の請求仕訳をクリックします。
5. クリックして [参照仕訳帳番号] フィールドのリンクに従います。
6. [明細行] をクリックします。


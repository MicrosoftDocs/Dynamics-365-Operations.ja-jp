---
title: つなぎ支払の設定および処理
description: この記事では、つなぎの顧客支払の設定および処理方法について説明します。 つなぎ支払は、2 つの手順で総勘定元帳に転記される支払です。
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb563008f156e1bfa6e4e9a705e9170342719ce7
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775171"
---
# <a name="set-up-and-process-bridged-payments"></a>つなぎ支払の設定および処理

[!include [banner](../includes/banner.md)]

つなぎ支払は、2 つの手順で総勘定元帳に転記される支払です。 通常、この方法は、支払方法が **銀行** に設定されている場合に使用され、トランザクションが銀行をクリアした場合にのみトランザクションを銀行口座に転記する必要があります。 ただし、勘定科目に対して使用することもできます。 この場合、つなぎ転記の処理時に、ある主勘定から別の主勘定に金額が移されます。

つなぎ支払は、買掛金勘定または売掛金勘定から作成できます。 この記事では、売掛金勘定に対するつなぎ転記の構成方法について説明しますが、買掛金勘定トランザクションの手順も同様です。

## <a name="set-up-bridging-posting"></a>つなぎ転記を設定

つなぎ転記を使用するには、**つなぎ転記** 方法を使用するように、1 つ以上の支払方法を設定する必要があります。 次につなぎ勘定を選択する必要があります。

1. **売掛金勘定 &gt; 支払の設定 &gt; 支払方法** の順に移動します。
2. つなぎ転記を有効にする既存の支払方法を選択します。 または、新しい支払方法を作成します。
3. **つなぎ転記** チェック ボックスを選択します。
4. **つなぎ勘定** フィールドで、支払が銀行口座に清算される前に転記する主勘定を選択します。
5. ページを閉じます。

## <a name="process-and-transfer-bridging-posting"></a>つなぎ転記の処理および転送

つなぎ転記を作成および処理するには、次の手順に従います。

1. **売掛金勘定 &gt; 支払 &gt; 支払仕訳帳** に移動します。
2. **新規** を選択して仕訳を作成します。
3. **名前** フィールドで名前を選択します。
4. 顧客支払仕訳帳に明細行を追加し、つなぎ転記用に構成された支払方法を選択します。
5. 仕訳帳を転記します。 トランザクションは、前述の手順の **つなぎ勘定** フィールドで選択した主勘定に転記されます。

トランザクションが銀行で決済され、つなぎ勘定から支払方法に指定されている支払勘定に支払を転送するには、次の手順に従います。

1. **一般会計 &gt; 仕訳入力 &gt; 一般仕訳帳** の順に移動します。
2. **新規** を選択して仕訳を作成します。
3. **名前** フィールドで名前を選択します。
4. **明細行** を選択して、仕訳帳の詳細を開きます。
5. **関数 &gt; つなぎ勘定トランザクションの選択** を選択します。
6. 決済された各支払にマークを付け、**承認** を選択します。
7. 仕訳帳を転記します。

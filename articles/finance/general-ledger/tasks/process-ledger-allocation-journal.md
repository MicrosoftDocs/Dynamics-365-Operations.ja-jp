---
title: 元帳配賦仕訳帳の処理
description: この記事では、Dynamics 365 Finance での配賦要求の処理方法について説明します。
author: aprilolson
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f22b5042e0e3726afcb1061852fdbd8de770c61
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779395"
---
# <a name="process-ledger-allocation-journal"></a>元帳配賦仕訳帳の処理

[!include [banner](../../includes/banner.md)]

この記事では、配賦要求の処理方法について説明します。 **配賦要求の処理** ページを使用して、[総勘定元帳] に転記する前に確認および承認したり、[総勘定元帳] に直接転記することが可能な配賦仕訳帳を作成します。 配賦仕訳帳を作成するためには、少なくとも 1 つの有効な [元帳配賦ルール] が必要です。 このタスクでは、USMF というデモ会社を使用します。

1. ナビゲーション ウィンドウで、**一般会計 > 配賦 > 配賦要求の処理** の順に移動します。
2. **ルール** フィールドで、ドロップダウン メニューから目的のレコードを選択します。
3. **現在の日付** フィールドに日付を入力します。

    - 元帳がルールのデータ ソースである場合、**現在の日付** はとても重要です。 この日付けによって、どの元帳残高を配賦に含めるかを制御します。  
    - **ゼロ ソース** フィールドで **停止** を選択します。 この操作により配賦プロセスを停止し、配賦元の金額ゼロが選択されたことを示すメッセージを表示します。  

4. **提案オプション** フィールドで、**提案のみ** を選択します。 **提案のみ** を選択し、総勘定元帳に配賦を転記する前に、**配賦仕訳帳** の結果を確認し、また必要に応じて承認します。  
5. **GL 転記日付** フィールドに日付を入力します。
6. **OK** を選択します。
7. ナビゲーション ウィンドウで、**モジュール > 一般会計 > 配賦 > 配賦仕訳帳** の順に移動します。
8. **明細行** を選択します。
9. **投稿** を選択します。
10. **投稿** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

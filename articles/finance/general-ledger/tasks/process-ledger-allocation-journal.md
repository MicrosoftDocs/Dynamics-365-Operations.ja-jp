---
title: 元帳配賦仕訳帳の処理
description: このトピックでは、Dynamics 365 Finance での配賦要求の処理方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 33e989d3641ae1eaa28a55398fcf51674ac1ed72
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445212"
---
# <a name="process-ledger-allocation-journal"></a>元帳配賦仕訳帳の処理

[!include [banner](../../includes/banner.md)]

このトピックでは、配賦要求の処理方法について説明します。 [配賦要求の処理] ページを使用して、[総勘定元帳] に転記する前に確認および承認したり、[総勘定元帳] に直接転記することが可能な配賦仕訳帳を作成します。 配賦仕訳帳を作成するためには、少なくとも 1 つの有効な [元帳配賦ルール] が必要です。 このタスクでは、USMF というデモ会社を使用します。

1. ナビゲーション ウィンドウで、**モジュール > 一般会計 > 配賦 > 配賦要求の処理** の順に移動します。
2. **ルール** フィールドで、ドロップダウン メニューから目的のレコードを選択します。
3. **現在の日付** フィールドに日付を入力します。

    - 元帳がルールのデータ ソースである場合、**現在の日付** はとても重要です。 この日付けによって、どの元帳残高を配賦に含めるかを制御します。  
    - **ゼロ ソース** フィールドで **停止** を選択します。 この操作により配賦プロセスを停止し、配賦元の金額ゼロが選択されたことを示すメッセージを表示します。  

4. **提案オプション** フィールドで、**提案のみ** を選択します。 **提案のみ** を選択し、総勘定元帳に配賦を転記する前に、配賦仕訳帳の結果を確認し、また必要に応じて承認します。  
5. [GL 転記日付] フィールドに日付を入力します。
6. **OK** を選択します。
7. ナビゲーション ウィンドウで、**モジュール > 一般会計 > 配賦 > 配賦仕訳帳** の順に移動します。
8. **明細行** を選択します。
9. **投稿** を選択します。
10. **投稿** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
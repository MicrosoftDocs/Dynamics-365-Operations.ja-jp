---
title: 償却提案の作成
description: このトピックでは、減価償却のバッチの提案の働きと、固定資産に対して減価償却を提案する方法について説明します。
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3d62e982d26afbec7ac04dd80592a73f4a3286f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968906"
---
# <a name="create-a-depreciation-proposal"></a>償却提案の作成

[!include [banner](../../includes/banner.md)]

このトピックでは、減価償却のバッチの提案の働きと、固定資産に対して減価償却を提案する方法について説明します。 このタスクでは USMF のデモ会社および経理担当者のロールを使用します。


## <a name="create-a-depreciation-proposal"></a>償却提案の作成
1. ナビゲーション ウィンドウで、**モジュール > 固定資産 > 仕訳入力 > 償却提案の作成** の順に移動します。
2. **仕訳帳名** フィールドで、ドロップダウン メニューからオプションを選択します。
3. **終了日** フィールドに、日付を入力します。

    - 月間の減価償却を 1 つの仕訳帳明細行に集計する場合に、**減価償却の集計** オプションを選択します。  
    - たとえば、終了日の値が 2015 年 3 月 31 日の場合、以下の説明が生成されます: "2015 年 1 月 31 日以降の減価償却。" 提案された仕訳帳明細行の **日付** フィールドは、2015 年 3 月 31 日に設定されます。  
    - 償却提案は資産、資産グループ、または他の検索条件別に、**フィルター** オプションを使用してフィルター処理できます。  
    - **固定資産に対する取得提案または償却提案の作成** フォームを使用すると、減価償却をバッチで提案できます。 これは、より多くのシステム リソースを使用する大規模な提案に対して推奨されています。 バッチのオプションを選択した場合、その処理中に他のタスクも実行できます。 この方法で減価償却を提案する場合、減価償却は固定資産の価値モデルに対して計算されます。  

4. **仕訳帳の作成** を選択します。

## <a name="review-depreciation-entries"></a>減価償却のエントリを確認します
1. ナビゲーション ウィンドウで、**モジュール > 固定資産 > 仕訳入力 > 固定資産仕訳帳** に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. **明細行** を選択します。
4. **投稿** を選択します。


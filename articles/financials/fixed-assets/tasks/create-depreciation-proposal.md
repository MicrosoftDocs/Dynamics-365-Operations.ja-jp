--- 
title: "償却提案の作成"
description: "この手順では、減価償却のバッチ提案がどうのように機能するか、および固定資産の減価償却を提案する方法について説明します。"
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 07d8cf2f1c46b99dfcd1d7c3419fe835f37c5a02
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-depreciation-proposal"></a>償却提案の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、減価償却のバッチ提案がどうのように機能するか、および固定資産の減価償却を提案する方法について説明します。 このタスクでは USMF のデモ会社および経理担当者のロールを使用します。


## <a name="create-depreciation-proposal"></a>償却提案を作成します
1. [固定資産] > [仕訳入力] > [償却提案の作成] の順に移動します。
2. [仕訳帳名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、選択された行のリンクをクリックします。
4. [終了日] フィールドで、日付を入力します。
    * 月間の減価償却を 1 つの仕訳帳明細行に集計する場合に、減価償却の集計オプションを選択します。  
    * たとえば、終了日の値が 2015 年 3 月 31 日の場合、次の説明: “2015 年 1 月 31 日以降の原価償却” が作成されます。 提案された仕訳帳明細行の [日付] フィールドは、2015 年 3 月 31 日に設定されます。  
    * 償却提案は資産、資産グループ、または他の検索条件別に、フィルター オプションを使用してフィルター処理できます。  
    * 固定資産のフォームの取得提案または償却提案を作成すると、減価償却をバッチで提案できます。 これは、より多くのシステム リソースを使用する大規模な提案に対して推奨されています。 バッチのオプションを選択した場合、その処理中に他のタスクも実行できます。 この方法で減価償却を提案する場合、減価償却は固定資産の価値モデルに対して計算されます。  
5. [仕訳帳の作成] をクリックします。

## <a name="review-depreciation-entries"></a>減価償却のエントリを確認します
1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. [明細行] をクリックします。
4. [転記] をクリックします。



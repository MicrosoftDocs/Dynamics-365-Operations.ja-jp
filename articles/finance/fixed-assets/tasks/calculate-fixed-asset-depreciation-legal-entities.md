---
title: 法人間での固定資産減価償却の計算
description: 固定資産減価償却は、単一のステップで複数の法人に対して実行することができます。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b09bbe4d0143aa521ca0a4cf67e86b7165b0f4f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968957"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>法人間での固定資産減価償却の計算

[!include [banner](../../includes/banner.md)]

固定資産減価償却は、単一のステップで複数の法人に対して実行することができます。 この手順では、複数の法人組織に対してプロセスを設定して実行する方法を示します。 これは USMF の法人に対して経理担当ロールとデモ データを使用します。


## <a name="set-up-cross-company-depreciation-run-journals"></a>会社間の減価償却実行ジャーナルを設定します
1. [固定資産] > [設定] > [固定資産パラメーター] の順に移動します。
2. 固定資産提案セクションを展開します。
3. [追加] をクリックします。
4. [転記階層] フィールドで値を入力または選択します。
5. [仕訳帳名] フィールドで値を入力または選択します。
    * 各法人の固定資産のパラメータのページで仕訳帳の設定を繰り返します。  

## <a name="depreciation-run"></a>減価償却
1. [固定資産] > [仕訳入力] > [償却提案の作成] の順に移動します。
2. [転記階層] フィールドで値を入力または選択します。
    * 仕訳帳名は固定資産のパラメータが既定で使用されます。 現在の法人をここで変更できます。  
3. [終了日] フィールドで、日付を入力します。
    * 減価償却の対象として法人を選択します。  
    * 固定資産パラメータページで固定資産提案に対して設定された仕訳を持つ法人のみがリストに表示されます。  
4. [仕訳帳の転記] フィールドで、[はい] を選択します。
    * フィルター フィールドには、この減価償却実行に対して選択された法人のすべての固定資産、グループ、および帳簿が含まれます。  
    * バッチ処理オプションが既定で有効になっています。 このオプションを有効にすると、減価償却の仕訳帳の作成と転記がバック グラウンドで実行されます。  
5. [仕訳帳の作成] をクリックします。
6. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。


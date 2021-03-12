---
title: 特別償却の設定
description: この手順では、特別減価償却費を作成する方法およびそれを固定資産帳簿に関連付ける方法を説明します。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fed9f09b4e37da00a5d78fa088e8814db48456b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968932"
---
# <a name="set-up-bonus-depreciation"></a>特別償却の設定

[!include [banner](../../includes/banner.md)]

この手順では、特別減価償却費を作成する方法およびそれを固定資産帳簿に関連付ける方法を説明します。 これは USMF の法人に対して経理担当ロールとデモ データを使用します。


## <a name="create-a-special-depreciation-allowance"></a>特別減価償却費の作成
1. [固定資産] > [設定] > [特別減価償却費] の順に移動します。
2. [新規] をクリックします。
3. [特別減価償却費] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [割合] フィールドに数値を入力します。
    * 割合が表示されなかった場合は金額を設定します。  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a>特別減価償却費を固定資産グループ帳簿と関連付ける
1. [固定資産] > [設定] > [固定資産グループ] の順に移動します。
2. 一覧で、特別減価償却費に関連する固定資産グループを選択します。
3. [帳簿] をクリックします。
4. 一覧で、特別減価償却費に関連する帳簿を選択します。
5. [特別減価償却費] をクリックします。
6. [新規] をクリックします。
7. [特別減価償却費] フィールドで、値を入力または選択します。
    * 割合または金額の既定値は特別減価償却費の設定によって決まります。  
8. [優先順位] フィールドに数値を入力します。


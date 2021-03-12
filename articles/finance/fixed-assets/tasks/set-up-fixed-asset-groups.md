---
title: 固定資産グループの設定
description: このトピックでは、新しい固定資産グループを作成する方法を説明します。
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4eead36e1274194b151b230767a4d6385173b12f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994843"
---
# <a name="set-up-fixed-asset-groups"></a>固定資産グループの設定

[!include [banner](../../includes/banner.md)]

このトピックでは、新しい固定資産グループを作成する方法を説明します。 これは USMF の法人に対して経理担当ロールとデモ データを使用します。

1. ナビゲーション ウィンドウで、**モジュール > 固定資産 > 設定 > 固定資産グループ** に移動します。
2. **新規** を選択します。
3. **固定資産グループ** フィールドに、値を入力します。
4. **名前** フィールドに値を入力します。 **固定資産** グループにおける固定資産の自動採番と番号順序コードは、固定資産のパラメータの設定より優先されます。 この固定資産グループの資産に他のグループからの異なる番号付けがある場合、ここでこれを変更できます。  
5. **帳簿** を選択します。
6. **帳簿** フィールドで値を入力または選択します。 **減価償却の計算** フィールドが **はい** に設定されている場合、資産帳簿は償却提案に含まれます。 **減価償却の計算** が **いいえ** に設定されている場合、資産は自動的に償却されません。  
7. 資産の耐用年数を設定します。 耐用年数を設定した後に、**減価償却期間** のフィールド値が計算されることに注意してください。  
8. **減価償却方法** フィールドで、オプションを選択します。
9. ページを閉じます。


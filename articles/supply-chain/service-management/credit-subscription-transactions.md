---
title: "定期売買トランザクションの貸方記入"
description: "このトピックでは、定期売買手数料トランザクションの貸方への記入方法について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: cd6c91126604fc704ac0283d5db062077275e725
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="credit-subscription-transactions"></a>定期売買トランザクションの貸方記入 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a>定期売買トランザクションの貸方記入

1.  **サービス管理** \> **共通** \> **サービスの定期売買** \> **すべてのサービス定期売買**の順にクリックします。

2.  貸方票を作成する定期売買トランザクションに関連付けられている定期売買を選択します。

3.  **分析**タブを選択し、アクション ウィンドウで**手数料トランザクション**ボタンをクリックします。

4.  **手数料トランザクション**フォームから、訂正票を作成するトランザクションを選択します。

5.  **機能** \> **貸方票の選択**の順にクリックします。

6.  **貸方票の選択**フォームで、貸方転記するトランザクションを選択し、**OK**をクリックします。


> [!NOTE]
> <P>貸方票を作成する場合は、必ず<STRONG>貸方票</STRONG>を選択してください。 これは、<STRONG>請求書の作成</STRONG>ダイアログ ボックスの<STRONG>請求方法</STRONG>リストにあります。</P>

**サービス管理パラメーター**フォームの**見越計上を貸方にリバース仕訳**フィールドが**手動**に設定されている場合は、トランザクションの貸方票提案を作成する前に、各未収収益トランザクションを個別に取り消す必要があります。

## <a name="see-also"></a>参照

[定期売買トランザクションの請求](invoice-subscription-transactions.md)


 


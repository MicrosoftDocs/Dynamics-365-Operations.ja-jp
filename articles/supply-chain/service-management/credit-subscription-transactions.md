---
title: サブスクリプション トランザクションの貸方記入
description: この記事では、サブスクリプション手数料トランザクションの貸方への記入方法について説明します。
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 482a276a86d4b4174d276d775513069d423c17a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015902"
---
# <a name="credit-subscription-transactions"></a>サブスクリプション トランザクションの貸方記入 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a>サブスクリプション トランザクションの貸方記入

1.  **サービス管理** \> **サービス サブスクリプション** \> **すべてのサービス サブスクリプション** をクリックします。

2.  貸方票を作成するサブスクリプション トランザクションに関連付けられているサブスクリプションを選択します。

3.  **分析** タブを選択し、アクション ウィンドウで **手数料トランザクション** ボタンをクリックします。

4.  **手数料トランザクション** フォームから、訂正票を作成するトランザクションを選択します。

5.  **機能** \> **貸方票の選択** の順にクリックします。

6.  **貸方票の選択** フォームで、貸方転記するトランザクションを選択し、**OK** をクリックします。


> [!NOTE]
> <P>貸方票を作成する場合は、必ず<STRONG>貸方票</STRONG>を選択してください。 これは、<STRONG>請求書の作成</STRONG>ダイアログ ボックスの<STRONG>請求方法</STRONG>リストにあります。</P>

**サービス管理パラメーター** フォームの **見越計上を貸方にリバース仕訳** フィールドが **手動** に設定されている場合は、トランザクションの貸方票提案を作成する前に、各未収収益トランザクションを個別に取り消す必要があります。

## <a name="see-also"></a>参照

[サブスクリプション トランザクションの請求](invoice-subscription-transactions.md)


 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
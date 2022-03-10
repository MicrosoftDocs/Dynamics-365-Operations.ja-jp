---
title: サブスクリプション トランザクションの貸方記入
description: このトピックでは、サブスクリプション手数料トランザクションの貸方への記入方法について説明します。
author: kamaybac
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ca690bc97aff2112c9464d8a6f7cee8fbc0879c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571452"
---
# <a name="credit-subscription-transactions"></a>サブスクリプション トランザクションの貸方記入 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a>サブスクリプション トランザクションの貸方記入

1.  **サービス管理** \> **共通** \> **サービス サブスクリプション** \> **すべてのサービス サブスクリプション** の順にクリックします。

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
---
title: 返品による請求書更新の実行
description: この機能は、返品注文と販売注文を同じ担当者が同時に請求する、組織で採用されている業務プロセスをサポートしています。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3890ea31ee899f021405fb5475b20f9dd63c1e2e103b63af8b53bccc53d0781f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730157"
---
# <a name="perform-invoice-updates-for-returns"></a>返品による請求書更新の実行 

[!include [banner](../includes/banner.md)]


返品注文は、返品された注文としてマークされた販売注文の一タイプです。 したがって 、**返品注文** フォームの代わりに返品注文の請求書を生成するには、**すべての販売注文** リスト ページを使用します。 この機能は、返品注文と販売注文を同じ担当者が同時に請求する、組織で採用されている業務プロセスをサポートしています。

返品品目の請求書は負の量であるため、訂正票と呼ばれます。

請求書の更新をバッチ処理として設定する場合、タイプが **返品注文** の販売注文の返品明細行ステータスを、注文の梱包明細が更新済であることを示す **受入済** にする必要があります。

## <a name="post-an-invoice-for-a-return-order"></a>返品注文の請求書を転記する

1.  **売掛金管理** \> **共通** \> **販売注文** \> **すべての販売注文** の順にクリックします。

2.  **返品注文** が **注文タイプ** フィールドに表示される販売注文を選択します。

3.  アクション ウィンドウの、**請求書** タブで、**生成** グループから **請求書** をクリックします。

4.  **パラメーター** タブで **転記** チェック ボックスをオンにします。

5.  フォームの情報を確認し、必要な変更を行います。

6.  **OK** をクリックします。 訂正票が転記されます。

## <a name="see-also"></a>参照

[返品による梱包明細票の更新](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
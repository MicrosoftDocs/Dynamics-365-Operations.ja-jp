---
title: "日本の固定資産配賦ルール"
description: "この記事は、日本の固定資産配賦ルールについてよく寄せられる質問に回答します。"
author: yijialuan
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetAllocationRuleSetup_CN
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10194
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 554c350961baed8be8f37854dd1b095d4342ae0e
ms.openlocfilehash: f0a78d0407ad52c5f42fad18d0b369f5b6829ae1
ms.contentlocale: ja-jp
ms.lasthandoff: 03/21/2018

---

# <a name="fixed-asset-allocation-rules-for-japan"></a>日本の固定資産配賦ルール

[!INCLUDE [banner](../includes/banner.md)]

日本では、固定資産は管理部門に登録され、減価償却量は使用部門間で割り当てられる必要があります。 減価償却金額を割合で複数の財務分析コードに割り当てる配賦ルールを設定できます。 この記事は、固定資産配賦ルールについてよく寄せられる質問に回答します。

自分の法人の分析コードに固定資産の減価償却費を配賦する配賦ルールを設定できます。 固定資産は、部門、コスト センターなどの、複数の分析コードのサービスに投入できます。 固定資産の減価償却時に、減価償却費は相手勘定に転記されます。 配賦ルールの設定によって、固定資産の減価償却費を法人の複数の分析コード間で分配できます。

## <a name="when-depreciation-costs-are-allocated-can-the-dimensions-that-are-based-on-the-allocation-rule-of-the-fixed-asset-model-override-the-default-dimensions-in-the-journal-header"></a>減価償却費を配賦するとき、固定資産モデルの配賦ルールに基づく分析コードが仕訳帳ヘッダーの既定の分析コードを上書きできますか
はい。 配賦ルールに指定する分析コードは、仕訳帳ヘッダーに通常表示される既定の分析コードを上書きします。

## <a name="what-happens-if-i-delete-a-dimension-that-is-part-of-an-allocation-rule"></a>配賦ルールの一部の分析コードを削除すると何が起こります。
配賦ルールに割り当てられている財務分析コードを削除すると、償却提案を実行することができないことを示すメッセージを表示します。 配賦ルールの別の財務分析コードを選択し、償却提案を再度実行する必要があります。

## <a name="how-does-rounding-the-currency-up-or-down-affect-the-allocation-rule"></a>通貨の端数の切り上げまたは切り下げはどのように配賦ルールに影響しますか
配賦ルールを固定資産に適用すると、法人の分析コードに配賦される減価償却費は合計額か、または分割した額になります。 通貨の丸めルールを適用した場合、配賦ルールに従って、結果として配賦される減価償却費は減価償却費よりも大きくなるか小さくなる場合があります。 通貨の丸め方が配賦ルールに影響を及ぼす例を以下に示します。

### <a name="rounded-up-currency"></a>通貨の切り上げ

この例では、固定資産の減価償却費の金額が 170 通貨単位です。 自分の法人の 100 種類の分析コードごとに減価償却費の 1% を割り当てる配賦ルールを設定します。 2 つの通貨単位間の中間値よりも大きい小数の通貨単位は、もっとも近い通貨単位に切り上げることを指示する丸めルールを設定します。 このシナリオでの分析コードごとの減価償却費の計算方法をここに示します。

-   分析コードごとの元の減価償却費 = 1.70 通貨単位
-   切り上げた分析コードごとの減価償却費 = 2.00 通貨単位
-   固定資産の合計の切り上げた減価償却費 = 2.00 × 100 = 200 通貨単位

### <a name="rounded-down-currency"></a>切り下げた通貨

この例では、固定資産の減価償却費の金額が 120 通貨単位です。 自分の法人の 100 種類の分析コードごとに減価償却費の 1% を割り当てる配賦ルールを設定します。 2 つの通貨単位間の中間値よりも小さい小数の通貨単位は、もっとも近い通貨単位に切り下げることを指示する丸めルールを設定します。 このシナリオでの分析コードごとの減価償却費の計算方法をここに示します。

-   分析コードごとの元の減価償却費 = 1.20 通貨単位
-   切り下げた分析コードごとの減価償却費 = 1.00 通貨単位
-   固定資産の合計の切り下げた減価償却費 = 1.00 × 100 = 100 通貨単位

各分析コードに割り当てる合計の切り下げた減価償却費が丸める額よりも小さい場合、この配賦ルールは減価償却に適用しません。 代わりに、減価償却額は主勘定に転記されるか、**固定資産転記プロファイル**  ページで設定する転記プロファイルを使用して相殺されます。 これらおよび同様のシナリオを回避するために、固定資産減価償却の丸めルールを**通貨**ページで手動で調整できます。

## <a name="additional-resources"></a>その他のリソース
- [資産グループへの共有資産とのれんの帳簿価額の配賦](./tasks/allocate-carrying-amount.md)


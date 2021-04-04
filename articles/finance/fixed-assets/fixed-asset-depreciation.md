---
title: 固定資産の減価償却
description: このトピックは、固定資産の償却の概要を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87317eedad06e93625212df3cc6e017b9475c932
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240997"
---
# <a name="fixed-asset-depreciation"></a>固定資産の減価償却

[!include [banner](../includes/banner.md)]

このトピックは、固定資産の償却の概要を示します。

減価償却は、一般に、貸借対照表の固定資産の価値を減少させる定期処理取引であり、損益勘定では支出として記帳します。 したがって、通常、主勘定を使用して貸借対照表の定期減価償却を貸方に転記します。 相手勘定は、勘定科目の損益部分の勘定です。

## <a name="depreciation-adjustment"></a>減価償却調整
通常は、転記済みの減価償却取引に対する修正のみが減価償却調整として転記されます。 したがって、主勘定と相手勘定は、減価償却の勘定と同様に設定します。 減価償却調整額は、正にも負にもなりますが、主勘定 (貸借対照表の勘定として) と相手勘定 (通常、損益勘定として) の機能は変わりません。

## <a name="extraordinary-depreciation"></a>特別減価償却
特別減価償却は基本的な減価償却として処理されます。 したがって、主勘定は減価償却金額を貸借対照表の貸方に転記するために使用され、固定資産の価値を減少させます。 相手勘定は、会計年度期間に対して計算された減価償却が経費として請求される損益勘定です。 

特別減価償却は、基本減価償却とは関係なく処理されます。 特別減価償却を異なる取引タイプにすると、通常の基本減価償却とは別に特別減価償却の転記と報告ができます。

## <a name="special-depreciation-allowance"></a>特別減価償却費
特別割引減価償却を使用すると、資産を供用し、減価償却を開始した初年度に、追加の減価償却金額を設定できます。 特別減価償却費は、他の減価償却計算の前に処理される必要があります。 特別減価償却費は固定資産の耐用年数までは不明なことが多いので、総勘定元帳に転記しない帳簿では、このタイプの減価償却を使用することをお勧めします。 総勘定元帳の周期機能に転記されないトランザクションの [削除] を使用して、これらの帳簿のトランザクション履歴を削除できます。 次に固定資産に関する減価償却履歴を削除し、削除の確認後、特別減価償却費を転記できます。それからその会計年度の残りの減価償却トランザクションを転記できます。 

特別減価償却費レコードは無数に作成できます。 固定資産グループ帳簿にこのレコードを割り当てた後、これらは固定資産帳簿に適用されます。 

特別減価償却費はパーセンテージまたは固定金額として入力されます。 減価償却提案を転記すると、特別減価償却費トランザクションが、減価償却トランザクションとは異なるトランザクションとして、帳簿に転記されます。

## <a name="depreciation-calendars"></a>償却年 : カレンダー
各帳簿には、固定資産の減価償却時に使用されるカレンダーがあります。 帳簿上でカレンダーを指定していない場合、帳簿では既定で元帳の会計カレンダーが使用されます。 帳簿に関連付けられた減価償却プロファイルによって減価償却会計年度が使用される場合、帳簿の会計カレンダーを選択する必要があります。 

総勘定元帳の **会計カレンダー** ページを使用して、共用カレンダーを作成できます。

詳細については、[減価償却方法](depreciation-methods-conventions.md) を参照してください。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
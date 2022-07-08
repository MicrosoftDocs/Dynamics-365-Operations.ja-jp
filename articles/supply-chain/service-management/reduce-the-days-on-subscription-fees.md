---
title: サブスクリプション手数料の日数の引き下げ
description: 既存のサブスクリプション手数料の日数の下方修正は、サブスクリプション手数料期間にもはや含まれない期間を除外した、新しいトランザクションを作成して行えます。
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
ms.openlocfilehash: 370722d5c2f66e316d7c37f711cdd086bc53f6a8
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014825"
---
# <a name="reduce-the-days-on-subscription-fees"></a>サブスクリプション手数料の日数の引き下げ 

[!include [banner](../includes/banner.md)]


既存のサブスクリプション手数料の日数の下方修正は、サブスクリプション手数料期間にもはや含まれない期間を除外した、新しいトランザクションを作成して行えます。

## <a name="reduce-the-days-on-a-subscription-fee"></a>サブスクリプション手数料の日数の下方修正

1.  **サービス管理** \> **サービス サブスクリプション** \> **すべてのサービス サブスクリプション** をクリックします。 サービス サブスクリプションを選択し、アクション ウィンドウで、**サブスクリプション手数料** をクリックします

2.  **サブスクリプション タイプ** フィールドで、**下方修正日数** を選択します。

3.  **開始日** フィールドおよび **終了日** フィールドを使用して、サブスクリプション手数料期間から除外するサブスクリプション手数料の日付範囲を定義し、 **OK** をクリックします。

作成したトランザクションを表示するには、**サブスクリプション** フォームで、**手数料トランザクション** をクリックします。

## <a name="example"></a>例

1 月 1 日から 1 月 31 日までのサブスクリプション トランザクションの期間を 10 日間だけ下方修正する場合は、1 月 1 日から 1 月 10 日までを下方修正期間とする新しいトランザクションを作成します。 (下方修正期間は、1 月 5 日から 1 月 15 日までなど、別の 10 日を指定することもできます)。

また、下方修正期間の **開始日** が 1 月 21 日 (31 - 10) である場合は、**終了日** を 1 月 31 日以降の任意の日付に設定できます。この場合も、手数料トランザクション期間が 10 日間下方修正されます。

## <a name="see-also"></a>参照

[下方修正日数の例](reduction-days-example.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
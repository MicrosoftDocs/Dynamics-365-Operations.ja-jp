---
title: 定期売買手数料の日数の引き下げ
description: 既存の定期売買手数料の日数の下方修正は、定期売買手数料期間にもはや含まれない期間を除外した、新しいトランザクションを作成して行えます。
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
ms.openlocfilehash: df1a27576b93c4ace4a5f17271595d259e96a51a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573228"
---
# <a name="reduce-the-days-on-subscription-fees"></a>定期売買手数料の日数の引き下げ 

[!include [banner](../includes/banner.md)]


既存の定期売買手数料の日数の下方修正は、定期売買手数料期間にもはや含まれない期間を除外した、新しいトランザクションを作成して行えます。

## <a name="reduce-the-days-on-a-subscription-fee"></a>定期売買手数料の日数の下方修正

1.  **サービス管理** \> **共通** \> **サービスの定期売買** \> **すべてのサービス定期売買** の順にクリックします。 サービスの定期売買を選択し、アクション ウィンドウで、**定期売買手数料** をクリックします

2.  **定期売買タイプ** フィールドで、**下方修正日数** を選択します。

3.  **開始日** フィールドおよび **終了日** フィールドを使用して、定期売買手数料期間から除外する定期売買手数料の日付範囲を定義し、 **OK** をクリックします。

作成したトランザクションを表示するには、**定期売買** フォームで、**手数料トランザクション** をクリックします。

## <a name="example"></a>例

1 月 1 日から 1 月 31 日までの定期売買トランザクションの期間を 10 日間だけ下方修正する場合は、1 月 1 日から 1 月 10 日までを下方修正期間とする新しいトランザクションを作成します。 (下方修正期間は、1 月 5 日から 1 月 15 日までなど、別の 10 日を指定することもできます)。

また、下方修正期間の **開始日** が 1 月 21 日 (31 - 10) である場合は、**終了日** を 1 月 31 日以降の任意の日付に設定できます。この場合も、手数料トランザクション期間が 10 日間下方修正されます。

## <a name="see-also"></a>参照

[下方修正日数の例](reduction-days-example.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
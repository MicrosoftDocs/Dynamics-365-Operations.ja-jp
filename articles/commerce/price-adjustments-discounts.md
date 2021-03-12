---
title: 価格調整および割引
description: この記事は、Dynamics 365 Commerce における価格調整および割引についての情報を提供します。
author: scott-tucker
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f29e90e1c61792c70d4d6eaeee7758676bf193b2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972488"
---
# <a name="price-adjustments-and-discounts"></a>価格調整および割引

[!include [banner](includes/banner.md)]

この記事は、Dynamics 365 Commerce における価格調整および割引についての情報を提供します。

コマースでは、製品の価格を調整したり、POS、コール センターの販売注文、またはオンライン注文で明細行品目またはトランザクションに適用される割引を設定したりできます。 価格調整と割引のどちらも、価格グループとリンクすることができます。 価格調整と割引の両方について、単一の開始日と終了日を指定するか、または期間コード、割引コード、その他の追加の属性を指定することができます。 

価格調整と割引は、製品、バリアント、またはカテゴリーに適用できます。 複数の割引が製品に適用される場合、割引コンフィギュレーションの設定によって、顧客はいずれか 1 つの割引、または複合された割引を受け取ります。 コマースでは、割引または複合割引を、顧客に最適な価格となるように自動的に適用します。 価格調整または割引を設定する場合、価格グループが、割引が適用される正しいチャンネル、カタログ、所属、またはロイヤルティ プログラムに割り当てられていることを確認します。 また、割引 ID を自動的に生成するには、新しい割引または価格調整を定義する前に、**コマース パラメーター** ページで番号順序を設定します。

> [!NOTE]
> 価格調整または割引を削除できます。 ただし、統計情報は失われます。

## <a name="types-of-discounts"></a>割引タイプ

割引には多くのタイプがあります。

- **単純割引** – 単一のパーセントまたは量。
- **数量割引** – 複数の製品を購入するときに適用される割引。
- **組み合わせ割引** – 顧客が特定の製品の組み合わせを購入した場合に提供される割引。
- **しきい値割引** – トランザクションの合計が指定金額より大きいときに適用される割引。
- **支払/入金ベースの割引** – トランザクションの合計が指定した金額を超えて、特定の支払タイプ (現金、貸方、またはデビット カードなど) が支払に使用された場合に適用される割引。
- **送料割引** – トランザクションの合計が指定した金額を超えて、特定の荷渡方法 (出荷または一括出荷) が注文で使用される場合に適用される割引。

価格調整と割引のどちらも、価格グループと関連付けることができます。 価格グループは、チャンネル、カタログ、加盟者およびロイヤルティ プログラムに関連付けることができます。

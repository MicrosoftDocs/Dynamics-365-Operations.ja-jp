---
title: 出荷割引
description: この記事では、Microsoft Dynamics 365 Commerce 内の出荷割引機能と、その機能を使用するために必要な設定について説明します。
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: f19566ce64becea4a53a8479cb5a08579567cda1
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346399"
---
# <a name="shipping-discount"></a>出荷割引

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce 内の出荷割引機能と、その機能を使用するために必要な設定について説明します。

送料無料または送料割引は、顧客がオンライン購入を決める際に影響を与える要因の 1 つです。 多くの小売業者は、トランザクションごとの収益を上げるために、自由出荷特典を利用してカートのサイズを大きくするように顧客を促しています。

Commerce は出荷割引機能をサポートしています。この機能を使用すると、トランザクションの特定品目の合計売上金額が特定の基準を満たしている場合に、小売業者は特定の出荷方法の出荷費用の割引率を構成できるようになります。 出荷割引機能を使用するシナリオの例として、"$50 以上の購入で翌日配達が無料" があります。

## <a name="prerequisites"></a>必要条件

出荷割引機能は、Commerce の [オムニチャネルの高度な自動請求](/dynamics365/unified-operations/retail/omni-auto-charges) 機能がサポートします。 出荷割引機能を使用するには、Commerce headquarters の **Commerce パラメーター** ページで **顧客注文** タブにある **高度な自動請求** の構成を有効にする必要があります。 小売業者は、高度な自動請求機能を使用して、処理、インストール、処分など、あらゆる種類の請求を設定できます。

これらの出荷割引は、出荷費用にのみ適用されます。 そのため、小売業者は、どの費用が出荷費用かを指定する必要があります。 出荷費用を指定するには、Commerce headquarters で **チャネル設定 \> 費用 \> 費用コード** に移動し、**出荷費用** オプションで **はい** を選択して使用する費用を設定します。

![出荷費用として請求金額を指定する。](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>構成

出荷割引機能は階層ベースであり、**値引き率** の計算タイプのみをサポートします。 Commerce headquarters で出荷割引を設定するには、**価格と割引 \> 出荷割引しきい値** に移動します。 その後、割引が適用される出荷モードを指定し、数量が 1 つ以上のしきい値を定義して、各しきい値の割引率を設定できます。 カテゴリまたは製品の一覧を、特定の品目として構成することもできます。 この方法では、トランザクションの合計がしきい値を満たすかどうかを価格決定エンジンが評価する際に、トランザクション内の品目に対する売上金額だけがカウントされます。

> [!NOTE]
> 他の割引タイプとは異なり、出荷割引では割引行は作成できません。 代わりに、出荷費用を直接編集し、費用の説明に割引の名前を追加します。

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: 優先技術者の設定
description: 作業者をサービス合意またはサービス注文の優先技術者として選択できます。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37986d6d939ad368e5be6a4696f0122ae8781065b61dc2178f817366ce993a64
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734070"
---
# <a name="set-up-a-preferred-technician"></a>優先技術者の設定 

[!include [banner](../includes/banner.md)]


作業者をサービス合意またはサービス注文の優先技術者として選択できます。 ただし、作業者が **派遣表** に含まれるように、作業者を適切な派遣チームに追加することをお勧めします。

## <a name="assign-employee-to-a-dispatch-team"></a>派遣チームへの従業員の割り当て

1.  **人事管理** \> **共通** \> **作業者** \> **作業者** の順にクリックします。 作業者の詳細ページを開くには、作業者をダブルクリックします。 **アクション ウィンドウ** で、**設定**\>**派遣チーム** をクリックして、**出荷作業者** フォームを開きます。

2.  **派遣チーム** フィールドで、作業者を割り当てるチームを選択します。

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>サービス合意への優先技術者の割り当て

1.  **サービス管理** \> **共通** \> **サービス契約** \> **サービス契約** の順にクリックします。 詳細フォームを開くには、サービス合意をダブルクリックします。

2.  **一般** タブで、**優先技術者** フィールドを選択し、適切な派遣チームのメンバをサービス合意の優先技術者として割り当てます。

## <a name="assign-a-preferred-technician-to-a-service-order"></a>サービス注文への優先技術者の割り当て

1.  **サービス管理** \> **定期処理** \> **派遣表** の順にクリックします。
    

    > [!NOTE]
    > <P><STRONG>派遣表</STRONG>フォームで、表示する派遣活動の日付範囲を指定します。 さらに、終了した活動を表示するかどうか、および派遣活動リストを自分が所属するチームまたは監視する権限があるチームに制限するかどうかを指定します。 <STRONG>OK</STRONG>をクリックして<STRONG>派遣表</STRONG>フォームを開きます。</P>



2.  変更するサービス活動の明細行を選択します。

3.  **関連** タブで、**作業者** リストを使用して、適切な派遣チームのメンバをサービス コールの優先技術者として割り当てます。

## <a name="see-also"></a>参照

[サービス契約の作成および締結の概要](service-agreements.md)

[サービス注文の手動作成](create-service-orders-manually.md)

[サービス契約 (フォーム)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
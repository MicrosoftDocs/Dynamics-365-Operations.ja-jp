---
title: 返品品目を検査に渡す
description: 返品品目を登録する場合、品目を在庫に戻すか、なんらかの手段で処分する前に、品目を検査に送ります。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7207c54a88b8a7fc6c38db50c4916d1fc16b5ec4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006683"
---
# <a name="pass-returned-items-on-to-inspection"></a>返品品目を検査に渡す 

[!include [banner](../includes/banner.md)]


返品品目を登録する場合、品目を在庫に戻すか、なんらかの手段で処分する前に、品目を検査に送ることがあります。

1.  **在庫管理** \> **仕訳帳** \> **品目到着** \> **品目到着** の順にクリックします。
    
    \-または-
    
    **在庫管理** \> **仕訳帳** \> **品目到着** \> **生産入力** の順にクリックします。

2.  通常どおり、**在庫場所仕訳帳** フォームで、品目の受入を登録してください。
    

    > [!NOTE]
    > <P>返品品目の受入登録の詳細については、<A href="register-the-receipt-of-returned-items.md">返品品目の受取の登録</A>を参照してください。</P>



3.  **既定値** タブの、**取扱方法** 領域で、**検査管理** ボックスをオンにします。

システムから検査指示が作成され、検査の担当者または担当部署が **検査指示** フォームを使ってこの指示に対応します。

## <a name="see-also"></a>参照

[検査による返却品目の受入](take-returned-items-through-inspection.md)

[返品品目の廃棄方法の指定](specify-how-to-dispose-of-returned-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
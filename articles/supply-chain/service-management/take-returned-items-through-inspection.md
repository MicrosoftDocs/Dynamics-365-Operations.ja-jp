---
title: 検査による返却品目の受入
description: 検査による返却品目を受け入れます。
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41214663ec48a8cbcd8bec7f6801adb4311b2373
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669939"
---
# <a name="take-returned-items-through-inspection"></a>検査による返却品目の受入 

[!include [banner](../includes/banner.md)]


1.  **在庫管理** \> **定期処理** \> **品質管理** \> **検査指示** の順にクリックします。

2.  検査する返品品目に対応する注文明細行を検索します。

    > [!NOTE]
    > <P>1 つの検査指示は、1 つの品目番号にのみ関連付けることができます。 品目番号が異なる 10 個の品目が一度の出荷で返品されて検査に送られる場合、10 個の別々の検査指示が作成されます。</P>

3.  品目を調べた後、**廃棄コード** フィールドで選択を行って、品目に対する作業、および関連する財務トランザクションの処理方法を示します。 たとえば、品目を在庫に戻して顧客に払戻したり、品目を廃棄して顧客に交換品目を送ったり、品目を貸方なしで顧客に返送したりします。
    
    > [!NOTE]
    > <P>1 つの品目番号のバッチに含まれる複数の返品品目に同一の廃棄コードを割り当てられない場合、サブバッチごとに異なる廃棄コードを割り当てるために検査指示を分割 (<STRONG>機能</STRONG> &gt; <STRONG>分割</STRONG>) する必要があります。</P>


4.  検査が終了したら、**完了レポート** をクリックし、返品品目をリリースして着荷仕訳帳のエントリを作成します。 次に、品目を入庫した担当者または部門が、在庫に戻される品目の仕訳を処理します。
    
    - または -
    
    検査指示を終了し、いずれかの **在庫** 機能を使用して品目を在庫に直接移動します。

5.  フォームを閉じて、変更を保存します。

## <a name="see-also"></a>参照

[返品品目の廃棄方法の指定](specify-how-to-dispose-of-returned-items.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
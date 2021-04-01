---
title: 返品品目の廃棄方法の指定
description: 返品品目の廃棄方法を指定します。
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61bff50d55ed4c251918a327f2a033369e731bf0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242376"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>返品品目の廃棄方法の指定 

[!include [banner](../includes/banner.md)]


返品注文を処理する場合、製品が返品されている理由を識別する返品理由コードを指定する必要があります。 返品製品自体に何が実行されたかを特定する廃棄コード、および処分アクションも指定する必要があります。

廃棄コードは、返品注文の作成、品目到着の登録または品目到着の梱包明細の更新、および検査指示の終了時に適用できます。

業務プロセスをサポートするため、任意の必要な廃棄コードを定義できます。 次の表に、返品品目の廃棄を割り当てるために一般的に使用されるコードを示します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>廃棄タイプ</p></th>
<th><p>一般的なコード</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>処分</p></td>
<td><p>SC</p></td>
<td><p>解体/廃棄</p></td>
</tr>
<tr class="even">
<td><p>処分</p></td>
<td><p>DC</p></td>
<td><p>慈善活動に寄贈</p></td>
</tr>
<tr class="odd">
<td><p>処分</p></td>
<td><p>TD</p></td>
<td><p>サード パーティによる廃棄</p></td>
</tr>
<tr class="even">
<td><p>処分</p></td>
<td><p>SL</p></td>
<td><p>回収</p></td>
</tr>
<tr class="odd">
<td><p>処分</p></td>
<td><p>TS</p></td>
<td><p>サード パーティへの売却 (二次市場)</p></td>
</tr>
<tr class="even">
<td><p>修復/変更</p></td>
<td><p>RW</p></td>
<td><p>再加工</p></td>
</tr>
<tr class="odd">
<td><p>修復/変更</p></td>
<td><p>RF</p></td>
<td><p>再製品化/修繕</p></td>
</tr>
<tr class="even">
<td><p>修復/変更</p></td>
<td><p>MD</p></td>
<td><p>変更</p></td>
</tr>
<tr class="odd">
<td><p>修復/変更</p></td>
<td><p>RP</p></td>
<td><p>修復</p></td>
</tr>
<tr class="even">
<td><p>修復/変更</p></td>
<td><p>RV</p></td>
<td><p>仕入先に返品</p></td>
</tr>
<tr class="odd">
<td><p>その他</p></td>
<td><p>AI</p></td>
<td><p>現状のまま使用</p></td>
</tr>
<tr class="even">
<td><p>その他</p></td>
<td><p>RS</p></td>
<td><p>再販売</p></td>
</tr>
<tr class="odd">
<td><p>その他</p></td>
<td><p>前</p></td>
<td><p>交換</p></td>
</tr>
<tr class="even">
<td><p>その他</p></td>
<td><p>Ms.</p></td>
<td><p>雑費</p></td>
</tr>
</tbody>
</table>


定義した各廃棄コードごとに、処分アクションを選択する必要があります。 処分アクションにより、廃棄コードの物理的および財務的意味が決まります。 たとえば、交換品目を顧客に送る必要がある場合、処分アクションにより、返品品目の物理的な処理や返品品目の財務上の影響などが決まります。 業務のニーズに応じて廃棄コードの数を任意に定義できますが、6 種類の定義済の処分アクションのみ選択できます。 次の表に、処分アクションとその定義を示します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>処分アクション</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>クレジット</strong></p></td>
<td><p>品目を在庫に返品し、顧客に対して貸方転記します。</p></td>
</tr>
<tr class="even">
<td><p><strong>貸方のみ</strong></p></td>
<td><p>品目の返品を要求または期待せずに、顧客に対して貸方転記します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>仕損</strong></p></td>
<td><p>品目を処分して、顧客に対して貸方転記します。</p></td>
</tr>
<tr class="even">
<td><p><strong>置換と貸方転記</strong></p></td>
<td><p>品目を在庫に戻して、交換注文を作成し、顧客に対して貸方転記します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>置換と仕損</strong></p></td>
<td><p>品目の処分し、交換注文を作成し、顧客に対して貸方転記します。</p></td>
</tr>
<tr class="even">
<td><p><strong>顧客に戻る</strong></p></td>
<td><p>品目の返品を拒否して、顧客に返送します。</p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a>検査指示の廃棄コードの選択

1.  **在庫管理** \> **定期処理** \> **品質管理** \> **検査指示** の順にクリックします。

2.  既存の検査指示に対して、**概要** タブの **廃棄コード** フィールドからアクションを選択します。



## <a name="see-also"></a>参照

[検査指示 (フォーム)](https://technet.microsoft.com/library/aa554073(v=ax.60))

[廃棄コード (フォーム)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
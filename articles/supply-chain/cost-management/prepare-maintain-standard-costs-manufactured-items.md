---
title: 製造品目の標準原価を管理するための準備
description: このトピックでは、製造品目の原価の管理を準備するステップについて説明します。
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f428f2e3966155b4fc95fd94b6a55d059eb3533d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263521"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>製造品目の標準原価を管理するための準備

[!include [banner](../includes/banner.md)]

このトピックでは、製造品目の原価の管理を準備するステップについて説明します。 製造品目のステップは、購入品目のステップからわずかに異なっています。

製造品目に割り当てられているポリシーは、親製造品目の原価計算に影響を与える可能性があります。 製造品目の原価の管理を準備するには、次の手順を実行します。

1. 製造品目に品目モデル グループを割り当てます。 

   品目モデル グループは、標準原価が使用されることを示します。

2. 製造品目に品目グループを割り当てます。 

   品目グループには、製造品目に適用する勘定科目が含まれます。 標準原価在庫モデルを持つ製造品目の勘定科目には、複数の製造差異、原価変更差額、および在庫原価再評価が含まれます。

3. 品目に在庫単位を割り当てます。 

   品目の原価は、常に品目の在庫単位で表現されます。

4. 原価グループは、品目を購入品目として扱わない場合、製造品目に割り当てないでください。

5. 部品表 (BOM) 計算グループを製造品目に割り当てます。 

   品目の BOM 計算グループは、適用する警告条件を定義します。 これにより、BOM 計算が行われた時に、計算エラーの考えられる原因についての警告メッセージが生成されるようになります。 たとえば、有効な BOM または工順が存在しないときに、警告メッセージでそれを示すことができます。 BOM 計算グループには、製造品目をいつ購入品目として扱うかを示す展開停止ポリシーが含まれています。

6. 製造品目に固定費がある場合は、標準注文数量を製造品目に割り当てます。 

   標準注文数量は、固定費を償却する際の会計ロット サイズです。 固定費には、工順操作での設定回数および BOM の固定コンポーネントの数量が含まれます。

7. 製造品目の BOM を定義します。 

   1 つまたは複数の BOM バージョンを、1 つの製造品目に対して定義できます。 必要なバージョンが承認済みで有効と指定され、そのバージョンに適切な有効日が設定されていることを確認します。 BOM バージョンは、会社全体またはサイト固有のどちらでもかまいません。

8. 製造品目の工順を定義します。 

   1 つまたは複数の工順バージョンを、1 つの製造品目に対して定義できます。 必要なバージョンが承認済みで有効と指定され、そのバージョンに適切な有効日が設定されていることを確認します。 工順バージョンは、サイト固有である必要があります。

原価計算のために工順情報を使用したい場合は、追加の準備手順が必要です。 たとえば、工順操作には正確で完全な原価カテゴリを割り当てる必要があります。

<a name="related-topics"></a>関連トピック
--------

[製造品目の固定費の償却](amortize-constant-costs-manufactured-item.md)

[生産または調達する製品を設定する](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
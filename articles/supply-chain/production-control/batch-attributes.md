---
title: バッチ属性 (複数)
description: この記事では、バッチ属性に関する情報を提供します。 バッチ属性は、在庫バッチを構成する原材料および完成製品の特性です。 この記事では、バッチ属性の割り当て方法と、バッチの引当を行うときにそれらを検索する方法についても説明します。
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e5f5a03df63cf4fa90b5e9e67082a0d60eef9afc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899385"
---
# <a name="batch-attributes"></a>バッチ属性 (複数)

[!include [banner](../includes/banner.md)]

この記事では、バッチ属性に関する情報を提供します。 バッチ属性は、在庫バッチを構成する原材料および完成製品の特性です。 この記事では、バッチ属性の割り当て方法と、バッチの引当を行うときにそれらを検索する方法についても説明します。

バッチ属性は、在庫バッチを構成する原材料および完成製品の特性です。 バッチ属性は環境条件、バッチの生産に使用される原材料の品質、完成品の結果などの要因によって異なります。 使用されるバッチ属性の数とタイプは、業界によって大きく異なります。 以下はバッチ属性の 2 つの使用例です。

-   チーズ業界でチーズを生産するための原材料の 1 つとして使用される牛乳は、脂肪分や重量パーセントなどの属性を持つ場合があります。 牛乳から生産されたチーズは、水分や年数などの属性を持つ場合があります。
-   鉄鋼業界で生産される鉄は、マグネシウム、銀、および亜鉛の含有比率などの属性を持つ場合があります。

属性の数とタイプをより上手に管理するために、バッチ属性グループを使用できます。 これにより、各属性を個別に追加する必要がなくなります。

## <a name="assign-batch-attributes"></a>バッチ属性の割り当て
在庫バッチの属性を在庫バッチで扱われる個々の製品に割り当てるか、それらを特定の顧客に関連付けられた製品に割り当てることができます。 顧客レベルでバッチ属性を割り当てる前に、製品レベルで割り当てる必要があります。 製品は、 追跡用分析コード グループで **有効** に設定されたバッチ分析コードが必要です。 個々の製品にバッチ属性を割り当てるには、製品固有ページを使用します。 属性が顧客の製品に固有な場合、顧客固有ページを使用します。 製品に属性を追加する場合、他のパラメータを定義します。 次にいくつか例を挙げます。

-   **整数** または **小数** タイプ属性の最小値と最大値幅。
-   **整数** または **小数** タイプの属性の許容アクション。 属性の値が最小と最大の範囲外にある場合、アクションは警告メッセージまたはエラー メッセージのいずれかです。
-   属性のターゲット値。 この値は、属性の最適な値であり、すべての属性タイプに適用されます。

[製品情報管理] の **リリースされた製品** リスト ページで選択する商品についてのページを使用できます。 製品へのバッチ属性を割り当てた後、**在庫バッチ属性** ページの属性に特定の値を追加できます。

## <a name="reserve-batches"></a>バッチ引当
顧客の注文を満たすための販売注文のバッチの引当を行うときや、製造オーダーでバッチのピッキングや引当を行うとき、バッチ属性で検索できます。 検索では、必要なバッチ属性を持つ製品を含む在庫バッチを見つけます。 バッチを見つけた後、元の在庫トランザクション明細行に製品を引当できます。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
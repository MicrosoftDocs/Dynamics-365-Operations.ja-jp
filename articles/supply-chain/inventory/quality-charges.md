---
title: 不適合工程の諸費用
description: このトピックでは、不適合の工程で使用できる品質諸費用を作成する方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c062fecea23017e603c55d11de542942576dba74e0dda07452fd7a91109fe78
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771494"
---
# <a name="charges-for-nonconformance-operations"></a>不適合工程の諸費用

[!include [banner](../includes/banner.md)]

このトピックでは、不適合の工程で使用できる品質諸費用を作成する方法について説明します。

**品質諸費用** ページを使用して、不適合の行程で追加できる諸費用の種類を定義します。 諸費用を使用すると、不適合製品に対して顧客に支払う必要がある手数料や諸費用、または受け取った不適合製品に対して仕入先が支払う必要がある手数料や諸費用に関する詳細を追跡できます。 また諸費用を使用して、外部の仕入先または工程を実行するサービスに対して必要な原価を追跡することもできます。

## <a name="examples-of-quality-charges"></a>品質諸費用の例

製造会社に勤務しているとします。 会社は複数の仕入先と契約を結んでいます。 これらの契約では、品目の期限内出荷、損害、および製品品質に関する基準が示されます。 同様に、複数の顧客が、返品、損害、および製品品質に関して会社と合意しています。

手数料構造は状況ごとに定義され、契約で指定されます。 品質諸費用を構成して、*損害*、*遅延出荷*、*品質* などさまざまな種類の費用を概要できます。 その後、不適合を作成するときに、1 つ以上の行程を追加します。 各行程に対して、**諸費用** を選択して手数料の詳細を定義します。

## <a name="create-a-quality-charge"></a>品質諸費用を作成する

1. **在庫管理 \> 設定 \> 品質管理 \> 品質諸費用** の順に移動します。
1. アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。 続いて、新しい行に次のフィールドを設定します:

    - **諸費用コード** – 品質諸費用の固有の ID または名前を入力します。
    - **説明** – 品質諸費用の詳細説明を入力します。

1. ページを閉じます。

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a>不適合の行程に品質諸費用を追加する

不適合に行程を追加し、諸費用を適用する方法の詳細については、[不適合の工程](quality-operations.md)を参照してください。

## <a name="additional-resources"></a>追加リソース

- [品質管理の概要](quality-management-processes.md)
- [品質および不適合管理の有効化](enable-quality-management.md)
- [不適合の承認を担当する作業者](quality-responsible-workers.md)
- [不適合の検査ゾーン](quality-quarantine-zones.md)
- [不適合の診断タイプ](quality-diagnostic-types.md)
- [不適合の品質諸費用](quality-charges.md)
- [不適合の工程](quality-operations.md)
- [倉庫プロセスに対する品質管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

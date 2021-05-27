---
title: 不適合の問題タイプ
description: このトピックでは、不適合の問題タイプを作成および使用する方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 742edec8570610efe41a2c627efd1df586e0733e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022159"
---
# <a name="problem-types-for-nonconformances"></a>不適合の問題タイプ

[!include [banner](../includes/banner.md)]

このトピックでは、不適合の問題タイプを作成および使用する方法について説明します。

**問題タイプ** ページを使用して、さまざまな不適合タイプで発生する可能性のある品質上の問題の分類を定義します。 作成する問題タイプごとに、問題タイプを使用できる不適合のタイプを指定する必要があります。 次の不適合タイプを設定できます。

- **内部** – このタイプの不適合は、手持在庫に関連しています (たとえば、品質指示や検査指示)。
- **顧客** – このタイプの不適合は、販売注文に関連しています。
- **仕入先** – このタイプの不適合は、発注書に関連しています。
- **サービス要求** – このタイプの不適合は、サービス注文に関連しています。
- **生産** – このタイプの不適合は、バッチ オーダーまたは製造オーダーに関連しています。
- **連産品の生産** – このタイプの不適合は、連産品のバッチ オーダーに関連しています。

新しい問題タイプを作成する場合は、アクション ウィンドウで **不適合タイプ** を選択して、その問題タイプに対して承認されている 1 つ以上の不適合タイプの一覧を作成します。 たとえば、欠陥コードに関する問題タイプは、すべての不適合タイプに適用される場合があります。 ただし、顧客の苦情に関連する問題タイプは、**顧客** および **サービス要求** の不適合タイプにのみ適用される場合があります。

## <a name="examples-of-problem-types"></a>問題タイプの例

さまざまな不適合タイプで使用できる問題タイプのシナリオの例を次に示します。

- **顧客:** 顧客が苦情を申し立て、顧客が返品を行った、または品質仕様が満たされていなかった。
- **仕入先:** 製品が破損していた、品質仕様が満たされていなかった、または間違った製品を受け取った。
- **サービス要求:** 品質仕様が満たされていなかった、顧客が苦情を申し立てた、または機械のメンテナンスが必要である。
- **生産:** 品質仕様を満たしていない、機械のメンテナンスが必要、または製品が破損していた。
- **連産品の生産:** 品質仕様を満たしていない、機械のメンテナンスが必要、または製品が破損していた。

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>問題タイプの作成および不適合タイプへの割り当て

1. **在庫管理 \> 設定 \> 品質管理 \> 問題タイプ** の順に移動します。
1. アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。 続いて、新しい行に次のフィールドを設定します:

    - **問題タイプ** – 問題タイプの固有の ID または名前を入力します。
    - **説明** – 問題タイプの詳細説明を入力します。

1. 新しい行がまだ選択されている間に、アクション ウィンドウで **不適合** タイプを選択します。
1. アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。 次に、新しい行に対して、**不適合タイプ** フィールドを、問題タイプに対して許可する不適合タイプに設定します。
1. 問題タイプに対して許可する追加の不適合タイプごとに、前の手順を繰り返します。
1. ページを閉じます。

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

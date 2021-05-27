---
title: 不適合の工程
description: このトピックでは、不適合の工程を作成および使用する方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a6cc88b80f82d77edac0341cb6a3c0db4b42ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022207"
---
# <a name="operations-for-nonconformances"></a>不適合の工程

[!include [banner](../includes/banner.md)]

このトピックでは、不適合の工程を作成および使用する方法について説明します。

**工程** ページを使用して、承認済の不適合に対して実行される作業の分類を定義します。 関連する工程を不適合に割り当てるときに、関連する材料、労働時間、諸経費など、その工程を実行するために必要な詳細を指定できます。 システムはこの情報を使用して、工程の見積原価を計算します。 詳細情報および見積原価は、参考目的で提供されます。 品質に関連する工程は、生産工順に対して定義できる工程とは異なります。

> [!NOTE]
> 不適合に関連する行程で使用される原価、時間、および品目を追跡できますが、入力するデータは情報提供にすぎません。 総勘定元帳、在庫の補助元帳、または **時刻と出勤** モジュールと自動的に統合されません。

## <a name="examples-of-operations"></a>行程の例

製造会社に勤務しているとします。 品質テストに合格しなかった品目に対して不適合が作成および承認されました。 問題が機械のベアリング不良に関連していることを示す修正が作成されました。 ベアリングを交換するには、いくつかの手順が必要であり、各工程の責任が追跡されます。 たとえば、次の手順が必要になる場合があります:

1. 生産ラインが停止され、定期クリーンアウトが実行されます。
1. メンテナンス担当者がベアリングを交換します。
1. 品質保証の担当者は、電源を入れる前に機械を検査します。

この例では、実行する必要がある作業を表すため次の行程を作成できます:

- 生産ラインを停止します。
- 生産ラインをクリーンアウトします。
- 機械メンテナンスを実行します。
- 機械を検査します。

## <a name="create-an-operation"></a>行程を作成する

1. **在庫管理 \> 設定 \> 品質管理 \> 工程** の順に移動します。
1. アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。 続いて、新しい行に次のフィールドを設定します:

    - **行程** – 行程の固有の ID または名前を入力します。
    - **説明** – 行程の詳細説明を入力します。
    - **タイプ** – 工程が特定のタイプの注文に関連する不適合でのみ使用できる場合は、注文タイプ (*発注書* または *販売注文*) を選択します。

1. ページを閉じます。

## <a name="additional-resources"></a>追加リソース

- [品質管理の概要](quality-management-processes.md)
- [品質および不適合管理の有効化](enable-quality-management.md)
- [不適合の作成および処理](tasks/create-process-non-conformance.md)
- [不適合の承認を担当する作業者](quality-responsible-workers.md)
- [不適合の検査ゾーン](quality-quarantine-zones.md)
- [不適合の診断タイプ](quality-diagnostic-types.md)
- [不適合の品質諸費用](quality-charges.md)
- [不適合の問題タイプ](quality-operations.md)
- [倉庫プロセスに対する品質管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

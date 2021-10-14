---
title: 不適合の診断タイプ
description: このトピックでは、不適合で使用できる診断タイプの使用方法および作成方法について説明します。
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: edaa3a8b5c6446f039f33589166d832dcd9d0b9a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580939"
---
# <a name="diagnostic-types-for-nonconformances"></a>不適合の診断タイプ

[!include [banner](../includes/banner.md)]

このトピックでは、不適合で使用できる診断タイプの使用方法および作成方法について説明します。

診断アクションの分類を定義するには、**診断タイプ** ページを使用します。 その後、不適合に対する修正を作成するときに、診断を選択します。 訂正は、承認された不適合に対して行う必要のある診断アクションのタイプ、担当者などを指定します。 また、要求された完了日、予定完了日を指定します。

## <a name="examples-of-diagnostic-types"></a>診断タイプの例

製造会社で勤務しており、複数の品目が品質テストに合格しなかったとします。 これらの品目は検査領域に移動し、不適合製品としてマークされます。 不適合レコードが Microsoft Dynamics 365 Supply Chain Management で作成され、問題解決を通じて詳細を追跡します。

この例では、品目のパッケージ化する機械のベアリングが劣化し過熱しているため、品質上の問題が発生しています。 この問題の修正には、機械の部品の交換が必要です。

診断タイプを構成する場合、複数のレコードを作成できます。各レコードは、機械に発生する可能性のあるさまざまな種類の問題を表します。 または、機械の修理を表す 1 つの包括的な診断タイプを作成できます。

## <a name="create-a-diagnostic-type"></a>診断タイプを作成する

1. **在庫管理 \> 設定 \> 品質管理 \> 診断タイプ** の順に移動します。
1. アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。 続いて、新しい行に次のフィールドを設定します:

    - **診断** – 診断タイプの固有の ID または名前を入力します。
    - **説明** – 診断タイプの詳細説明を入力します。

1. ページを閉じます。

## <a name="additional-resources"></a>追加リソース

- [品質管理の概要](quality-management-processes.md)
- [品質および不適合管理の有効化](enable-quality-management.md)
- [不適合の承認を担当する作業者](quality-responsible-workers.md)
- [不適合の検査ゾーン](quality-quarantine-zones.md)
- [不適合の問題タイプ](quality-problem-types.md)
- [不適合の品質諸費用](quality-charges.md)
- [不適合の工程](quality-operations.md)
- [倉庫プロセスに対する品質管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: 不適合の検査ゾーン
description: このトピックでは、不適合の検査ゾーンを作成および使用する方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c770da899f07597896d0d392b5192ddc4162bec6271d0e11c34797d7a15f857e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754038"
---
# <a name="quarantine-zones-for-nonconformances"></a>不適合の検査ゾーン

[!include [banner](../includes/banner.md)]

このトピックでは、不適合の検査ゾーンを作成および使用する方法について説明します。

**検査ゾーン** ページを使用して、不適合に割り当てることができるゾーンを定義します。 不適合を作成する場合、**不適合** ページの **全般** タブで、**検査ゾーン** フィールドおよび **検査タイプ** フィールドを設定できます。 **検査ゾーン** フィールドは通常、品目が保管されているエリアまたは場所を示します。 **検査タイプ** フィールドは、品目を *使用制限* または *使用不可* として定義します。

不適合または不適合の修正レポートを印刷すると、品目が配置されている検査ゾーンを表示できます。

不適合の不適合タグを印刷することもできます。 このレポートには、割り当てられた検査ゾーンと使用法に関する情報が表示され、欠陥材料をどのように扱うべきかに関するガイダンスが提供されます。 検査ゾーンは在庫場所または運営リソースに対応する場合があります。

## <a name="examples-of-quarantine-zones"></a>検査ゾーンの例

### <a name="example-1"></a>例 1

テレビ、スピーカー、メディア プレーヤーを製造および販売している電子製品製造会社で働いているとします。 この場合、各タイプの製品を表す検査ゾーンを構成できます。

### <a name="example-2"></a>例 2

3 つの容器と 2 つのラックは、不適合品目を保管するために使用されます。 この場合は、5 つの検査ゾーン (各容器と各ラックごとに 1 つずつ) を構成できます。

## <a name="create-a-quarantine-zone"></a>検査ゾーンの作成

1. **在庫管理 \> 設定 \> 品質管理 \> 検査ゾーン** の順に移動します。
1. アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。 続いて、新しい行に次のフィールドを設定します:

    - **検査ゾーン** – 検査ゾーンの固有の ID または名前を入力します。
    - **説明** – 検査ゾーンの詳細説明を入力します。

1. ページを閉じます。

## <a name="additional-resources"></a>追加リソース

- [品質管理の概要](quality-management-processes.md)
- [品質および不適合管理の有効化](enable-quality-management.md)
- [不適合の承認を担当する作業者](quality-responsible-workers.md)
- [不適合の問題タイプ](quality-quarantine-zones.md)
- [不適合の診断タイプ](quality-diagnostic-types.md)
- [不適合の品質諸費用](quality-charges.md)
- [不適合の工程](quality-operations.md)
- [倉庫プロセスに対する品質管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

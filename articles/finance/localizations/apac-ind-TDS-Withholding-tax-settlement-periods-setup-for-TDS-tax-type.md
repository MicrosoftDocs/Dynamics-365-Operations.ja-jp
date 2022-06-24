---
title: TDS 税タイプに対する源泉徴収税精算期間の設定
description: この記事では、源泉徴収税 (TDS) 決済期間の決済帰還を設定する方法について説明します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 855bda71f0967c53166cf0a7f5e7e465146f34a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846558"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a>TDS 税タイプに対する源泉徴収税精算期間の設定

[!include [banner](../includes/banner.md)]

この記事では、源泉徴収税 (TDS) 決済期間の決済帰還を設定する方法について説明します。

1. **税 \> 間接税 \> 源泉徴収税 \> 源泉徴収税決済期間** の順に移動します。

    [![源泉徴収税の背取るメント期間ページ。](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)

2. **税タイプ** フィールドで、**TDS** を選択して、TDS 税タイプの源泉徴収税決済期間を設定します。
3. **新規** を選択して、明細行を作成します。
4. **決済期間** フィールドに、TDS 決済期間の名前を入力します。
5. **説明** フィールドに説明を入力します。
6. **源泉徴収税オーソリティ** フィールドで、TDS 決済期間を定義する TDS オーソリティを選択します。
7. **一般** クイック タブの **期間間隔** フィールドで、TDS 決済期間の期間間隔のタイプを選択します。
8. **単位数** フィールドで、期間間隔タイプの単位数を指定します。
9. **期間** クイック タブの **開始日** フィールドで、TDS 決済期間の開始日を選択します。 **終了日** フィールドで、終了日を選択します。
10. 既存の期間、期間間隔および期間単位に基づいてその後のTDS決済期間を作成するには、**新しい期間** を選択します。
11. 特定の決済期間に対して実行される定期 TDS 決済の詳細を表示するには、**源泉徴収税の支払** を選択して **源泉徴収税の支払** ページ を開きます。

    > [!NOTE]
    > 定期的な TDS 決済プロセスを実行するには、**一般会計 \> 定期 \> 源泉徴収税 \> 源泉徴収税の支払** に移動します。

    [![源泉徴収税支払のページ。](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)

12. ページを閉じます。

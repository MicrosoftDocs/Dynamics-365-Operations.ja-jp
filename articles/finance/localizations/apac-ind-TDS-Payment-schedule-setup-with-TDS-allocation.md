---
title: TDS 配賦の支払スケジュールの設定
description: このトピックでは、源泉徴収 (TDS) の配賦を考慮した支払いスケジュールを設定する方法について説明します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023396"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>TDS 配賦の支払スケジュールの設定

[!include [banner](../includes/banner.md)]

このトピックでは、源泉徴収 (TDS) の配賦を考慮した支払いスケジュールを設定する方法について説明します。

1. **買掛金勘定 \> 支払の設定 \> 支払スケジュール** の順に移動します。

    [![支払スケジュール ページ](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. アクション ペインで、**新規** を選択して、支払いスケジュールを作成し、必要な情報を入力します。
3. **配賦** フィールドで、支払スケジュールの支払の配賦に使用する手段を選択します。

    - 小計
    - 固定金額
    - 固定数量
    - 指定

    **源泉徴収税の配賦** フィールドには、支払スケジュールの TDS の配賦方法が表示されます。 **配賦** フィールドで **合計** を選択すると、**源泉徴収税の配賦** フィールドが自動的に **合計** に設定されます。 **配賦** フィールドで **固定金額**、**固定数量**、または **指定済** を選択した場合、**源泉徴収税の配賦** フィールドが自動的に **比例して** 設定されます。

    > [!NOTE]
    > **源泉徴収税の配賦** フィールドが **合計** に設定されている場合は、TDS 金額を含む総額に基づいて支払の配分が計算されます。 **源泉徴収税の配賦** フィールドが **比例** に設定されている場合は、分割払いは、TDS金額を差し引いた後の正味の請求書金額に基づいて計算されます。

4. その他の必要な詳細をフォームに入力し、ページを閉じます。

---
title: TDS 支払および TDS 清算期間に対して転記されたトランザクションの表示
description: このトピックでは、決済期間に転記された源泉徴収税 (TDS) の支払およびトランザクションでを表示する方法について説明します。
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 2921cb22bedf04db1c8d11a382b979b3c63e6683
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349979"
---
# <a name="view-posted-tds-payments-and-transactions-for-a-tds-settlement-period"></a>TDS 支払および TDS 清算期間に対して転記されたトランザクションの表示

[!include [banner](../includes/banner.md)]

このトピックでは、決済期間に転記された源泉徴収税 (TDS) の支払およびトランザクションでを表示する方法について説明します。

1. **税 \> 間接税 \> 源泉徴収税 \> 源泉徴収税決済期間** の順に移動します。

    [![源泉徴収税の背取るメント期間ページ。](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)

2. **源泉徴収税の精算期間** ページで、**源泉徴収税の支払い** を選択して **源泉徴収税の支払** ページを開き、特定の TDS 決済期間に対して行われた TDS 決済を表示できます。

    **概要** タブには次の情報が表示されます:

    - **日付** – TDS 決済の日付。
    - **伝票** – TDS 決済取引の伝票番号。
    - **税タイプ** - 決済プロセスが実行される税タイプ。
    - **税勘定番号 (TAN)** - 決算済 TDS トランザクションの税勘定番号。
    - **決済期間** - 決済プロセスを実行する TDS の決済期間。
    - **開始日** - 決済期間の開始日。
    - **終了日** - 決済期間の終了日。
    - **源泉徴収税の支払バージョン** -  源泉徴収税支払のバージョン: **元の**、**最新の訂正**、または **合計リスト**。

5. TDS トランザクションの伝票エントリを表示するには、**伝票** を選択します。
6. 精算期間中に特定の期間に決済された TDS トランザクションの詳細を表示するには、**源泉徴収税トランザクション** を選択します。 TDS トランザクションの伝票エントリを表示するには、**伝票** を選択します。 特定の TDS 税コードの TDS 税要素ごとに計算された TDS を表示するには、**源泉徴収税コンポーネント** を選択します。
7. **源泉徴収税の支払** ページを閉じて、**源泉徴収税の精算期間** ページに戻ります。
8. 精算期間中に特定の期間に決済された TDS トランザクションの詳細を表示するには、**源泉徴収税トランザクション** を選択します。

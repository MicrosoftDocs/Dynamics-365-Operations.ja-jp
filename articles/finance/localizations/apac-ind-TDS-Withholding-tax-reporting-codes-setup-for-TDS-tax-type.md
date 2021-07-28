---
title: TDS 税タイプに対する源泉徴収税レポートの設定
description: 源泉徴収税レポート コードは、源泉徴収税 (TDS) のフォーム 26Q およびフォーム 27Q ステートメントを生成するために使用されます。 このトピックでは、TDS レポート コードを設定できるよう、源泉徴収税レポート コードの手順を設定する方法について説明します。
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
ms.openlocfilehash: c74132af95f088ea88155b722a8270861fba50e7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361289"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a>TDS 税タイプに対する源泉徴収税レポートの設定

[!include [banner](../includes/banner.md)]

源泉徴収税レポート コードは、源泉徴収税 (TDS) のフォーム 26Q およびフォーム 27Q ステートメントを生成するために使用されます。 このトピックでは、TDS レポート コードを設定できるよう、源泉徴収税レポート コードの手順を設定する方法について説明します。

1. **税 \> 設定 \> 源泉徴収税 \> 源泉徴収税レポート コード** に移動します。

    [![源泉徴収税レポート コード ページ。](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)

2. **税タイプ** フィールドで、**TDS** を選択して、TDS 税タイプの源泉徴収税レポート コードを定義します。
3. **源泉徴収税コンポーネント** フィールドで、源泉徴収税のレポート コードを定義する TDS コンポーネントを選択します。 **源泉徴収税コンポーネント グループ** フィールドには、定義している TDS コンポーネントに対して定義された TDS コンポーネント グループ が表示されます。

    **一般** クイック タブの **セクション コード** フィールドには、TDS コンポーネント グループに関連付けられたセクション コード が表示されます。

4. **一般** クイックタブの **レポート コード** フィールドで、TDS レポート コードを選択します。

    - TDS
    - TCS
    - 割増金
    - PE\_Cess
    - SHE\_Cess

5. ページを閉じます。

---
title: TDS 税タイプに対する源泉徴収税レポートの設定
description: 源泉徴収税レポート コードは、源泉徴収税 (TDS) のフォーム 26Q およびフォーム 27Q ステートメントを生成するために使用されます。 この記事では、TDS レポート コードを設定できるよう、源泉徴収税レポート コードの手順を設定する方法について説明します。
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
ms.openlocfilehash: bdd2e89d29807dc31d8f2d4684ee413470b1dbde
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907801"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a>TDS 税タイプに対する源泉徴収税レポートの設定

[!include [banner](../includes/banner.md)]

源泉徴収税レポート コードは、源泉徴収税 (TDS) のフォーム 26Q およびフォーム 27Q ステートメントを生成するために使用されます。 この記事では、TDS レポート コードを設定できるよう、源泉徴収税レポート コードの手順を設定する方法について説明します。

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

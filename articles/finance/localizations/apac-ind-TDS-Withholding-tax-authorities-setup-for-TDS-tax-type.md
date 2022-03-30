---
title: TDS 税タイプに対する源泉徴収税オーソリティの設定
description: このトピックでは、源泉徴収税 (TDS) オーソリティの設定方法について説明します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a9b6105c227b530f0cd7a932aac18e8942482d12
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408258"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a>TDS 税タイプに対する源泉徴収税オーソリティの設定

[!include [banner](../includes/banner.md)]

このトピックでは、源泉徴収税 (TDS) オーソリティの設定方法について説明します。

1. **税 \> 間接税 \> 源泉徴収税オーソリティ** に移動します。

    [![源泉徴収税オーソリティ ページ。](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)

2. **税タイプ** フィールドで、**TDS** を選択して、TDS 税タイプの源泉徴収税オーソリティを設定します。
3. アクション ウィンドウで **新規** を選択して、明細行を作成します。
4. **源泉徴収税オーソリティ** フィールドに、TDS オーソリティの名前を入力します。
5. **説明** フィールドに説明を入力します。
6. **一般** クイックタブの、**仕入先アカウント** フィールドで、TDS オーソリティの仕入先アカウントを選択します。

    > [!NOTE]
    > TDS オーソリティ仕入先に支払う必要がある預金を行う銀行の名前を定義する必要があります。 銀行の名前は **銀行口座** ページ (**買掛金勘定 \> すべての仕入先 \> 仕入先 \> 設定 \> 銀行口座**)。

7. ページを閉じます。

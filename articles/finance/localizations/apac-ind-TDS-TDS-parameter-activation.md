---
title: TDS パラメーターの設定
description: このトピックでは、パラメーターを設定して、指定されたトランザクションで源泉徴収税 (TDS) 機能を有効にする方法について説明します。 これは、源泉徴収税 TDS 機能を使用するために必要な手順です。
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023386"
---
# <a name="set-the-tds-parameters"></a>TDS パラメーターの設定

[!include [banner](../includes/banner.md)]

このトピックでは、パラメーターを設定して、指定されたトランザクションで源泉徴収税 (TDS) 機能を有効にする方法について説明します。 これは、源泉徴収税 TDS 機能を使用するために必要な手順です。

1. **一般会計 \> 元帳の設定 \> 一般会計パラメーター** の順に移動します。
2. **直接税** タブの **源泉徴収税** セクションで、**TDS の有効化** オプションを **はい** に設定して、TDS 機能とそれに使用されるページおよびフィールドを有効にします。
3. **請求書** オプションを **はい** に設定して、請求書レベルで TDS の計算および控除に使用されるフィールドを有効にします。
4. **支払** オプションを **はい** に設定して、支払レベルで TDS の計算および控除に使用されるフィールドを有効にします。

    [![直接税タブ](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. **番号順序** タブで、**参照** フィールドが **源泉徴収税の支払** に設定されている行を検索します。 行の **番号順序コード** フィールドで、番号順序コードを選択します。 番号順序コードは、定期的な TDS 決済プロセスの伝票番号を生成するために使用されます。

    > [!NOTE]
    > 定期的な TDS 決済プロセスを実行するには、**税 \> 申告 \> 源泉徴収税 \> 源泉徴収税の支払** に移動します。

    [![番号順序タブ](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. ページを閉じます。

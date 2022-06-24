---
title: TDS パラメーターの設定
description: この記事では、パラメーターを設定して、指定されたトランザクションで源泉徴収税 (TDS) 機能を有効にする方法について説明します。 これは、源泉徴収税 TDS 機能を使用するために必要な手順です。
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
ms.openlocfilehash: 3390cad6979858fbff73769d0d25132ba18a2157
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865616"
---
# <a name="set-the-tds-parameters"></a>TDS パラメーターの設定

[!include [banner](../includes/banner.md)]

この記事では、パラメーターを設定して、指定されたトランザクションで源泉徴収税 (TDS) 機能を有効にする方法について説明します。 これは、源泉徴収税 TDS 機能を使用するために必要な手順です。

1. **一般会計 \> 元帳の設定 \> 一般会計パラメーター** の順に移動します。
2. **直接税** タブの **源泉徴収税** セクションで、**TDS の有効化** オプションを **はい** に設定して、TDS 機能とそれに使用されるページおよびフィールドを有効にします。
3. **請求書** オプションを **はい** に設定して、請求書レベルで TDS の計算および控除に使用されるフィールドを有効にします。
4. **支払** オプションを **はい** に設定して、支払レベルで TDS の計算および控除に使用されるフィールドを有効にします。

    [![直接税タブ。](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. **番号順序** タブで、**参照** フィールドが **源泉徴収税の支払** に設定されている行を検索します。 行の **番号順序コード** フィールドで、番号順序コードを選択します。 番号順序コードは、定期的な TDS 決済プロセスの伝票番号を生成するために使用されます。

    > [!NOTE]
    > 定期的な TDS 決済プロセスを実行するには、**税 \> 申告 \> 源泉徴収税 \> 源泉徴収税の支払** に移動します。

    [![番号順序タブ。](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. ページを閉じます。

---
title: 買掛金勘定および売掛金勘定の TDS パラメータの設定
description: このトピックでは、源泉徴収税 (TDS) 控除をサポートするために買掛金勘定と売掛金勘定のパラメータを設定する方法について説明します。
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
ms.openlocfilehash: d2cb434346dbbe5487522fe9f7110716c3a8c761
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725152"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>買掛金勘定および売掛金勘定の TDS パラメータの設定

[!include [banner](../includes/banner.md)]

このトピックでは、源泉徴収税 (TDS) 控除をサポートするために買掛金勘定と売掛金勘定のパラメータを設定する方法について説明します。

1. **税 \> 設定 \> パラメーター \> 売掛金勘定パラメーター** に移動します。
2. **更新** タブで **注文明細行の更新** を選択して **注文明細行の更新** ダイアログ ボックスを開きます。
3. **TDS グループ** セクションの **TDS グループの更新** フィールドで、TDS グループを明細行レベルで更新するために使用する方法を指定します。 この設定は、注文ヘッダーで TDS グループが更新される場合に使用されます。 次のオプションを使用できます。

    - **許可しない** – 注文ヘッダーで TDS グループが更新されても、注文明細行の TDS グループは更新されません。
    - **常時** – 注文ヘッダーで TDS グループが更新されると、注文明細行の TDS グループは自動的に更新されます。
    - **プロンプト** – ユーザーは、注文明細行の TDS グループを更新するように求めるメッセージを受信します。
4. **OK** を選択します。

    [![注文明細行のダイアログ ボックスを更新します。](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. **税 \> 設定 \> パラメーター \> 買掛金勘定パラメーター** に移動します。
6. **全般** タブの **配送情報に基づく分割** クイック タブで、**製品受領書** オプションを **はい** に設定して、異なる配送先住所および税勘定番号 (TAN) を持つ製品受領書を転記および分割します。 このオプションが **いいえ** に設定されている場合は、配送先住所と TAN が異なる購買梱包明細を転記できません。
7. **請求書** オプションを **はい** に設定し、異なる配送先住所と TAN を含む仕入請求書を転記および分割します。

    [![配送情報クイック タブに基づいて分割します。](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. ページを閉じます。

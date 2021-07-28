---
title: TDS 税タイプに対する源泉徴収税コードの設定
description: このトピックでは、源泉徴収税 (TDS) の税コードの設定方法について説明します。
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
ms.openlocfilehash: 57de382c6d363a6c1d87cf734e9aedb32d6009a9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349931"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>TDS 税タイプに対する源泉徴収税コードの設定

[!include [banner](../includes/banner.md)]

このトピックでは、源泉徴収税 (TDS) の税コードの設定方法について説明します。

1. **税 \> 間接税 \> 源泉徴収税 \> 源泉徴収税コード** に移動します。

    [![源泉徴収税コード ページ。](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. アクション ペインで、**新規** を選択して、 TDS の源泉徴収税コードを作成し、必要な詳細を入力します。
3. **一般** クイック タブの **税タイプ** フィールドで、**TDS** を選択して、税コードを TDS 税コードとして分類します。
4. **決済期間** フィールドで、TDS 税コードの TDS 決済プロセスを選択します。
5. **主要勘定** フィールドで、TDS 金額を転記する勘定科目を選択します。
6. **売掛金勘定** フィールドで、販売トランザクションで控除されるTDS金額の転記が必要な売掛金勘定を選択します。

    **発生元** フィールドは自動的に **総額の割合** に設定され、値を変更することはできません。

    > [!NOTE]
    > TDS 税タイプの税コードの発生元を **正味金額の割合** に設定することもできます。

7. **源泉徴収税コンポーネント** フィールドで、TDS 税コードの TDS 税コンポーネントを選択します。
8. アクション ペインで **値** を選択して、**源泉徴収税の値** ページを開きます。
9. **開始日** フィールドで、TDS 値の開始日を入力します。 **終了日** フィールドに終了日を入力します。

    > [!NOTE]
    > **最小制限**、**上限**、および **除外率** フィールドは、TDS 税タイプの税コードには使用できません。

10. **値** フィールドに、TDS 税コードの TDS の割合を入力します。
11. **源泉徴収税の値** ページを閉じて、**源泉徴収税コード** ページに戻ります。

    > [!NOTE]
    > **源泉徴収税コード** ページの **制限** ボタンは、TDS 税タイプの税コードには使用できません。

12. ページを閉じます。

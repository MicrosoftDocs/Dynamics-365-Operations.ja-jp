---
title: グローバル源泉徴収税の為替レート タイプと日付タイプの設定を有効にする
description: この記事では、源泉徴収税の為替レート タイプと日付タイプのグローバル設定を有効にする方法について説明します。
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9db9cf41381b8b4de7dffe1c755a7df805a003ea
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573227"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>グローバル源泉徴収税の為替レート タイプと日付タイプの設定を有効にする

[!include[banner](../includes/banner.md)]

この記事では、源泉徴収税の為替レート タイプと日付タイプのグローバル設定を有効にする方法について説明します。 源泉徴収税の通貨に対して、専用の為替レート タイプと為替レート算定日タイプを選択できるようになりました。 これらの選択により、支払トランザクションでの源泉徴収税額の計算に使用される外貨為替レートが源泉徴収税の通貨で決定されます。

この機能は、Microsoft Dynamics 365 Finance バージョン 10.0.29 以降で使用できます。

1. **税** \> **設定** \> **パラメーター** \> **一般会計パラメーター** の順に移動します。
2. **源泉徴収税** タブで、**高度な源泉徴収税通貨を有効にする** オプションを **はい** に設定します。
3. **為替レート タイプ** フィールド で、源泉徴収税の通貨の為替レート タイプを選択します。
4. **算定日タイプ** フィールド で、源泉徴収税の通貨為替レートを決定する算定日のタイプを選択します。

    - **支払期日** – 支払仕訳帳の転記日に基づいて為替レートを決定します。
    - **請求日** – 請求仕訳帳の請求日に基づいて為替レートを決定します。 伝票の請求日が空白の場合は、請求書の転記日付が使用されます。 
    - **ドキュメント日付**  – 支払仕訳帳のドキュメント日付に基づいて為替レートを決定します。 伝票のドキュメント日付が空白の場合は、支払期日が使用されます。

5. **保存** を選択します。

トランザクション通貨が、源泉徴収税コードで定義されている源泉徴収税通貨と異なる場合、源泉徴収税の通貨の金額はトランザクション通貨から前の設定に基づいて計算され、転記された源泉徴収税トランザクションに記録されます。

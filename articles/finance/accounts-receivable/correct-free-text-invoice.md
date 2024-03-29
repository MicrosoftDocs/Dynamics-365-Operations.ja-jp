---
title: 自由書式の請求書を訂正
description: この記事では、自由書式の請求書を転記後に修正し、修正済請求書として再発行する方法を説明します。
author: abruer
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3cc07a1f0ba444250eddcf892681e2ca63e9c1a
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780518"
---
# <a name="correct-a-free-text-invoice"></a>自由書式の請求書を訂正

[!include [banner](../includes/banner.md)]

この記事では、自由書式の請求書を転記後に修正し、修正済請求書として再発行する方法を説明します。

すでに転記された自由書式の請求書を修正するには: 
1. 転記済みの自由書式の請求書を開きます。 
2. **請求書** ページで、**キャンセル** を選択してから、**請求書の修正** を選択します。 
3. 理由コードを選択し、コメントを追加して、および新しい訂正請求書の日付を選択します。
4. 訂正請求書を変更して、転記できます。 

訂正請求書を転記すると、キャンセル請求書が元の請求金額と一致する貸方金額に対して作成されます。 したがって、元の請求書とキャンセル請求書の合計残高が 0 (ゼロ) になります。 キャンセル請求書が元の請求書に対して決済されます。 

訂正請求書を転記すると、3 つの請求書ができます。

-   **元の請求書** – 修正している情報を含む請求書。
-   **キャンセル請求書** – システム生成の貸方請求書。最後に修正された請求書をキャンセルするために作成されます。
-   **訂正請求書** – 修正された請求書情報を含む請求書。

2 つの方法でキャンセル請求書と訂正請求書を識別できます。

-   **すべての自由書式の請求書** ページには、**訂正** 列が含まれており、ここでキャンセル請求書か訂正請求書かを確認できます。
-   自由書式の請求書ヘッダーには、**キャンセル請求書 '\[請求書番号\]'** または **訂正請求書 '\[請求書番号\]'** のステータスが示されます。

> [!NOTE]
> この機能は、**自由書式の請求訂正** コンフィギュレーション キーが選択されている場合にのみ利用できます。 構成キーを有効にする方法の詳細については、[メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) の、設定キーの有効化 (または無効化) セクションを参照してください。 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

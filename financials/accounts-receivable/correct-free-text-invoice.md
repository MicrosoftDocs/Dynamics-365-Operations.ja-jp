---
title: "自由書式の請求書を訂正"
description: "この記事では、自由書式の請求書を転記後に修正し、修正済請求書として再発行する方法を説明します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: ab16c517abfd3fa2b59625fff04b7427ee3471bb
ms.lasthandoff: 03/31/2017


---

# <a name="correct-a-free-text-invoice"></a>自由書式の請求書を訂正

この記事では、自由書式の請求書を転記後に修正し、修正済請求書として再発行する方法を説明します。

既に転記された自由書式の請求書を修正するには、転記された自由書式の請求書を開きます。 [**請求**ページで**キャンセル**、[**請求書を修正します。**。 理由コードを選択し、コメントを追加して、および新しい訂正請求書の日付を選択します。 訂正請求書を変更して、転記できます。 

訂正請求書を転記すると、キャンセル請求書が元の請求金額と一致する貸方金額に対して作成されます。 したがって、元の請求書とキャンセル請求書の合計残高が 0 (ゼロ) になります。 キャンセル請求書が元の請求書に対して決済されます。 

訂正請求書を転記すると、3 つの請求書ができます。

-   **元の請求書** – 修正している情報を含む請求書。
-   **キャンセル請求書** – システム生成の貸方請求書。最後に修正された請求書をキャンセルするために作成されます。
-   **訂正請求書** – 修正された請求書情報を含む請求書。

2 つの方法でキャンセル請求書と訂正請求書を識別できます。

-   **すべての自由書式の請求書**ページには、[**訂正**] 列が含まれており、ここでキャンセル請求書か訂正請求書かを確認できます。
-   自由書式の請求書のヘッダーは**請求書のステータスを「\[請求書番号\]」取り消します**またはなく**修正された請求「\[請求書番号\]」**。

> [!NOTE]
> この機能は**自由書式の請求書の訂正**コンフィギュレーション キーが選択されている場合にのみ使用できます。



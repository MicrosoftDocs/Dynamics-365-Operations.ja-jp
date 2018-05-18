---
title: "注文保留"
description: "このトピックでは、Dynamics 365 for Retail を使用して、注文の保留について説明します。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8b4c8ecbef1dc667d3b60411a53f0c63686529c2
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="order-holds"></a>注文保留

[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 for Retail を使用して、注文の保留について説明します。

注文はさまざまな理由で保留にすることができます。 たとえば、顧客の住所や支払方法が確認できるまで、またはマネージャーが顧客の与信限度額を確認できるまで、注文を保留にすることがあります。 販売プロセスの間は、販売注文は保留中にすることが必要な場合があります。 たとえば、顧客の支払いに関する問題のために、または管理者の確認が必要なために、販売注文を保留中にすることが必要な場合があります。 販売注文を保留中にすると、保留の理由を示す注文保留コードが販売注文に割り当てられます。 **販売とマーケティング** &gt; **設定** &gt; **販売注文** &gt; **注文保留コード** で販売注文保留コードがコンフィギュレーションされます。 販売注文は注文の作成時に、または後で手動で保留にすることができます。 また、注文を不正ルールに基づいて、自動的に保留にすることができます。 販売注文が保留中の間、詳細情報に基いてそれを更新する必要がある場合があります。 または、販売注文をチェック アウトして作業を続行することもできます。 販売注文をチェックアウト、もう一度確認、および注文保留ワークベンチを使用して、別のユーザーのチェックアウトを上書きすることができます (**小売** &gt; **顧客** &gt; **注文保留**)。 注文を完了する準備が整ったら、注文プロセスを完了する前に、保留を解除する必要があります。





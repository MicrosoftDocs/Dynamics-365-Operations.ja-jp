---
title: "単位間会計のバランス仕訳帳"
description: "この記事は、差引勘定する財務分析コードを [元帳] ページで選択したときに仕訳帳がどのように自動的に差引勘定されるかを示します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0909b64a77024d551af0dad2de985887cf6ff06d
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a>単位間会計のバランス仕訳帳

[!include[banner](../includes/banner.md)]


この記事は、差引勘定する財務分析コードを [元帳] ページで選択したときに仕訳帳がどのように自動的に差引勘定されるかを示します。 

会計項目は財務分析コード値のレベルで収支を合わせないため、仕訳帳の収支を合わせるための追加の会計項目が自動的に作成されます。 これらの勘定項目は、**自動トランザクションの勘定**ページで**単位間 - 借方**と**単位間 - 貸方**を使用して主勘定を決定します。 たとえば、勘定科目の 2 番目の区分である [分岐] は、差引勘定する財務分析コードとして選択され、次の勘定項目が作成されます。

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 DR |
| 6100 – NY – OU\_249  | 100.00 DR |
| 2100 – MSP – OU\_256 | 200.00 CR |

この場合、次の残高が決定されます:

-   ブランチ MSP = 100.00 CR
-   ブランチ NY = 100.00 DR

したがって、次の勘定項目は、このエントリが財務分析コード値のレベルで仕訳帳を差引勘定するように自動的に作成されます。

|                                   |           |
|-----------------------------------|-----------|
| (単位間の借方) – MSP – OU\_256 | 100.00 DR |
| (単位間の借方) – NY – OU\_249 | 100.00 CR |






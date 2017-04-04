---
title: "interunitの会計の釣り合った仕訳帳"
description: "この記事は、差引勘定する財務分析コードを [元帳] ページで選択したときに仕訳帳がどのように自動的に差引勘定されるかを示します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 8b6fda79222905b0df211a0b944aca9e4dc76850
ms.lasthandoff: 03/31/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a>interunitの会計の釣り合った仕訳帳

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
|  (Interunitの借方) – MSP – OU\_256 | 100.00 DR |
|  (Interunitの貸方) – NY – OU\_249 | 100.00 CR |





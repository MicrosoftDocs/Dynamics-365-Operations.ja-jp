---
title: 単位間会計のバランス仕訳帳
description: この記事は、差引勘定する財務分析コードを [元帳] ページで選択したときに仕訳帳がどのように自動的に差引勘定されるかを示します。
author: kweekley
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38a7d88602dcd0121eb331dab8bf35a815287f8c
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712317"
---
# <a name="balanced-journals-for-interunit-accounting"></a>単位間会計のバランス仕訳帳

[!include [banner](../includes/banner.md)]

この記事は、差引勘定する財務分析コードを [元帳] ページで選択したときに仕訳帳がどのように自動的に差引勘定されるかを示します。 

会計項目は財務分析コード値のレベルで収支を合わせないため、仕訳帳の収支を合わせるための追加の会計項目が自動的に作成されます。 これらの勘定項目は、**自動トランザクションの勘定** ページで **単位間 - 借方** と **単位間 - 貸方** を使用して主勘定を決定します。 たとえば、勘定科目の 2 番目の区分である [事業単位] は、差引勘定する財務分析コードとして選択され、次の勘定項目が作成されます。

| &nbsp;               | &nbsp;    |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 DR |
| 6100 – NY – OU\_249  | 100.00 DR |
| 2100 – MSP – OU\_256 | 200.00 CR |

この場合、次の残高が決定されます:

-   事業単位MSP = 100.00 CR
-   事業単位NY = 100.00 DR

したがって、次の勘定項目は、このエントリが財務分析コード値のレベルで仕訳帳を差引勘定するように自動的に作成されます。

| &nbsp;                            | &nbsp;    |
|-----------------------------------|-----------|
| (単位間の借方) – MSP – OU\_256 | 100.00 DR |
| (単位間の借方) – NY – OU\_249 | 100.00 CR |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: 経費精算書での個人経費
description: このトピックでは、作業者の個人経費を Microsoft Dynamics 365 for Finance and Operations で処理するための 2 つの方法を説明します。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b072fa9e78563d3e89b4d60e9ce61473902fee76
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794995"
---
# <a name="personal-expenses-on-an-expense-report"></a>経費精算書での個人経費

[!include [banner](../includes/banner.md)]

出張中に、作業者は、会社のクレジット カードで個人経費を支払う場合があります。 個人経費を取扱うプロセスを定義していない場合は、作業員が経費明細精算書を提出すると、経費精算書承認プロセスが混乱する可能性があります。 

Microsoft Dynamics 365 for Finance and Operations では、作業者の個人経費を処理する 2 つの方法があります。

- **従業員による支払** – 組織は、会社のクレジット カードの請求に表示される個人経費を支払いません。 代わりに、会社のクレジット カードに請求された会社経費と共に個人経費を表示するレポートを作成します。
- **会社による支払** – 組織は、法人のクレジット カードの請求を全額支払った後に、個人経費を作業者の勘定の借方に転記します。

**経費管理パラメーター**ページで組織が使用する方法を選択できます。

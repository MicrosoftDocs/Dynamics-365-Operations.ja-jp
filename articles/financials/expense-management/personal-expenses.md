---
title: "経費精算書での個人経費"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations で作業者の個人経費を取扱う 2 通りの方法について説明します。"
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 27698b02795b709a167235537d8b1ca871bdd371
ms.contentlocale: ja-jp
ms.lasthandoff: 03/13/2018

---

# <a name="personal-expenses-on-an-expense-report"></a>経費精算書での個人経費

[!include [banner](../includes/banner.md)]

出張中に、作業者は、会社のクレジット カードで個人経費を支払う場合があります。 個人経費を取扱うプロセスを定義していない場合は、作業員が経費明細精算書を提出すると、経費精算書承認プロセスが混乱する可能性があります。 

Microsoft Dynamics 365 for Finance and Operations では、作業者の個人経費を取扱う 2 通りの方法があります。

- **従業員による支払** – 組織は、会社のクレジット カードの請求に表示される個人経費を支払いません。 代わりに、会社のクレジット カードに請求された会社経費と共に個人経費を表示するレポートを作成します。
- **会社による支払** – 組織は、法人のクレジット カードの請求を全額支払った後に、個人経費を作業者の勘定の借方に転記します。

[経費管理パラメーター] ページで組織が使用する方法を選択できます。


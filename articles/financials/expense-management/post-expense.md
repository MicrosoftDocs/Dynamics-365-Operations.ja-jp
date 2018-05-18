---
title: "経費精算書の転記"
description: "このトピックでは、一般会計への経費精算書を転記する方法について説明します。"
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: cc3aae061038202ec4f314654d9149c31e2575bb
ms.contentlocale: ja-jp
ms.lasthandoff: 03/13/2018

---

# <a name="post-an-expense-report"></a>経費精算書の転記

[!include [banner](../includes/banner.md)]

経費精算書は、承認されて一般仕訳帳に転送された後、一般会計に転記できます。 経費精算書を転記すると、付加価値税 (VAT) の還付に適用できる経費が特定されます。 VAT の支払の確認および還付タスクは、経費精算書の確認を担当する従業員に割り当てられます。

経費精算書の経費が従業員の採用会社以外の会社に請求される場合は、経費の支払先会社と経費の支払元会社を確認する必要があります。 たとえば、経費精算書を送信した従業員は DAT 社に勤務しているが、DIR 社への経費を請求されたとします。 この場合、DAT は経費の支払先会社、DIR は経費の支払元会社です。 これらの仕訳帳明細行を確認した後は、経費明細行を一般会計に転記できます。

経費精算書を転記するには、[承認された経費精算書] ページで経費精算書を選択し、アクション ウィンドウで [転記] を選択します。

同時にリストですべての経費精算書を転記することもできます。 すべての経費精算書を選択し、[転記] を選択します。


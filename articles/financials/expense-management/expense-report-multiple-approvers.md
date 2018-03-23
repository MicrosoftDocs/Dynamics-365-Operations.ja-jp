---
title: "経費精算書と複数の承認者"
description: "このトピックでは、2 人以上の承認を必要とする経費精算書に関する情報を提供します。"
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 0f7592c580a21040c8b630885939ceaab3855c2c
ms.contentlocale: ja-jp
ms.lasthandoff: 03/13/2018

---

# <a name="expense-reports-and-multiple-approvers"></a>経費精算書と複数の承認者

[!include[banner](../includes/banner.md)]

組織の経費の承認ポリシーに応じて、従業員が提出した経費レポートの承認を複数の人が行う必要がある場合があります。 経費レポートの承認のワークフロー プロセスを設定する場合、経費レポートの承認者のタスクまたはステップを一つ以上含むワークフロー要素を追加できます。 たとえば、すべての経費レポートは、まず最初に精算書を提出した従業員の管理者、そして買掛金勘定コーディネーターにより承認されることが要求される場合があります。

複数の経費レポートの承認者を要求するようにした場合、次の方法のいずれかでワークフロー要素を追加できます:

- 1 つのステップを有する 1 件の承認の要素を追加します。 たとえば、ステップでは経費精算書をユーザー グループに割り当て、ユーザー グループのメンバーの 50 パーセントで承認される必要がある場合があります。
- 複数のステップを有する 1 件の承認の要素を追加します。 たとえば、承認要素は次のステップを有する場合があります。

    1. 経費レポートを提出した従業員の管理者がそれを承認します。
    2. 買掛金勘定の事務員は、受領および経費レポートの項目を確認します。
    3. 予算の所有者が経費レポートを承認します。

- 複数の承認要素を追加します。それぞれの要素には 1 つのステップがあります。 たとえば、次の手順の個別の承認要素を追加できます。

    1. 従業員の管理者が経費レポートを承認します。
    2. 予算の所有者が経費レポートを承認します。


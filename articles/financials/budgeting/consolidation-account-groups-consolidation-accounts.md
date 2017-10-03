---
title: "連結勘定グループおよび追加連結勘定"
description: "このトピックでは、連結勘定グループおよび追加連結勘定に関する情報、および Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition での使用方法を説明します。"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 3c08e48b22f964c3f643c5ddc4ecd687502d7fda
ms.contentlocale: ja-jp
ms.lasthandoff: 08/01/2017

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>連結勘定グループおよび追加連結勘定

[!include[banner](../includes/banner.md)]


このトピックでは、連結勘定グループおよび追加連結勘定に関する情報、および Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition での使用方法を説明します。

<a name="consolidation-account-groups"></a>連結勘定グループ
----------------------------

連結勘定グループで、データを連結するのに使用する勘定のグループを作成することができます。 連結勘定グループは通常、政府指定の勘定科目表を表すか、会社の本社によって定義されるグループにアカウントをマップします。 [**連結**] モジュールの [**設定**] 領域で連結勘定グループを検索できます。 新しいグループを追加するときに、勘定グループと名前の固有 ID を入力します。

## <a name="additional-consolidation-accounts"></a>追加連結勘定
連結統合で、既存の勘定科目表から連結勘定グループに勘定を割り当てることができます。 その後、連結勘定の値と名前を指定できます。 

[**連結**] モジュールの [**設定**] 領域で追加の連結勘定を検索できます。 新しい連結勘定を作成するときに、次の情報を指定する必要があります。

-   **主勘定** – このフィールドは、このページで選択した勘定科目表に基づいているすべての主勘定を示すルックアップです。 アカウントを選択すると、名前が [**主勘定名**] フィールドに自動的に入力されます。
-   **連結勘定グループ** – このフィールドを使用して、勘定を割り当てるグループを指定します。 2 つの異なる方法で連結する場合、4 つすべての連結勘定グループに同じ勘定を追加する必要があります。
-   **連結勘定** – 連結勘定の値を入力します。 この値は、勘定科目表の勘定である必要はありません。 必要とするどの値でも可能です。
-   **連結勘定名** – 照会およびレポートに表示させる勘定の名前を入力します。
-   **SAT レベル** – このフィールドは、メキシコの税務当局に取引明細書をレポートするのに使用されます。 

連結勘定グループおよび追加の連結勘定の作成を終了すると、[オンラインで連結] プロセスでこのグループを選択できます。


詳細については、[連結グループおよび追加の連結勘定の作成](../general-ledger/tasks/create-consolidation-groups.md)を参照してください。 





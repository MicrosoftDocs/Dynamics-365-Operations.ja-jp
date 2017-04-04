---
title: "連結の勘定グループ、および追加統合の勘定"
description: "このトピックでは、連結の勘定グループ、および追加統合の勘定に関する情報を提供し、それらの工程にMicrosoft Dynamics 365 for Operationsで使用方法を説明します。"
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f9c5aaa389c9c2f85d1ab91cbf3d2222cbebef55
ms.lasthandoff: 03/31/2017


---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>連結の勘定グループ、および追加統合の勘定

このトピックでは、連結の勘定グループ、および追加統合の勘定に関する情報を提供し、それらの工程にMicrosoft Dynamics 365 for Operationsで使用方法を説明します。

<a name="consolidation-account-groups"></a>連結勘定グループ
----------------------------

連結の勘定グループは、データを連結するのに使用する勘定のグループを作成することができます。 最もよく統合の勘定グループは、必須指定された勘定科目表を表しますまたはマップは、会社の本部によって定義されたグループに説明します。 **統合**モジュールの**設定**領域で連結の勘定グループを検索できます。 新しいグループを追加するときに、勘定グループと名前の固有IDを入力します。

## <a name="additional-consolidation-accounts"></a>追加連結勘定
追加統合の勘定は既存の勘定科目表の統合の勘定グループに勘定を割り当てるようにします。 その後、統合の勘定の金額と名前を指定できます。 

**統合**モジュールの**設定**領域で追加統合の勘定を検索できます。 新しい連結のアカウントを作成すると、次の情報を指定する必要があります:

-   **主要な勘定の– **このフィールドは、ここで選択した勘定科目表に基づいているすべての主要な勘定を示す参照です。 アカウントを選択すると、名前は**主要な勘定科目名**フィールドに自動的に入力されます。
-   **統合の勘定グループ**勘定に割り当てるグループを指定する–このフィールドを使用します。 二つの異なる方法で連結すると、すべての4人の統合の勘定グループに同じ勘定を追加する必要があります。
-   **統合の勘定– **は統合の勘定の値を入力します。 この値は、勘定科目表の勘定になくては限りません。 必要なのは、値です。
-   **統合の勘定科目名**、照会やレポートに表示するように–は、勘定の名前を入力します。
-   ** SATのレベル メキシコ税務当局に取引明細書を報告するのに**このフィールド–が使用されます。 

連結の勘定グループの作成が完了したら、追加の統合を表す、連結のオンライン処理のグループを選択できます。




--- 
title: "クロス ドッキングおよび集中的購買のルールとパラメーターの設定"
description: "この手順では、補充ルールを作成するための手順を示します。"
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: f3a20b7bf476cae854c7f7c86d89d73e44b6749b
ms.contentlocale: ja-jp
ms.lasthandoff: 02/07/2018

---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a>クロス ドッキングおよび集中的購買のルールとパラメーターの設定

[!include[task guide banner](../includes/task-guide-banner.md)]

この手順では、補充ルールを作成するための手順を示します。 クロスドッキングと集中的購買を実行するときに、補充ルールを製品の店舗への配分を管理するために使用できます。 補充ルールは、店舗または店舗グループに対して設定できます。 ルールの行ごとに定義された重量によって、補充ルールをクロスドッキングまたは集中的購買で配分方法として使用する場合に、店舗間で配分される製品の数量が制御されます。 この手順では、USMF というデモ会社を使用します。

1. [補充ルール] に移動します。
2. [新規] をクリックします。
3. [補充ルール] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [保存] をクリックします。
6. [追加] をクリックします。
7. 一覧で、選択された行をマークします。
    * 補充階層またはタイプのチャンネルを選択できます。 この値によって、名前で選択した内容がチャンネルの階層または特定のチャンネルであるかが管理されます。  この例では、補充階層として設定を保持します。  
8. [名前] フィールドで値を選択します。
    * 既定の重量の値は、倉庫で定義された重量から入力されます。  この重量を補充ルールで使用できます。また、[重量] フィールドに新しい重量を入力できます。  
9. [重量] フィールドに数値を入力します。
10. [追加] をクリックします。
11. 一覧で、選択された行をマークします。
12. [タイプ] フィールドで [チャンネル] を選択します。
13. [名前] フィールドで値を入力または選択します。
14. [重量] フィールドに数値を入力します。
15. [保存] をクリックします。



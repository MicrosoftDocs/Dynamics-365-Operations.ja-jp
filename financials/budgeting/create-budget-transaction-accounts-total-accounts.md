---
title: "トランザクション勘定と合計勘定からの予算作成"
description: "この記事は、勘定合計に基づいて予算を作成するプロセスの概要を提供します。 予算管理が必要な場合に、勘定合計の予算管理を有効にする方法を説明します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: af9b6a5ebb25c0054704b60c84057eee609ffab7
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>トランザクション勘定と合計勘定からの予算作成

この記事は、勘定合計に基づいて予算を作成するプロセスの概要を提供します。 予算管理が必要な場合に、勘定合計の予算管理を有効にする方法を説明します。

予算計画および予算登録エントリの文書の両方が、**合計**タイプの主勘定を持つ主勘定での予算作成に使用できます。 実績は、トランザクション用の主勘定にのみ転記できます。 

**一般会計から予算計画を生成**の定期プロセスについて、**ソース** タブで、**合計**の主勘定タイプを基準として指定できます。 この場合、各合計の主勘定がターゲット予算計画に含まれ、金額は選択範囲の主勘定の合計金額と一致します。 

**合計**タイプの主勘定の予算管理を有効にできます。 この機能は、予算グループの使用でサポートされます。 個々の合計主要なアカウントには、予算のグループに対して制御される予算は**予算管理コンフィギュレーション**ページで作成する必要があります。 指定した基準は、主要な勘定および勘定範囲を設定する必要があります。 予算グループの作成プロセスの処理速度を上げるために、予算管理グループのデータ エンティティを使用できます。 

予算を財務諸表などのレポートで使用する場合、合計勘定の予算合計は、次の金額で構成されます。

-   勘定合計の期間内に各トランザクション勘定科目から作成される予算
-   勘定合計に直接入力された予算金額

これにより、勘定合計の期間内の最重要トランザクション勘定に個別の予算を作成することも、利用可能な予算額を勘定合計に追加することもできます。



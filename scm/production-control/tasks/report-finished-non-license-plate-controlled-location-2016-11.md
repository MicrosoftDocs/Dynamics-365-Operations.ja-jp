--- 
title: "プレートにより制御されている場所への完了レポート"
description: "このタスク ガイドでは、ライセンス プレートにより制御されていない場所への完了報告時の例を示します。"
author: ChristianRytt
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 9b861d8499db2b7ba362664e271bedda1d392a23
ms.contentlocale: ja-jp
ms.lasthandoff: 07/28/2017

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a>プレートにより制御されている場所への完了レポート 

[!include[task guide banner](../../includes/task-guide-banner.md)]

このタスク ガイドでは、ライセンス プレートにより制御されていない場所への完了報告時の例を示します。 適用できる作業ポリシーは、このタスクの前提条件です。 前のタスク ガイドでは、作業ポリシーの設定を示しました。 このタスク ガイドでは、Dynamics AX アプリケーション 7.0.1 以降が必要です。




## <a name="set-up-an-output-location"></a>出荷場所の設定
1. [組織管理] > [リソース] > [リソース グループ] の順に移動します。
2. 一覧で、リソース グループ「5102」を選択します。
3. [編集] をクリックします。
4. [出荷倉庫] フィールドに、「51」を入力します。
5. [出荷場所] フィールドに、「001」を入力します。
    * 場所 001 はライセンス プレートにより制御される場所ではありません。 場所に適用できる作業ポリシーが存在する場合にのみ、ライセンス プレートのない出荷場所を設定できます。  

## <a name="create-a-production-order-and-report-it-as-finished"></a>製造オーダーを作成して完了として報告
1. ページを閉じます。
2. [生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。
3. [新しい製造オーダー] をクリックします。
4. [品目番号] フィールドに、「L0101」を入力します。
5. [作成] をクリックします。
6. アクション ペインで、[製造オーダー] をクリックします。
7. [見積] をクリックします。
8. [OK] をクリックします。
9. [開始] をクリックします。
10. [一般] タブをクリックします。
11. [自動 BOM 消費] フィールドで、「なし」を選択します。
12. [OK] をクリックします。
13. ［完了レポート] をクリックします。
14. [一般] タブをクリックします。
15. [エラー適用] フィールドで、[はい] を選択します。
16. [OK] をクリックします。
17. アクション ペインで [倉庫] をクリックします。
18. [作業の詳細] をクリックします。
    * 製造オーダーが完了と報告されたときに、作業はプット アウェイに生成されませんでした。 これは、製品 L0101 が場所 001 に完了として報告されるときに作業が生成されないように作業ポリシーを定義しているために発生します。  



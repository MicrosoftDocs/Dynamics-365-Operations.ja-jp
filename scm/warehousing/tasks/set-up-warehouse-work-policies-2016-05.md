--- 
title: "倉庫作業ポリシーの設定"
description: "倉庫のプロセスは倉庫作業を常に含みません。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 5db1c99833276a92467ed57b7be51b0ebaa74d83
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-warehouse-work-policies"></a>倉庫作業ポリシーの設定 

[!include[task guide banner](../../includes/task-guide-banner.md)]

倉庫のプロセスは倉庫作業を常に含みません。 作業ポリシーを定義して、原材料のピッキングの作業の作成、および特定の場所での一連の製品に対する完成品のプット アウェイを防ぐことができます。 デモ データの会社 USMF がこの記録の作成に使用されました。 このタスク ガイドでは、Dynamics AX アプリケーション 7.0.1 以降が必要です。

1. [倉庫管理] > [設定] > [作業] > [作業ポリシー] の順に移動します。
2. [新規] をクリックします。
3. [作業ポリシー名] フィールドに、「プット アウェイ作業なし」と入力します。
4. [保存] をクリックします。
5. [追加] をクリックします。
6. 一覧で、選択された行をマークします。
7. [ワーク オーダー タイプ] フィールドで、[完成品のプット アウェイ] を選択します。
8. [追加] をクリックします。
9. 一覧で、選択された行をマークします。
10. [ワーク オーダー タイプ] フィールドで、[連産物と副産物のプット アウェイ] を選択します。
11. [在庫場所] セクションを展開します。
12. [追加] をクリックします。
13. 一覧で、選択された行をマークします。
14. 倉庫の一覧で、「51」を入力します。
15. [場所] フィールドで「001」を入力または選択します。
16. [製品] セクションを展開します。
17. [製品の選択] フィールドで、[選択済] を選択します。
18. [追加] をクリックします。
19. 一覧で、選択された行をマークします。
20. [品目番号] フィールドで、「L0101」を入力または選択します。
21. [保存] をクリックします。



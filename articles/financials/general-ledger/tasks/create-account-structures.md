---
title: 勘定構造の作成
description: このタスク ガイドでは、勘定構造の作成について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2183f88356fc8094781af147bf079c4e53ffb2b4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846706"
---
# <a name="create-account-structures"></a>勘定構造の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスク ガイドでは、勘定構造の作成について説明します。 手順は、デモ データの会社 USMF を使用します。

1. [総勘定元帳] > [勘定科目表] > [構造] > [勘定構造のコンフィギュレーション] に移動します。
2. [新規] をクリックすると、ドロップ ダイアログが開きます。
3. [勘定構造] フィールドで、勘定構造の目的を説明する名前を入力します。
4. [説明] フィールドで、勘定構造の目的を指定するための説明を入力します。
5. [作成] をクリックします。
6. [区分の追加] をクリックします。
7. [分析コード リスト] で、勘定構造に追加する分析コードを選択します。
8. [区分の追加] をクリックします。
9. [区分の追加] をクリックします。
10. [分析コード リスト] で、勘定構造に追加する分析コードを選択します。
11. [区分の追加] をクリックします。
12. [区分の追加] をクリックします。
13. [分析コード リスト] で、勘定構造に追加する分析コードを選択します。
14. [区分の追加] をクリックします。
15. グリッドで、許可された値を編集する区分を選択します。
    * たとえば、[主勘定] をクリックします。  
16. [演算子] フィールドで、「is between」や「includes」などのオプションを選択します。
17. [値] フィールドに値を入力します。
    * たとえば、600000 です。  
18. [終了日] フィールドに値を入力します。
    * たとえば、699999 です。  
19. [適用] をクリックします。
20. グリッドで、許可された値を編集する区分を選択します。
    * 例えば [部門] です。  
21. [演算子] フィールドで、「is between」や「includes」などのオプションを選択します。
22. [値] フィールドに値を入力します。
    * 例えば 022 です。  
23. [終了日] フィールドに値を入力します。
    * たとえば、031 です。  
24. [新しい基準の追加] をクリックします。
25. [演算子] フィールドで、「is between」や「includes」などのオプションを選択します。
26. [値] フィールドに値を入力します。
    * たとえば、033 です。  
27. [終了日] フィールドに値を入力します。
    * たとえば、034 です。  
28. [適用] をクリックします。
29. グリッドで、許可された値を編集する区分を選択します。
    * たとえば、[減価部門] です。  
30. [減価部門] フィールドに値を入力します。
    * たとえば、007..021 です。  
31. [追加] をクリックします。
32. [主勘定] フィールドに値を入力します。
    * たとえば、600000..699999  
33. グリッドで、許可された値を編集する区分を選択します。
    * 例えば [部門] です。  
34. [部門] フィールドに値を入力します。
    * たとえば、032 です。  
35. [減価部門] フィールドに値を入力します。
    * たとえば、086 です。  
36. [検証] をクリックします。
37. [有効化] をクリックします。
38. [有効化] をクリックします。


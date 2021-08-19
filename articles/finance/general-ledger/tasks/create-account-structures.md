---
title: 勘定構造の作成
description: このタスク ガイドでは、勘定構造の作成について説明します。
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93cc2e9ceb15070491bb3d0a790367e6d5bf8c4a30cd7efa690fd825963165b6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779544"
---
# <a name="create-account-structures"></a>勘定構造の作成

[!include [banner](../../includes/banner.md)]

このタスク ガイドでは、勘定構造の作成について説明します。 手順は、デモ データの会社 USMF を使用します。

1. **ナビゲーション ウィンドウ > モジュール > 一般会計 > 勘定科目表 > 構造 > 勘定構造の構成** の順に移動します。
2. **アクション ウィンドウ** で、**新規** をクリックすると、ドロップ ダイアログが開きます。
3. **勘定構造** フィールドで、勘定構造の目的を説明する名前を入力します。
4. **説明** フィールドで、勘定構造の目的を指定するための説明を入力します。
5. **作成** をクリックします。
6. **区分および許可された値** で、**区分の追加** をクリックします。
7. 分析コード リストで、勘定構造に追加する分析コードを選択します。
8. リストの最後で、**区分の追加** をクリックします。
9. 必要に応じて、手順 6 ～ 9 を繰り返します。
10. **許可された値の情報** セクションで、許可された値を編集する区分を選択します。
    たとえば、**主勘定** フィールドをクリックします。  
11. **演算子** フィールドで、is between や includes などのオプションを選択します。
12. **値** フィールドに値を入力します。 たとえば、600000 です。  
13. **終了日** フィールドに値を入力します。 たとえば、699999 です。  
14. **許可された値の情報** セクションで、**適用** をクリックします。
15. 必要に応じて、手順 10 ～ 15 を繰り返します。  
16. **許可された値の情報** セクションで、**新しい基準の追加** をクリックします。
17. [演算子] フィールドで、「is between」や「includes」などのオプションを選択します。
18. **値** フィールドに値を入力します。 たとえば、033 です。  
19. **終了日** フィールドに値を入力します。 たとえば、034 です。  
20. **適用** をクリックします。
21. グリッドで、許可された値を編集する区分を選択します。 たとえば、[減価部門] です。  
22. **CostCenter フィールド** に値を入力します。 たとえば、007..021 です。  
23. **区分および許可された値** で、**追加** をクリックします。
24. **主勘定** フィールドに値を入力します。 たとえば、600000..699999  
25. グリッドで、許可された値を編集する区分を選択します。 例えば [部門] です。  
26. [部門] フィールドに値を入力します。 たとえば、032 です。  
27. [減価部門] フィールドに値を入力します。 たとえば、086 です。  
28. **アクション ウィンドウ** で、**検証** をクリックします。
29. **アクション ウィンドウ** で、**有効化** をクリックします。
30. **有効化** をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
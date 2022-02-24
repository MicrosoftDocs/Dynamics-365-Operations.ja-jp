---
title: 詳細ルール構造の作成と割り当て
description: このトピックでは、詳細なルール構造を作成して勘定構造に割り当てる方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6a3f7d174c91e357dce8a19ab50a5cd42a85561
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968607"
---
# <a name="create-and-assign-advanced-rule-structures"></a>詳細ルール構造の作成と割り当て

[!include [banner](../../includes/banner.md)]

このトピックでは、詳細なルール構造を作成して勘定構造に割り当てる方法について説明します。 このガイドでは、USMF デモ会社を使用します。

## <a name="create-an-advanced-rule-structure"></a>詳細なルール構造の作成
1. **ナビゲーション ウィンドウ > モジュール > 一般会計 > 勘定科目表 > 構造 > 詳細なルール構造** の順に移動します。
2. **新規** を選択すると、ドロップ ダイアログが開きます。
3. **詳細なルール構造** フィールドにルール構造を説明する名前を入力します。
4. **OK** を選択します。
5. **区分の追加** を選択します。
6. 区分リストで、財務分析コードを選択します。 たとえば **店舗** です。  
7. **区分の追加** を選択します。
8. **有効化** を選択します。

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>詳細ルール構造の勘定構造への適用
1. **ナビゲーション ウィンドウ > モジュール > 一般会計 > 勘定科目表 > 構造 > 勘定構造の構成** の順に移動します。
2. 一覧で、詳細ルールを適用する勘定構造を検索し選択します。
3. **編集** を選択します。 **詳細ルール** を選択すると、勘定構造を **ドラフト モード** に設定するよう要求されます。  
4. **詳細ルール** を選択します。
5. **新規** を選択すると、ドロップ ダイアログが開きます。
6. **詳細ルール** フィールドに値を入力します。
7. **名前** フィールドに値を入力します。
8. **作成** を選択します。
9. **新しい基準の追加** を選択します。
10. **適用箇所** フィールドで、主勘定または財務分析コードを選択します。
11. **演算子** フィールドで、**is between** や **includes** などのオプションを選択します。
12. **値** フィールドに値を入力します。
13. **終了日** フィールドに値を入力します。
14. **追加** を選択してドロップ ダイアログを開きます。
15. 一覧で、入力した基準と一致した場合に使用する詳細ルール構造を検索します。
16. **追加** を選択します。
17. ページを閉じます。
18. **有効化** を選択します。


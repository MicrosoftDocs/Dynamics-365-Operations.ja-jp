---
title: 会社間プロジェクト請求のコンフィギュレーション
description: この手順では、組織内の 2 つの会社間のプロジェクト請求の設定方法を示します。
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fe06978d3a1c41a1133a568cca61df05b49d235
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "352761"
---
# <a name="configure-intercompany-project-invoicing"></a>会社間プロジェクト請求のコンフィギュレーション

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、組織内の 2 つの会社間のプロジェクト請求の設定方法を示します。 このタスクでは、USSI データ セットを使用します。

1. [買掛金勘定] > [仕入先] > [すべての仕入先] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. アクション ウィンドウで、[一般] をクリックします。
4. [会社間] をクリックします。
5. 会社間取引を有効にするには、[アクティブ] に [はい] を設定します。
6. [顧客の会社] フィールドで、値を入力または選択します。
7. [自社会社コード] フィールドで、値を入力または選択します。
8. [保存] をクリックします。
9. ページを閉じます。
10. ページを閉じます。
11. [プロジェクト管理および会計] > [設定] > [プロジェクト管理および会計パラメーター] の順に移動します。
12. [会社間] タブをクリックします。
13. スライダーを [はい] まで動かして、会社間リソース スケジューリングとタイムシートを有効にします。
14. 一覧で、選択された行をマークします。
15. [新規] をクリックします。
16. 一覧で、選択された行をマークします。
17. [借入側の法人] フィールドで、値を入力または選択します。
18. [未収収益] チェック ボックスをオンにします。
19. [既定のタイムシート カテゴリ] フィールドで、値を入力または選択します。
20. [既定の経費カテゴリ] フィールドで、値を入力または選択します。
21. [保存] をクリックします。
22. ページを閉じます。
23. [プロジェクト管理および会計] > [設定] > [転記] > [元帳転記の設定] の順に移動します。
24. [勘定タイプ] フィールドでオプションを選択します。
25. [新規] をクリックします。
26. 一覧で、選択された行をマークします。
27. 一覧で、選択された行をマークします。
28. [主勘定] フィールドに、目的の値を指定します。
29. [保存] をクリックします。
30. ページを閉じます。
31. [プロジェクト管理および会計] > [設定] > [価格] > [移転価格] の順にクリックします。
32. [新規] をクリックします。
33. [有効日] フィールドに日付を入力します。
34. [借入側の法人] フィールドで、値を入力または選択します。
35. [移転価格モデル] フィールドで、オプションを選択します。
36. [価格決定] フィールドに、数を入力します。
37. [保存] をクリックします。


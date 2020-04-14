---
title: 会社間プロジェクト請求のコンフィギュレーション
description: このトピックでは、組織内の 2 つの会社間のプロジェクト請求の設定方法を示します。
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144282"
---
# <a name="configure-intercompany-project-invoicing"></a>会社間プロジェクト請求のコンフィギュレーション

[!include [banner](../../includes/banner.md)]

このトピックでは、組織内の 2 つの会社間のプロジェクト請求の設定方法を示します。 このタスクでは、USSI データ セットを使用します。

1. ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 仕入先 > すべての仕入先**の順に移動します。
2. **すべての仕入先**一覧で、目的のレコードを検索し、選択します。
3. アクション ウィンドウで、**一般**を選択します。
4. **会社間**を選択します。
5. 会社間取引を有効にするには、**アクティブ**を**はい**に設定します。
6. **顧客の会社**フィールドで、値を入力または選択します。
7. **自社会社コード** フィールドで、値を入力または選択します。
8. **保存** を選択します。
9. ページを閉じて、ホーム ページに戻ります。
10. ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > プロジェクト管理および会計パラメーター**の順に移動します。
11. **会社間**タブを選択します。
12. スライダーを**はい**まで動かして、会社間リソース スケジューリングとタイムシートを有効にします。
13. 一覧で、選択された行をマークします。
14. **新規** を選択します。
15. **借入側の法人**フィールドで、値を入力または選択します。
16. **未収収益**チェック ボックスをオンにします。
17. **既定のタイムシート カテゴリ** フィールドで、値を入力または選択します。
18. **既定の経費カテゴリ** フィールドで、値を入力または選択します。
19. **保存** を選択します。
20. ページを閉じます。
21. ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 転記 > 元帳転記の設定**の順に移動します。
22. **勘定タイプ** フィールドでオプションを選択します。
23. **新規** を選択します。
24. 新しい行の**主勘定**フィールドに、目的の値を指定します。
25. **保存** を選択します。
26. ページを閉じます。
27. ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 価格 > 移転価格**の順に移動します。
28. **新規** を選択します。
29. **有効日**フィールドに日付を入力します。
30. **借入側の法人**フィールドで、値を入力または選択します。
31. **移転価格モデル** フィールドで、オプションを選択します。
32. **価格決定**フィールドに、数を入力します。
33. **保存** を選択します。


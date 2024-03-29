---
title: 会社間財務データ共有のコンフィギュレーション
description: この手順では、会社間でデータを共有するときに、コンフィギュレーション、有効化、検証、および競合を解決する方法を示します。
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2caaa971790c31ed4c88bd0b2365179fb22b644e3d4512f4f06bb33bd29f8d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736281"
---
# <a name="configure-financial-cross-company-data-sharing"></a>会社間財務データ共有のコンフィギュレーション

[!include [banner](../../includes/banner.md)]

この手順では、会社間でデータを共有するときに、コンフィギュレーション、有効化、検証、および競合を解決する方法を示します。 これは、USMF 社と財務データ共有テンプレートを使用します。

このタスク ガイドでは、Dynamics AX platform 7.1 以降が必要です。

1. **ナビゲーション ウィンドウ > モジュール > システム管理 > ワークスペース > データ管理** の順に移動します。
2. **インポート** をクリックします。
3. **名前** フィールドに値を入力します。
4. **ソース データ形式** フィールドで、「パッケージ」タイプを選択します。 **アップロード** をクリックします。 財務データ共有テンプレート パッケージ ファイルの場所に移動し、そのファイルを選択します。
5. **保存** をクリックします。
6. 一覧で、選択された行をマークします。 作成したデータ共有ポリシーを選択します。  
7. **インポート** をクリックします。
8. **閉じる** をクリックします。
9. ページを更新します。
10. ページを閉じます。
11. ページを閉じます。
12. ページを閉じます。
13. **ナビゲーション ウィンドウ > モジュール > システム管理 > セットアップ > 会社間データ共有のコンフィギュレーション** の順に移動します。
14. 一覧で **支払期日** を検索して、選択します。
15. **追加** をクリックします。
16. 一覧で、選択された行をマークします。
17. **会社** フィールドで、「USSI」と入力します。
18. **追加** をクリックします。
19. **会社** フィールドで、「USMF」と入力します。
20. **保存** をクリックします。
21. **有効化** をクリックします。
22. **はい** をクリックします。
23. **共有の問題を検索する** をクリックします。
24. **はい** をクリックします。
25. **フィールド値の更新** をクリックします。
26. **会社 1 の値を使用** をクリックします。
27. ページを更新します。
28. ページを閉じます。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
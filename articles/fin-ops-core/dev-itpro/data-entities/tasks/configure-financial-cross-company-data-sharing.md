---
title: 会社間財務データ共有のコンフィギュレーション
description: この手順では、会社間でデータを共有するときに、コンフィギュレーション、有効化、検証、および競合を解決する方法を示します。
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc368351641f3e2432dfdbbaf8eed8694595bd4e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184373"
---
# <a name="configure-financial-cross-company-data-sharing"></a>会社間財務データ共有のコンフィギュレーション

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、会社間でデータを共有するときに、コンフィギュレーション、有効化、検証、および競合を解決する方法を示します。 これは、USMF 社と財務データ共有テンプレートを使用します。

このタスク ガイドでは、Dynamics AX platform 7.1 以降が必要です。

1. **ナビゲーション ウィンドウ > モジュール > システム管理 > ワークスペース > データ管理**の順に移動します。
2. **インポート**をクリックします。
3. **名前**フィールドに値を入力します。
4. **ソース データ形式**フィールドで、「パッケージ」タイプを選択します。 **アップロード** をクリックします。 財務データ共有テンプレート パッケージ ファイルの場所に移動し、そのファイルを選択します。
5. **保存**をクリックします。
6. 一覧で、選択された行をマークします。 作成したデータ共有ポリシーを選択します。  
7. **インポート**をクリックします。
8. **閉じる**をクリックします。
9. ページを更新します。
10. ページを閉じます。
11. ページを閉じます。
12. ページを閉じます。
13. **ナビゲーション ウィンドウ > モジュール > システム管理 > セットアップ > 会社間データ共有のコンフィギュレーション**の順に移動します。
14. 一覧で**支払期日**を検索して、選択します。
15. **追加**をクリックします。
16. 一覧で、選択された行をマークします。
17. **会社**フィールドで、「USSI」と入力します。
18. **追加**をクリックします。
19. **会社**フィールドで、「USMF」と入力します。
20. **保存**をクリックします。
21. **有効化**をクリックします。
22. **はい** をクリックします。
23. **共有の問題を検索する**をクリックします。
24. **はい** をクリックします。
25. **フィールド値の更新**をクリックします。
26. **会社 1 の値を使用**をクリックします。
27. ページを更新します。
28. ページを閉じます。


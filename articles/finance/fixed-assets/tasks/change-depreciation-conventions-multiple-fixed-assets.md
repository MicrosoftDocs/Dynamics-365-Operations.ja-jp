---
title: 複数の固定資産の減価償却方法の変更
description: このタスクは、指定した固定資産グループに適用する減価償却方法を更新します。
author: moaamer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31d499f55652377b91dd6ef9d3ece13806fbcee3
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710532"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a>複数の固定資産の減価償却方法の変更

[!include [banner](../../includes/banner.md)]

このタスクは、指定した固定資産グループに適用する減価償却方法を更新します。 このタスク ガイドでは、デモ会社 USMF を使用します。

1. [固定資産] > [定期処理のタスク] > [一括更新] の順に移動します。
2. [減価償却簿] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、選択された行のリンクをクリックします。
4. [資産利用開始日] フィールドで、日付を入力します。
5. [資産利用終了日] フィールドで、日付を入力します。
    * 選択した減価償却簿に含まれる資産のうち、これらの日付の間に利用されていた資産のみが更新されます。  
6. [現在の減価償却方法] フィールドで、オプションを選択します。
    * 現在の減価償却方法がある資産のみ更新されます。  
7. [新規減価償却方法] フィールドで、オプションを選択します。
    * レポートの検証は、任意の出力先に印刷します。  
8. [対象に含めるレコード] セクションを展開します。
9. [フィルター] をクリックします。
10. リストで、[固定資産グループ] を選択します。
11. [基準] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
12. 目的の固定資産グループを選択します。
13. 一覧で、選択された行のリンクをクリックします。
14. [OK] をクリックします。
15. [OK] をクリックします。
    *  処理結果は、一括更新のレポートに表示されます。     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

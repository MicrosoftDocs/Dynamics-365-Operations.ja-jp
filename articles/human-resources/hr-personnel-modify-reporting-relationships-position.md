---
title: 職位の報告関係の修正
description: この手順は、従業員に対して報告関係を変更する方法を示します。
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ad7220661677ce72168d20903486230411ec00f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688528"
---
# <a name="modify-reporting-relationships-for-a-position"></a>職位の報告関係の修正


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



この手順は、従業員に対して報告関係を変更する方法を示します。 報告関係は、ワークフローを通してドキュメントを回覧するときに使用できます。 手順は、追加の階層に従業員を割り当てる方法も示します。 たとえば、従業員がプロジェクトの監修者への非公式の報告関係を伴うプロジェクト・チームの一員である場合があります。 追加の報告関係は、さまざまなプロジェクトまたはマトリックスのシナリオに対応する職位に定義できます。 この手順の作成に使用するデモ データの会社は USMF です。

1. **人事管理** \> **職位** \> **職位** に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、**000091** という値で **職位** フィールドをフィルター処理します。
3. 一覧で、選択した行のリンクを選択します。
4. **報告先職位** セクションを展開します。
5. **新規** を選択して、ドロップダウン ダイアログ ボックスを開きます。
6. **報告先職位** フィールドで値を入力または選択します。
7. **作成** を選択します。
8. **リレーションシップ** セクションを展開します。
9. **追加** を選択します。
10. グリッドの左にあるチェック ボックスをオンにします。
11. **階層名** フィールドで、値 (例: **プロジェクト**) を入力または選択します。
12. **報告先職位** フィールドで値を入力または選択します (例: **000437**)。
13. **保存** を選択します。



[!INCLUDE[footer-include](../includes/footer-banner.md)]

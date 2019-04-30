---
title: 職位の報告関係の修正
description: この手順は、従業員に対して報告関係を変更する方法を示します。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a1afd2c1cdc2ebaa303030d01b3bbe5fd2af44f
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "857272"
---
# <a name="modify-reporting-relationships-for-a-position"></a>職位の報告関係の修正

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順は、従業員に対して報告関係を変更する方法を示します。 報告関係は、ワークフローを通してドキュメントを回覧するときに使用できます。 手順は、追加の階層に従業員を割り当てる方法も示します。 たとえば、従業員がプロジェクトの監修者への非公式の報告関係を伴うプロジェクト・チームの一員である場合があります。 追加の報告関係は、さまざまなプロジェクトまたはマトリックスのシナリオに対応する職位に定義できます。 この手順の作成に使用するデモ データの会社は USMF です。

1. [人事管理] > [職位] > [職位] に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、「000091」という値を含む [職位] フィールドをフィルター処理します。
3. 一覧で、選択された行のリンクをクリックします。
4. [報告先職位] セクションを展開します。
5. [新規] をクリックすると、ドロップ ダイアログが開きます。
6. [報告先職位] フィールドで値を入力または選択します。
7. [作成] をクリックします。
8. [リレーションシップ] セクションを展開します。
9. [追加] をクリックします。
10. グリッドの左にあるチェック ボックスをオンにします。
11. [階層名] フィールドで、値を入力または選択します。
    * 例 : プロジェクト  
12. [報告先職位] フィールドで値を入力または選択します。  例: 000437
13. [保存] をクリックします。


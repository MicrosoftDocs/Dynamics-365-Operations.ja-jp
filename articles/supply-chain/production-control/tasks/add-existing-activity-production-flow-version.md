---
title: 生産フロー バージョンへの既存の活動の追加
description: 生産フローの新バージョンを作成する際に、旧バージョン向けに作成された活動を新バージョンに加えることができます。
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 315a82ce3502164fcf7813e866fb3dc1806d03d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843964"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>生産フロー バージョンへの既存の活動の追加

[!include [task guide banner](../../includes/task-guide-banner.md)]

生産フローの新バージョンを作成する際に、旧バージョン向けに作成された活動を新バージョンに加えることができます。 この手順では、活動をコピーしないで既存の生産フロー向けの新バージョンの作成方法を示します。 次の手順では、既存の活動が新バージョンに追加されます。 

この作業には、既に作成されたバージョンおよび活動を含む生産フローが必要です。


## <a name="create-a-new-production-flow-version"></a>新しい生産フロー バージョンの作成
1. [生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. [編集] をクリックします。
5. 一覧で、選択された行をマークします。
6. [有効期限] フィールドに日時を入力します。
    * 新規生産フロー バージョンを作成する前に、有効なバージョンの期限切れの日時をチェックすることに注意してください。 新規バージョンは有効な開始日（バージョン終了日の翌日）で作成します。  
7. [追加] をクリックします。
8. [バージョンからのコピー] フィールドで、「いいえ」を選択します。
    * コピーしたバージョンの活動の大半が新しい活動と交換された場合、[空のバージョンで開始する] に「いいえ」を選択します。 変更のない活動を、手動で「活動形式における既存機能に加える」に加えます。  
9. [重複するかんばんルール] フィールドで、「いいえ」を選択します。
    * 活動が新しいバージョンにコピーされていない場合、新しいバージョンの作成時にかんばんルールをコピーすることはできません。   代わりに、旧生産フローバージョンのかんばんルールを新規バージョンの活動を使用するかんばんルールと交換するために、交換かんばん機能かんばんルール形式で作成します。  
10. [OK] をクリックします。
11. 一覧で、目的のレコードを見つけ、選択します。

## <a name="add-an-existing-activity"></a>既存の活動を追加する
1. [活動] をクリックします。
2. [既存を追加] をクリックして、ドロップ ダイアログを開きます。
    * 新規生産フロー バージョンに追加される既存の活動を検索、選択します。  リストは、フローの以前のバージョンに代わるこの生産フローのために作成されたすべての活動を示すことに注意してください。  
3. [活動] フィールドで値を入力または選択します。
4. [OK] をクリックします。


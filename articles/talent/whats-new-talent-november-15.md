---
title: Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 11 月 15 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "305091"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a>Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 11 月 15 日)

[!include [banner](includes/banner.md)]

**ビルド 8.1.2045**

このトピックでは、Core HR の新機能または変更された機能について説明します。

## <a name="other-changesfixes"></a>その他の変更または修正

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>従業員の現在の職位を将来の空いている職位に変更することができない

職位が将来でのみ利用可能な場合、職位の転送を有効にするための変更が行われました。 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>新しい従業員を作成するときに職位が表示されない

Talent で新しい従業員を採用するときに割り当て可能なすべての空いている職位を表示するための変更が行われました。 これには、過去の職位または、職位が将来の日付になっているかどうかが含まれます。 職位が雇用開始日に基づいて正しく表示されます。 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>退職日はユーザーの設定に基づいて表示される

退職日を表示しているときに、従業員の優先タイム ゾーンのタイム ゾーン オフセットを考慮に入れるための変更が過去の従業員のリストに行われました。

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>自分に割り当てられた作業項目のリンクが正しい情報を表示しない

この変更により、個々の作業項目のリストの詳細へのナビゲーションは、選択した項目の正しい情報を表示します。 この問題は、高度なセキュリティ オプションでのみ発生しました。


## <a name="known-issue"></a>既知の問題

- **問題**: 作業者に新しい添付ファイルを追加する時、**新規**および**編集**ボタンが灰色表示になります。 
- **回避策:** 添付ファイル ページを開く前に、**作業者**ページの Factbox が閉じていることを確認します。 **作業者**ページが読み込まれる時、FactBoxes が閉じている場合には、添付ファイルボタンが有効になります。 (この問題は次のプラットフォーム更新プログラムで修正されます。)

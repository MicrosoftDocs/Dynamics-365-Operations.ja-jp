---
title: Attract ユーザーがキャリア ポータルから仕事に応募できない
description: このトピックでは、Attract ユーザーが求人ポータルからジョブに応募できない問題のトラブルシューティング方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461723"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Attract ユーザーがキャリア ポータルから仕事に応募できない

[!include [banner](includes/banner.md)]

## <a name="issue"></a>出庫

Attract ユーザーがキャリア ポータルからジョブに応募できません。 Dynamics 365 Talent: Attract で作成したジョブに応募しようとすると、ブラウザーがページを読込んだままになり、アクションが実行されません。

## <a name="cause"></a>原因

この問題は、Talent Relationship チームが Talent ユーザー ロールを持っていない場合に発生します。

## <a name="resolution"></a>解像度

Talent ユーザー ロールを Talent Relationship チームに割り当ててください。

1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com) に次のいずれかの管理者資格情報を使用してログインします。

   - Dynamics 365 管理者
   - Global 管理者
   - Power Platform 管理者

2. ナビゲーション ペインで、**環境** を選択し、Talent ユーザー ロールを Talent Relationship チームに割り当てる環境を選択します。

   ![環境の選択](./media/attract-troubleshoot-career-portal-select-environment.png)

3. **環境** ペインで、**環境 URL** を選択し、環境管理者ポータルにログインします (たとえば、https:<orgname> .crm.dynamics.com)。

4. **設定**、**システム**、**セキュリティ** の順に選択します。

   ![セキュリティに移動する](./media/attract-troubleshoot-career-portal-security.png)

5. **チーム** を選択します。

   ![チームの選択](./media/attract-troubleshoot-career-portal-security-teams.png)

6. 検索ボックスで **Talent Relationship チーム** を検索し、検索結果からチームを選択します。

7. リボンから **ロールの管理** を選択します。

8. **チーム ロールの管理** ダイアログで、使用可能なロールの一覧から **Talent ユーザー** を選択し、**OK** を選択してロールを適用します。

   ![ロールの適用](./media/attract-troubleshoot-career-portal-apply-role.png)

9. 次のように変更をテストします。

   1. 新しいブラウザ ウィンドウから、キャリア ポータルにログインします。
   2. このジョブを求人ポータルから適用します。 
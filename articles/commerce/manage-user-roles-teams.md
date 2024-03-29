---
title: Microsoft Teams でユーザーとロールを管理する
description: この記事では、Microsoft Dynamics 365 Commerce のユーザー ロールを Microsoft Teams で管理する方法を説明します。
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2984bf1d4d93c3a83cb6ba215617074c786c2c99
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286387"
---
# <a name="manage-user-roles-in-microsoft-teams"></a>Microsoft Teams でユーザーとロールを管理する

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce のユーザー ロールを Microsoft Teams で管理する方法を説明します。

Teams 内の各店舗またはチャネルに対してチームを作成する場合は、そのチームに対応するグループのメンバー数 (たとえば、`HOUSTON_D365@<YourTenantAzureADDomain>.com`)。 チーム グループのメンバーとなっているすべての店舗の従業員には、**オーナー** または **メンバー** 2つのユーザー ロールのうちの1つが割り当てられます。 **所有者** のユーザー ロールを持つ店舗の従業員は、プライベート チャンネルの追加、メンバーの追加または削除などの操作を実行できます。 通常、店長は **所有者** のユーザー ロールを持っています。

次の図は、チーム メンバーの一覧と、Microsoft Teams 管理センターでのユーザー ロールの例を示しています。

![Microsoft Teams 管理センターのチーム メンバーとユーザー ロール。](media/d365-commerce-teams-integration-user-roles.png)

詳細については、[Microsoft Teams におけるチームの所有者とメンバーの割り当て](/microsoftteams/assign-roles-permissions)を参照してください。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce と Microsoft Teams データ統合の概要](commerce-teams-integration.md)

[Dynamics 365 Commerce と Microsoft Teams の統合を有効化する](enable-teams-integration.md)

[Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング](provision-teams-from-commerce.md)

[Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる](synchronize-tasks-teams-pos.md)

[Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします](map-stores-existing-teams.md)

[Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ](teams-integration-faq.md)

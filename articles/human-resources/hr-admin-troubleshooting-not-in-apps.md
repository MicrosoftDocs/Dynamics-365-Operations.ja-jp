---
title: Microsoft Dynamics 365 アプリでは、人事管理が表示されない
description: このトピックでは、Microsoft Dynamics 365 Human Resources が Microsoft Dynamics 365 アプリで表示されない場合の対処方法について説明します。
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bdbe6c4065a8266fd30a3b093743ded91524f6a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069683"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources アプリが Microsoft Dynamics 365アプリに表示されない


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**問題**

顧客は、Microsoft Dynamics 365 アプリで Dynamics 365 Human Resources を表示できません。

**解像度**

ユーザーは、Microsoft Power Apps の環境の、環境メーカー ロールに追加される必要があります。

1. Power Apps プラン 2 ライセンスを持つ管理者ユーザーは、[Power Apps 管理ポータル](https://preview.admin.powerapps.com/) を開く必要があります。

2. **環境** を選択してから、人事管理の正しい環境を選択します。

3. **セキュリティ** タブの、**環境ロール** タブで、**環境メーカー** を選択します。

    ![環境ロール タブ。](media/environment-roles.png)

4. **ユーザー** タブで、ユーザーまたは組織を追加します。

    ![ユーザー タブ。](media/environment-maker.png)

5. **保存** を選択します。

6. ユーザーはこの時点で [Microsoft Dynamics 365](https://home.dynamics.com/) にサインインする必要があります。

7. **同期** を選択してユーザー アプリを更新します。

    ![同期ボタン。](media/get-more.png)

    同期が完了した後、人事管理はホーム ページに表示されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]

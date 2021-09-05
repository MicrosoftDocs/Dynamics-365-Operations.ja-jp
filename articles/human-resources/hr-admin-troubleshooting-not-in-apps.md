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
ms.openlocfilehash: dfed82463eece882bed66c7b2dac1dd30e04720e
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413404"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources アプリが Microsoft Dynamics 365アプリに表示されない

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

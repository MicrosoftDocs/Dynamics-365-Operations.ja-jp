---
title: Microsoft Dynamics 365 アプリでは、人事管理が表示されない
description: この記事では、顧客が Microsoft Dynamics 365 アプリの中で Microsoft Dynamics 365 Human Resources アプリを表示できない場合の対処方法について説明します。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d78199cf0e76ffd0676a26961a8e646938dc7333
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113305"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Microsoft Dynamics 365 アプリでは、人事管理が表示されない

**問題点**

顧客は、Microsoft Dynamics 365 アプリで Dynamics 365 Human Resources を表示できません。

**解像度**

ユーザーは、Microsoft Power Apps の環境の、環境メーカー ロールに追加される必要があります。

1. Power Apps プラン 2 ライセンスを持つ管理者ユーザーは、[Power Apps 管理ポータル](https://preview.admin.powerapps.com/) を開く必要があります。

2. **環境** を選択してから、人事管理の正しい環境を選択します。

3. **セキュリティ** タブの、**環境ロール** タブで、**環境メーカー** を選択します。

    ![環境ロール タブ](media/environment-roles.png)

4. **ユーザー** タブで、ユーザーまたは組織を追加します。

    ![ユーザー タブ](media/environment-maker.png)

5. **保存** を選択します。

6. ユーザーはこの時点で [Microsoft Dynamics 365](https://home.dynamics.com/) にサインインする必要があります。

7. **同期** を選択してユーザー アプリを更新します。

    ![同期ボタン](media/get-more.png)

    同期が完了した後、人事管理はホーム ページに表示されます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
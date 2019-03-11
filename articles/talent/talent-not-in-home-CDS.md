---
title: Microsoft Dynamics 365 アプリ (CDS1.0) で Talent が表示されない
description: このトピックでは、顧客が Microsoft Dynamics 365 アプリの中で Microsoft Dynamics 365 for Talent アプリを表示できない場合の対処方法について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "305191"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>Microsoft Dynamics 365 アプリ (CDS1.0) で Talent が表示されない

[!include [banner](includes/banner.md)]

**払出**

顧客は、Microsoft Dynamics 365 アプリの中で Microsoft Dynamics 365 for Talent アプリを表示できません。

**解像度**

ユーザーは、Microsoft PowerApps の環境の、環境メーカー ロールに追加される必要があります。

1. PowerApps プラン 2 ライセンスを持つ管理者ユーザーは、[PowerApps 管理ポータル](https://preview.admin.powerapps.com/) を開く必要があります。
2. **環境**を選択してから、Talent の正しい環境を選択します。
3. **セキュリティ**タブの、**環境ロール**タブで、**環境メーカー**を選択します。

    ![環境ロール タブ](media/environment-roles.png)

4. **ユーザー**タブで、ユーザーまたは組織を追加します。

    ![ユーザー タブ](media/environment-maker.png)

5. **保存** を選択します。
6. ユーザーはこの時点で [Microsoft Dynamics 365](https://home.dynamics.com/) にサインインする必要があります。
7. **同期**を選択してユーザー アプリを更新します。

    ![同期ボタン](media/get-more.png)

    同期が完了した後、Talent はホーム ページに表示されます。

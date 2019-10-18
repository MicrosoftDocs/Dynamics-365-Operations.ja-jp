---
title: ユーザーが Core HR にアクセスできるが、Onboard または Attract にアクセスできない
description: このトピックでは、ユーザーが Microsoft Dynamics 365 Talent - Core HR にはアクセスできるが、Attract または Onboard にはアクセスできない問題を解決する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 80b1f8aeabfd033f393463f4be5a61447377f2d9
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009309"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a>ユーザーが Core HR にアクセスできるが、Onboard または Attract にアクセスできない

[!include [banner](includes/banner.md)]

**環境の詳細**

- Microsoft Dynamics Lifecycle Services (LCS) の配置がユーザー A によって実行されました。
- ユーザー A は、Microsoft Dynamics 365 Talent: Core HR にユーザーとしてユーザー B を追加します。

**問題点**

ユーザー B は、Core HR にアクセスできますが、Talent に: Attract または Talent に: Onboard アプリにアクセスできません。 ユーザーが**エクスペリエンス アプリ**に移動しようとすると、代わりに試用環境に移動してしまいます。

**ソリューション**

ユーザー B は、プロビジョニング プロセス中にユーザー A が作成した Microsoft PowerApps の環境を表示するための権限を割り当てられる必要があります。

詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) の「環境へのアクセス許可の付与」セクションを参照してください。

**長期のソリューション**

Microsoft は、ユーザーが Core HR に追加される際に Onboard および Attract に適切な権限を自動的に割り当てることを検討しています。

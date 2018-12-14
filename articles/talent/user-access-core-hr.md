---
title: "ユーザーは Core HR にアクセスできるが、Onboard または Attract アプリにはアクセスできない"
description: "このトピックでは、ユーザーが Microsoft Dynamics 365 for Talent Core HR にはアクセスできるが、Attract または Onboard アプリにはアクセスできない問題を解決する方法について説明します。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>ユーザーは Core HR にアクセスできるが、Onboard または Attract アプリにはアクセスできない

[!include [banner](includes/banner.md)]

**環境の詳細**

- Microsoft Dynamics Lifecycle Services (LCS) の配置がユーザー A によって実行されました。
- ユーザー A は、Microsoft Dynamics 365 for Talent Core HR にユーザーとしてユーザー B を追加します。

**払出**

ユーザー B は、Core HR にアクセスできますが、Talent に: Attract または Talent に: Onboard アプリにアクセスできません。 ユーザーが**エクスペリエンス アプリ**に移動しようとすると、代わりに試用環境に移動してしまいます。

**ソリューション**

ユーザー B は、プロビジョニング プロセス中にユーザー A が作成した Microsoft PowerApps の環境を表示するための権限を割り当てられる必要があります。

詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) の「環境へのアクセス許可の付与」セクションを参照してください。

**長期のソリューション**

Microsoft は、ユーザーが Core HR に追加される際に Onboard および Attract に適切な権限を自動的に割り当てることを検討しています。


---
title: ユーザーは人事管理にアクセスできるが、Onboard または Attract にアクセスできない
description: このトピックでは、ユーザーが Microsoft Dynamics 365 Talent - 人事管理にはアクセスできるが、Attract または Onboard にはアクセスできない問題を解決する方法について説明します。
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006313"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a>ユーザーは人事管理にアクセスできるが、Onboard または Attract にアクセスできない

[!include [banner](includes/banner.md)]

**環境の詳細**

- Microsoft Dynamics Lifecycle Services (LCS) の配置がユーザー A によって実行されました。
- ユーザー A は、Microsoft Dynamics 365 Human Resources にユーザーとしてユーザー B を追加します。

**問題点**

ユーザー B は人事管理にアクセスできますが、Talent: Attract または Talent: Onboard アプリにはアクセスできません。 ユーザーが**エクスペリエンス アプリ**に移動しようとすると、代わりに試用環境に移動してしまいます。

**ソリューション**

ユーザー B は、プロビジョニング プロセス中にユーザー A が作成した Microsoft Power Apps の環境を表示するための権限を割り当てられる必要があります。

詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) の「環境へのアクセス許可の付与」セクションを参照してください。

**長期のソリューション**

Microsoft は、ユーザーが人事管理に追加される際に Onboard および Attract に適切な権限を自動的に割り当てることを検討しています。

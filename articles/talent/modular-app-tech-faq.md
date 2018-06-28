---
title: "Microsoft Dynamics 365 for Talent のモジュラー アプリのプロビジョニング"
description: "Dynamics 365 for Talent には Core HR 機能および Attract や Onboard などの追加エクスペリエンスを提供する機能が含まれます。 このような機能は、スタンドアロン モジュール アプリケーションとして購入することもできます。"
author: rschloma
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: Talent March 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 26ef32f7af0c2d8f6e4c5b1105d31672fd16065c
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent-modular-apps"></a>Microsoft Dynamics 365 for Talent のモジュラー アプリのプロビジョニング

[!include [banner](includes/banner.md)]

Dynamics 365 for Talent には、Core Human Resources 機能および Attract や Onboard などの追加エクスペリエンスを提供する機能が含まれます。 このような機能は、Web ダイレクトを通じたスタンドアロン モジュール アプリケーションとして購入することもできます (Dynamics 365 for Talent: Attract または Dynamics 365 for Talent: Onboard SKU など)。 完全な Talent をモジュラー アプリケーションと比べて購入すると、操作上の違いがいくつかあります。  

モジュラー アプリケーションは、試用版の開始時または Web ダイレクトを通じたサービスの購入時に自動的に準備されます。 Dynamics 365 for Talent のプロビジョニングに使用される Lifecycle Services (LCS) は、モジュラー アプリケーションとは使用されません。 顧客は Attract または Onboard の評価版に個別にサインアップができます。

顧客は、モジュラー アプリケーションのプロビジョニングを具体的に選択するのではなく、モジュラー アプリケーションのプロビジョニングを決定します。 

 > + 組織の既存の PowerApps 環境の場所
 > + PowerApps 環境が存在しない場合は、組織の既存のテナントの場所
 > + 現在 Dynamics 365 for Talent でサポートされているデータ センター 

モジュラー アプリケーションは、以下のロジックに従って (Microsoft Trust Center for Talent データ透過性で定義されたとおり) サポートされている地域でのみ準備されます。 

[![モジュラー アプリケーションの地域](./media/modular-apps-diagram-mod-app-tech.png)](./media/modular-apps-diagram-mod-app-tech.png)

Dynamics 365 for Talent とは異なり、モジュラー アプリケーションでは各ユーザーがアクセス可能な環境のリストは維持されません。 モジュール アプリケーション サービスを使用すると、ユーザーは最後に使用した環境に自動的にログインし、装置メニューから代替環境を選択できます。 


---
title: Dynamics 365 for Talent のモジュラー アプリのプロビジョニング
description: このトピックでは、Microsoft Dynamics 365 for Talent に含まれる Core Human Resources (HR) 機能を提供するために購入できるスタンドアロンのモジュラー アプリケーションをプロビジョニングする方法について説明します。 この機能は、Attract および Onboard などの追加エクスペリエンスを提供します。
author: andreabichsel
manager: AnnBe
ms.date: 08/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: Talent March 2018 update
ms.openlocfilehash: aa02b016e4193c2280d959b351dab1f5c74b4c2e
ms.sourcegitcommit: 3630054272c42bbfb8949c128b0284fc830254bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/30/2019
ms.locfileid: "907923"
---
# <a name="provisioning-for-the-dynamics-365-for-talent-modular-apps"></a>Dynamics 365 for Talent のモジュラー アプリのプロビジョニング

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 for Talent には、Core Human Resources (HR) 機能および Attract や Onboard などの追加エクスペリエンスを提供する機能が含まれます。 この機能は、Web ダイレクトを通じたスタンドアロン モジュール アプリケーションとして購入することもできます。 Microsoft Dynamics 365 for Talent: Attract および Microsoft Dynamics 365 for Talent: Onboard SKU などがその例です。 完全な Talent を購入するか、モジュラー アプリケーションを購入するのかによって、エクスペリエンスは多少異なります。

モジュラー アプリケーションは、サービスの試用を開始したり、Web ダイレクトを通じて購入すると自動的にプロビジョニングされます。 顧客は Attract および Onboard の試用版を個別にサインアップできます。

Microsoft Dynamics Lifecycle Services (LCS) は Talent をプロビジョニングするために使用されますが、モジュラー アプリケーションのプロビジョニングには使用されません。

顧客は、モジュラー アプリケーションをプロビジョニングする必要な正確な場所を選択しません。 代わりに、次の要因により、モジュラー アプリケーションがプロビジョニングされる場所が決定します。

+ 組織の既存の Microsoft PowerApps 環境の場所
+ PowerApps 環境が存在しない場合は、組織の既存のテナントの場所は
+ Talent が現在サポートするデータ センター

サポートされている国または地域でのみ、モジュラー アプリケーションがプロビジョニングされます。 次の図は、使用されるロジックを示しています。 サポートされている国と地域は Microsoft Trust Center for Talent データ透過性で定義されています。 サポートされている国と地域の一覧は、『[Microsoft Dynamics 365 の国際可用性ガイド](https://docs.microsoft.com/en-us/dynamics365/get-started/availability)』を参照してください。

[![国/地域に基づくモジュラー アプリケーションのプロビジョニング プロセス](./media/modular-apps-diagram-mod-app-tech.png)](./media/modular-apps-diagram-mod-app-tech.png)

Talent とは異なり、モジュラー アプリケーションでは各ユーザーがアクセス可能な環境のリストは維持されません。 ユーザーは、使用した最後の環境に自動的にサインインされます。 **設定**ボタン (ギヤ記号) を使用して、さまざまな環境を選択できます。

---
title: オンボード プロビジョニング
description: このトピックでは、スタンドアロン Dynamics 365 Talent - Onboard アプリをプロビジョニングする方法について説明します。
author: andreabichsel
ms.date: 04/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: Talent March 2018 update
ms.openlocfilehash: 8a50292c58d004fb3dcb676532b80fc31479c5ad
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353878"
---
#  <a name="provision-onboard"></a>オンボード プロビジョニング

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent の完全版には、中核人事 (Core HR) 機能に加えて Attract と Onboard が含まれており、社内の 採用と オンボードのプロセス を認識することができます。 また、オンボード アプリのスタンドアロンバージョンを購入することもできます。 Talent の完全版とスタンドアロンのオンボードアプリのどちらを購入したかによって、プロビジョニング内容が若干異なります。

オンボードアプリは、試用版を起動するか、またはオンラインで購入したときに自動的に準備されます。 完全版の Talent を使用するにはプロビジョニングのために Microsoft Dynamics Lifecycle Services (LCS) が必要となりますが、スタンドアロンの Onboard アプリには LCS は必要ありません。

スタンドアロンの Onboard アプリでは、プロビジョニングの対象を選択をすることはありません。 そのかわりに、以下の要素によって Onboard がプロビジョニングされる場所が決まります。

- Microsoft Power Apps 環境が存在する場合は同環境の場所を参照します
- Power Apps 環境が存在しない場合は、組織の既存のテナントの場所を参照します
- Talent が現在対応しているデータ センター

Onboard アプリは、対応する国または地域でのみで提供しています。 サポートされている国と地域は Microsoft Trust Center for Talent データ透過性で定義されています。 サポートされている国と地域の一覧は、『[Microsoft Dynamics 365 の国際可用性ガイド](/dynamics365/get-started/availability)』を参照してください。

以下の図では、スタンドアロンの Onboard アプリを提供するにあたって使用されているロジックを示しています。

[![国/地域に基づいた、スタンドアロン Onboard アプリのプロビジョニング プロセス。](./media/modular-apps-diagram-mod-app-tech.png)](./media/modular-apps-diagram-mod-app-tech.png)

完全版の Talent とは異なり、スタンドアロンの Onboard アプリ では、各ユーザーがアクセス可能となる環境の一覧を管理していません。 ユーザーは、最後に使用した環境に自動的にサインインします。 **設定** ボタン (ギヤ記号) を使用して、さまざまな環境を選択できます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
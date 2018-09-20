---
title: "小売機能の配置オプション"
description: "このトピックでは、Dynamics 365 for Retail と Dynamics 365 for Finance and Operations の間の小売機能の違いについて説明します。"
author: ashishmsft
manager: AnnBe
ms.date: 10/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: asharchw
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: df560a3c3e628f3971af29281f5f8bd0500e42fe
ms.openlocfilehash: 2e0ffe70db059a0bddac9861c4df8b0dc095d5a8
ms.contentlocale: ja-jp
ms.lasthandoff: 08/14/2018

---

# <a name="deployment-options-for-retail-functionality"></a>小売機能の配置オプション

[!include [banner](../../includes/banner.md)]

小売機能は、次の製品で使用できます。
 
- Dynamics 365 for Retail
- Dynamics 365 for Finance and Operations
 
Dynamics 365 for Retail には、ほとんどの小売業者が通常使用する主要な小売機能が含まれています。 この状況に応じた機能が、生産性を向上し、従業員の採用およびトレーニングのプロセスの簡素化に役立ちます。 

Dynamics 365 for Retail には、追加機能を有効にするオプションがあります。 つまり、Dynamics 365 for Finance and Operations 環境と同じ機能フットプリントを持つ Dynamics 365 for Retail 環境を展開できます。
 
次のテーブルに、Dynamics 365 for Retail と Dynamics 365 for Finance and Operations の主な違いを示します。

| 能力   |  Dynamics 365 for Retail   |  Dynamics 365 for Finance and Operations  |
|--------------|----------------------------|-------------------------------------------|
|アプリケーション モデルの更新をシームレスに受け取ります。 (アプリケーション モデルの更新は、カスタマイズしてコンパイルしたりマージしたりする必要はありません。) | 有 | 無|
|小売チャンネル コンポーネントの更新プログラムをシームレスに受け取ります。 (小売チャネル コンポーネントの更新は、カスタマイズしてマージする必要はありません。) | 有 | 有 |
|小売機能のみを提供するスコープのあるソリューションを展開します。 | 有  | はい*<br><br>\* 配置後にコンフィギュレーションできます。  |
|インテリジェントで最新の企業ビジネス アプリケーションによって、財務および操作を最適化して成長を促進し、リアルタイムのデータに基づく判断を行います。| いいえ*<br><br>\* Unified Operations Plan または Dynamics 365 Plan で追加機能を有効にすることができます。 | 有 |

ライセンスの詳細については、[ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409) を参照してください。

テナントとしての必要なライセンスを取得した後、Lifecycle Services (LCS) を最初にアクセスするとき、実装プロジェクト タイプを選択するように要求されます。実装プロジェクト タイプでは、**Dynamics 365 for Retail** または **Dynamics 365 for Finance and Operations** を選択する必要があります。 上記の考慮事項を使用すると、適切な製品を選択して展開することができます。
 
上の表に示すように、Dynamics 365 for Retail を配置する場合、(必要なライセンスがある場合) 配置時にソリューションを構成するオプションがあります。 

- ソリューションの対象範囲を小売機能のみにする場合は、**小売のみ**を選択します。 
- 追加機能を有効にする場合は、**小売 + 工程**を選択します。
 
![配置設定](media/Deployment-settings.png)


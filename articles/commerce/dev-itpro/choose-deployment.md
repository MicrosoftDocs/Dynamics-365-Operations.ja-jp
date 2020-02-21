---
title: 小売機能の配置オプション
description: このトピックでは、Dynamics 365 Commerce と Dynamics 365 Finance 間の機能の違いについて説明します。
author: ashishmsft
manager: AnnBe
ms.date: 10/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: asharchw
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: f77fc4857c743a35bf176f3b578e49b9b4831dab
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004597"
---
# <a name="deployment-options-for-retail-functionality"></a>小売機能の配置オプション

[!include [banner](../../includes/banner.md)]

コマース機能は、次の製品で使用できます。
 
- Dynamics 365 Commerce
- Dynamics 365 Finance
 
コマースには、ほとんどの小売業者が通常使用する主要な小売機能が含まれています。 この状況に応じた機能が、生産性を向上し、従業員の採用およびトレーニングのプロセスの簡素化に役立ちます。 

コマースには、追加機能を有効にするオプションがあります。 つまり、Finance 環境として機能的範囲が同じ環境を展開することができます。
 
次の表に、Commerce と Finance and Operations との主な違いを示します。

| 能力   |  Dynamics 365 Commerce   |  Dynamics 365 Finance |
|--------------|----------------------------|-------------------------------------------|
|アプリケーション モデルの更新をシームレスに受け取ります。 (アプリケーション モデルの更新は、カスタマイズしてコンパイルしたりマージしたりする必要はありません。) | はい | いいえ|
|チャンネル コンポーネントの更新プログラムをシームレスに受け取ります。 (チャネル コンポーネントの更新は、カスタマイズしてマージする必要はありません。) | はい | はい |
|コマース機能のみを提供するスコープのあるソリューションを展開します。 | はい  | はい*<br><br>\* 配置後にコンフィギュレーションできます。  |
|インテリジェントで最新の企業ビジネス アプリケーションによって、財務および操作を最適化して成長を促進し、リアルタイムのデータに基づく判断を行います。| いいえ*<br><br>\* Finance and Operations Plan または Dynamics 365 Plan で追加機能を有効にすることができます。 | はい |

ライセンスの詳細については、[ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409) を参照してください。

テナントとしての必要なライセンスを取得した後、Lifecycle Services (LCS) を最初にアクセスするとき、実装プロジェクト タイプを選択するように要求されます。実装プロジェクト タイプでは、**Dynamics 365 Commerce** または **Dynamics 365 Finance** を選択する必要があります。 上記の考慮事項を使用すると、適切な製品を選択して展開することができます。
 
上の表に示すように、Dynamics 365 Commerce を展開する場合 (また必要なライセンスがある場合)、必要に応じて、展開時にソリューションを構成することができます。 

- ソリューションの対象範囲をコマース機能のみにする場合は、**コマースのみ**を選択します。 
- 追加機能を有効にする場合は、**コマース + 工程**を選択します。
 
![配置設定](media/Deployment-settings.png)

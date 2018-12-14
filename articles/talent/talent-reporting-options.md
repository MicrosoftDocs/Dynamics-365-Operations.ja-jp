---
title: "Talent のレポート オプション"
description: "このトピックでは、顧客が Microsoft Dynamics 365 for Talent のレポートをカスタマイズしたり、新しいレポートを作成する場合の問題を解決する方法について説明します。"
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
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a>Talent のレポート オプション

[!include [banner](includes/banner.md)]

**環境の詳細**

この問題は、すべての環境に適用されます。

**現象**

顧客は Microsoft Dynamics 365 for Talent のレポートをカスタマイズしたり、新しいレポートを作成したいと考えています。

**払出**

ユーザーは、埋め込み Microsoft Power BI レポートをカスタマイズすることはできません。

**ソリューション**

- アプリ用 Common Data Service にフローする Core HR データは、Power BI Desktop に PowerApps CD コネクタ経由でレポートできます。 アプリ用 Common Data Service には Core HR データのサブセットが含まれていることに注意してください。 Power BI およびダッシュボードの詳細については、[PowerApps Common Data Service を使用した Power BI レポートおよびダッシュボードの作成](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi) を参照してください。
- 電子申告 (ER) は、一部の Talent レポートで利用できます。 顧客主導のカスタマイズは、ER コンフィギュレーション オプション経由で実行できます。
- データは、Microsoft Office 統合によって Talent が提供するさまざまなデータ エンティティを使用して、Microsoft Excel や Microsoft Word にエクスポートできます。

**長期のソリューション**

追加の Power BI オプションが利用可能になり、さらに多くのデータとエンティティがアプリ用 Common Data Service の一部になります。


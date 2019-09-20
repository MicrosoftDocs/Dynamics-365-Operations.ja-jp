---
title: Talent のレポート オプション
description: このトピックでは、顧客が Microsoft Dynamics 365 for Talent のレポートをカスタマイズしたり、新しいレポートを作成する場合の問題を解決する方法について説明します。
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
ms.openlocfilehash: 8e7348a515b08523c15aa8f74d5616a3daf645b7
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741801"
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

- Common Data Service にフローする Core HR データは、Power BI Desktop に PowerApps Common Data Service コネクタ経由でレポートできます。 Common Data Service には Core HR データのサブセットが含まれていることに注意してください。 Power BI およびダッシュ ボードの詳細については、「[PowerApps Common Data Service を使用した Power BI レポートおよびダッシュ ボードの作成](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi)」を参照してください。
- 電子申告 (ER) は、一部の Talent レポートで利用できます。 顧客主導のカスタマイズは、ER コンフィギュレーション オプション経由で実行できます。
- データは、Microsoft Office 統合によって Talent が提供するさまざまなデータ エンティティを使用して、Microsoft Excel や Microsoft Word にエクスポートできます。

**長期のソリューション**

追加の Power BI オプションが利用可能になり、さらに多くのデータとエンティティが Common Data Service の一部になります。

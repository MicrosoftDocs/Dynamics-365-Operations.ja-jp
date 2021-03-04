---
title: レポート オプション
description: この記事は、顧客が Microsoft Dynamics 365 Human Resources のレポートをカスタマイズしたり、新しいレポートを作成する場合の問題を解決する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51d84df5c3c29510e2742148b8c260a2cf402639
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527720"
---
# <a name="reporting-options"></a>レポート オプション

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**環境の詳細**

この問題は、すべての環境に適用されます。

**現象**

顧客は Microsoft Dynamics 365 Human Resources のレポートをカスタマイズしたり、新しいレポートを作成したいと考えています。

**払出**

ユーザーは、埋め込み Microsoft Power BI レポートをカスタマイズすることはできません。

**ソリューション**

- Common Data Service にフローする人事管理データは、Power BI Desktop に Power Apps Common Data Service コネクタ経由でレポートできます。 Common Data Service には、人事管理データのサブセットが含まれていることに注意してください。 Power BI およびダッシュ ボードの詳細については、[Power Apps Common Data Service を使用した Power BI レポートおよびダッシュ ボードの作成](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) を参照してください。
- 電子申告 (ER) は、一部の人事管理レポートで利用できます。 顧客主導のカスタマイズは、ER コンフィギュレーション オプション経由で実行できます。
- データは、Microsoft Office 統合によって人事管理が提供するさまざまなデータ エンティティを使用して、Microsoft Excel や Microsoft Word にエクスポートできます。

**長期のソリューション**

追加の Power BI オプションが利用可能になり、さらに多くのデータとエンティティが Common Data Service の一部になります。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
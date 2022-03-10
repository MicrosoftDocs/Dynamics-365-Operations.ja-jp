---
title: レポート オプション
description: このトピックでは、Microsoft Dynamics 365 Human Resources レポートをカスタマイズする、または新しいレポートを作成する方法について説明します。
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3c82f3d4f040f680cab68228f1aa8ab16f548961
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069074"
---
# <a name="reporting-options"></a>レポート オプション


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



**環境の詳細**

この問題は、すべての環境に適用されます。

**現象**

顧客は Microsoft Dynamics 365 Human Resources のレポートをカスタマイズしたり、新しいレポートを作成したいと考えています。

**出庫**

ユーザーは、埋め込み Microsoft Power BI レポートをカスタマイズすることはできません。

**ソリューション**

- Dataverse にフローする人事管理データは、Power BI Desktop に Power Apps Dataverse コネクタ経由でレポートできます。 Dataverse には、人事管理データのサブセットが含まれていることに注意してください。 Power BI およびダッシュ ボードの詳細については、[Power Apps Common Data Service を使用した Power BI レポートおよびダッシュ ボードの作成](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) を参照してください。
- 電子申告 (ER) は、一部の人事管理レポートで利用できます。 顧客主導のカスタマイズは、ER コンフィギュレーション オプション経由で実行できます。
- データは、Microsoft Office 統合によって人事管理が提供するさまざまなデータ エンティティを使用して、Microsoft Excel や Microsoft Word にエクスポートできます。

**長期のソリューション**

追加の Power BI オプションが利用可能になり、さらに多くのデータとエンティティが Dataverse の一部になります。


[!INCLUDE[footer-include](../includes/footer-banner.md)]

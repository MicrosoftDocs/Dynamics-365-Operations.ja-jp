---
title: 顧客ロイヤルティ カードと報酬ポイント
description: この記事では、二重書き込みでの顧客ロイヤルティ カードと報酬ポイントに関するデータの統合について説明します。
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 399682b3042c32fbf6fa200213f1b4982ed97174
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289117"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>顧客ロイヤルティ カードと報酬ポイント

[!include [banner](../../includes/banner.md)]



企業は、顧客の買い物と支出パターンに基づいて、顧客を分類し、高度なサービスを提供します。 例えば、Dynamics 365 Commerce では、顧客ロイヤルティ カード、報酬ポイント、ロイヤルティに基づく買い物による価格設定、報奨ベースの買い物に役立つように、インフラストラクチャと機能が搭載されています。 顧客のロイヤルティ カードと Commerce での報奨ポイントに関するデータが Dataverse に同期されている場合、Customer Engagement アプリでそのデータを使用できます。 たとえば、Dynamics 365 Customer Service のユーザーは、このデータを使用して、ヘルプデスクを介して同じ高度なサービスを提供することができます。

## <a name="templates"></a>テンプレート

財務と運用アプリ | Customer Engagement アプリ     | 説明
|-----------------------------|-----------------------------------|-------------|
[ロイヤルティ カード](mapping-reference.md#149) | msdyn_loyaltycards | このテンプレートは、顧客のロイヤリティ カードに関する情報を同期します。 |
[ロイヤルティ レベル](mapping-reference.md#226) | msdyn_loyaltylevels | このテンプレートは、顧客の報酬ポイントに関する情報を同期します。 |
[ロイヤルティ報酬ポイント](mapping-reference.md#150) | msdyn_loyaltyrewardpoints | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

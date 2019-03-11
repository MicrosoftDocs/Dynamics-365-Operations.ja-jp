---
title: ローカライズ モデルの分離
description: ローカライズおよび翻訳向け LCS ソリューションの要件の一部として、以前のバージョンの Microsoft Dynamics 365 for Finance and Operations のローカライズ ソリューションに、規制と競合の両方の機能が含まれている場合、ローカライズ ISV ソリューション プロバイダーはソリューションを各機能タイプごとに別々のモデルに分割する必要があります。 この記事では、この要件に関する情報を提供します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: shylaw
ms.search.scope: Operations
ms.custom: 27561
ms.assetid: 49b634ab-d7f7-4e34-a7e9-7350548bf1a0
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b94a8eb9ee319286dc203201611b3f5151f24f53
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368913"
---
# <a name="separation-of-localization-models"></a>ローカライズ モデルの分離

[!include [banner](../includes/banner.md)]

ローカライズおよび翻訳向け LCS ソリューションの要件の一部として、以前のバージョンの Microsoft Dynamics 365 for Finance and Operations のローカライズ ソリューションに、規制と競合の両方の機能が含まれている場合、ローカライズ ISV ソリューション プロバイダーはソリューションを各機能タイプごとに別々のモデルに分割する必要があります。 この記事では、この要件に関する情報を提供します。

多国籍の顧客は、Finance and Operations を配置するすべての国/地域で法的な要求事項を遵守する必要があります。 同時に顧客はコード メンテナンスのコストを最小限に抑えたいと考えています。 したがって、以前のバージョンの Finance and Operations のローカリゼーション ソリューションに規制機能と競合機能の両方が含まれている場合、顧客が必要とする機能を採用して展開できるように、ソリューションを別々のモデルに分割する必要があります。 アプリケーション ファンデーションおよび Finance and Operations スタックのアプリケーション スイートを複数のモデルに分割する努力がなされています。 

時間の経過とともにモデルの数は増加すると予想されます。 モノシリック コード ベースを分割すると、スケーラビリティ、管理性、および保守性の向上など、多くの利点が提供されます。 ローカライズ ソリューションをより詳細なモデルに分割するためのローカライズ要件は、この作業に基づいています。 目標は、Finance and Operations の多国籍の顧客に同じ利益を提供することです。 

機能を規制または競争のいずれかに分類した後、[ローカライズ機能の分類](classify-localization-features.md) で説明せれているように、これらの機能のコードを少なくとも 2 つのモデルに分割し、1 つのモデルは規制機能のため、また少なくとも 1 つのモデルは競合機能となります。 競合機能をさらに分割することができる場合 (たとえば、小売に関連する機能や固定資産に関連する機能など)、分割することをお勧めします。 ただし、さらに分割する必要はありません。 Finance and Operations のスタックを複数のモデルに分割する方法の詳細については、[モデルの分割を理解する](../dev-tools/model-split.md) を参照してください。




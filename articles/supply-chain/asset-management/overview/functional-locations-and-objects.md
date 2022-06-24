---
title: 機能の場所と資産
description: この記事では、資産管理の機能的な場所と資産について説明します。 資産管理は、Dynamics 365 Supply Chain Management の資産およびメンテナンス ジョブを管理するための高度なモジュールです。
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 274e80136ee303af9d0fe5fd04095f575a345d19
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875658"
---
# <a name="functional-locations-and-assets"></a>機能の場所と資産

[!include [banner](../../includes/banner.md)]

 

この記事では、資産管理の機能的な場所と資産について説明します。 資産管理は、Dynamics 365 Supply Chain Management の資産およびメンテナンス ジョブを管理するための高度なモジュールです。

## <a name="overview"></a>概要

資産管理は、Finance and Operations アプリでいくつかのモジュールとシームレスに統合されています。 次の図は、他のモジュールとのインターフェイスを示しています。

![他のモジュールとの資産管理インターフェイスを示す図。](media/01-overview-image.png)

資産管理を使用すると、社内のさまざまな種類の設備の管理とサービスに関連するすべてのタスクを効率的に管理および実行できます。 この設備には、機械、生産施設、および車両が含まれます。 資産管理は、さまざまな業界にわたるソリューションもサポートしています。

次の図は、資産管理で対象となる主な機能の概要を示しています。

![資産管理の主要機能を示す図。](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>機能の場所と資産

機能的な場所は、場所にある資産を管理するために使用されます。 この管理には、機能的な場所の資産原価の追跡が含まれます。 機能的な場所は階層構造で、場所はサブの場所を持つことができます。 機能的な場所の構造は静的です。 つまり、場所を変更することはできません。 資産は機能的な場所に導入でき、必要に応じて、後で他の機能的な場所に導入することができます。

資産原価は、常に資産の場所に従います。 つまり、新しい機能的な場所に資産を導入すると、その資産は新しい機能的な場所に関連する財務分析コードを自動的に使用します。 したがって、資産原価は、常に資産が現在導入されている機能的な場所に関連付けられています。 財務分析コードのこの自動処理は、会社が機能的な場所に関するプロジェクト管理とレポートを行う際に、コストの完全な追跡をするのに役立ちます。

機能的な場所の階層を構築する方法は、内部設備の管理や顧客設備の管理に関する会社の要件によって異なります。 次の図は、地理的な場所に基づく機能的な場所の例を示しています。

![地理的な場所に基づく機能上の場所を示す図。](media/03-overview-image.png)

次の図は、顧客に基づく機能的な場所の例を示しています。

![顧客に基づく機能上の場所を示す図。](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: 顧客レコードが Commerce 本社に表示されない
description: この記事では、顧客レコードがすぐに Commerce headquarters に表示されない場合に役立つトラブルシューティング ガイドを提供します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: f1ad1f45abbc95cbf6d41b3c8681db781c6c9d23
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268841"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>顧客レコードが Commerce 本社に表示されない

[!include [banner](../../includes/banner.md)]

この記事では、顧客レコードがすぐに Commerce headquarters に表示されない場合に役立つトラブルシューティング ガイドを提供します。

## <a name="description"></a>説明

電子商取引店舗のサインアップ フローを使用して新しい顧客レコードを作成する場合、対応する顧客レコードが Commerce 本社にすぐに表示されるわけではありません。

## <a name="resolution"></a>解像度

### <a name="disable-customer-creation-in-async-mode"></a>非同期モードでの顧客作成の無効化

> [!IMPORTANT]
> 非同期の顧客作成を無効にすると、各レコードの作成によって Commerce 本社へのリアルタイムの要求が生成されるため、システム パフォーマンスに影響を与える可能性があります。 さらに、Commerce 本社がダウンしている場合 (たとえばサービス フロー中)、新しい顧客作成フローではエラーが発生します。

Commerce 本社で非同期モードでの顧客作成を無効にするには、次の手順を実行します。

1. **Retail と Commerce \> チャネル設定 \> オンライン ストアの設定 \> 機能プロファイル** の順に移動します。
1. オンライン チャネルの機能プロファイルをまだ使用していない場合は、それを作成します。
1. **非同期モードで顧客を作成** オプションが **いいえ** に設定されていることを確認してください。
1. **Retail と Commerce \> チャネル \> オンライン ストア** に移動します。
1. 非同期顧客作成を無効にするオンライン ストアを選択します。
1. **一般** タブで、**機能プロファイル** フィールドがオンライン チャネルに使用している機能プロファイルに設定されていることを確認します。

## <a name="additional-resources"></a>追加リソース

[Commerce での B2C テナントの設定](../set-up-b2c-tenant.md)

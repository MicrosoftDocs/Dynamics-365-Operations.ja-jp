---
title: 非同期顧客を同期顧客に変換する
description: この記事では、Microsoft Dynamics 365 Commerce で非同期顧客を同期顧客に変換する方法について説明しています。
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: b442bfc0685706359771e4d9e2729565d3652a60
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278195"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>非同期顧客を同期顧客に変換する

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で非同期顧客を同期顧客に変換する方法について説明しています。

非同期顧客を同期顧客に変換する方法については、以下の手順に従います。

1. Commerce 本部で **P ジョブ** を実行し、非同期の顧客を Commerce 本部に送信します。
1. **非同期モードから顧客とビジネス パートナーを同期する** ジョブを実行して、顧客 ID を作成します。 (このジョブの旧名称は、**同期モードから顧客とビジネス パートナーを同期する** です。)
1. **1010** ジョブを実行して、新しい顧客 ID をチャネルに同期します。

注文が、Commerce 本部にまだ同期されていない非同期の顧客または住所を参照する場合、顧客または住所は **注文の同期** バッチジョブの一部として同期されます。 キャッシュ アンド キャリー取引が非同期の顧客またはアドレスを参照する場合、顧客またはアドレスは、営業終了 (EOD) 転記のに同期されます。

## <a name="additional-resources"></a>追加リソース

[店舗内の顧客管理](customer-mgmt-stores.md)

[顧客作成モードを非同期化する](async-customer-mode.md)

[顧客属性](dev-itpro/customer-attributes.md)

[オフライン データの除外](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)

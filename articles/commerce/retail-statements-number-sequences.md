---
title: 小売明細書の番号順序を設定する
description: この記事では、Microsoft Dynamics 365 Commerce で小売明細書に必要な番号順序を構成する方法について説明します。
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 5c4eb872ec2151a9f4ac5462ad43dd03a6705487
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880006"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>小売明細書の番号順序を設定する

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で小売明細書に必要な番号順序を構成する方法について説明します。

Dynamics 365 Commerce で使用される 2 種類の小売明細書: 

- **トランザクション明細書は**、作成および高頻度で転記することを目的とします。 店舗内の財務以外のすべてのトランザクションを Dynamics 365 Commerce 本社へ転記するために使用されます。 
- **財務明細書**、1 日あたり 1 回作成して転記することを目的とします。 このシフトには、p- ジョブを通じて Commerce 本社にアップロードされた小売店舗のクローズ済シフトだけが含まれます。

## <a name="configure-a-number-sequence-for-statement-posting"></a>明細書転記の番号シーケンスのコンフィギュレーション

Commerce 本社で小売店舗の設定を完了したら、明細書の作成プロセス中に明細書に使用する固有の番号順序を構成する必要があります。

Commerce で明細書転記の番号シーケンスを構成するには、次の手順を実行します。

1. **組織管理 \> 番号順序 \> 番号順序** の順に移動します。
1. **新しい \> 新しいシーケンス** を選択し、新しい記録を作成します。
1. **番号シーケンス コード** フィールドの **ID** クイックタブで、番号シーケンス コードを入力します。
1. **番号シーケンス名** フィールドで、名前を入力します。
1. **スコープ** フィールドの **スコープ パラメーター** クイック タブで、**作業単位** を選択します。
1. **作業単位** フィールドで、番号シーケンスが使用される添付を選択します。
1. **セグメント** クイックタブで、セグメントを定義します。
1. **参照** クイックタブで、**エリア** フィールドを **小売店舗** に設定します。
1. **参照** フィールドを **明細書番号** に設定し、**OK** を選択します。

    ![番号シーケンス ページの ID、スコープ パラメータ、セグメント、および参照クイックタブ。](media/retail-statements-num-seq-setup-01.png)

1. **番号割り当て** セクションの **一般** クイックタブで、**最小** と **最大** フィールドを更新すると、**セグメント** クイックタブで定義された **英数字** セグメントの長さに一致します。
1. **パフォーマンス** クイックタブで、**事前割り当て** オプションを **はい** に、**番号の数量** フィールドを **25** に設定することをお勧めします。

    ![番号シーケンス ページの一般およびパフォーマンス クイックタブ。](media/retail-statements-num-seq-setup-02.png)

1. アクション ウィンドウで、**保存** を選択し、変更を保存およびページを閉じます。

---
title: 追加の場所ゾーン
description: この記事では、Microsoft Dynamics 365 Supply Chain Management に追加された新しい場所ゾーンの概要を示します。
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 819330e0f6e6cd419da441f919d68ff996b6475c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336518"
---
# <a name="additional-location-zones"></a>追加の場所ゾーン

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management では、3 つの新しいゾーン フィールドを使用できます。 倉庫管理者は、これらを使用して追加の倉庫組織またはレイアウトを定義できます。 新しいゾーン フィールドは、手動で設定するか、または **場所設定** ウィザードを使用して設定できます。 これらは、場所テーブルを使用する任意のクエリまたはフィルター処理で使用できます。

ゾーン フィールドを使用するための追加の設定は必要ありません。

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>追加の場所ゾーン機能のオン/オフ

この機能を使用するには、システムでオンにする必要があります。 Supply Chain Management バージョン 10.0.25 では、この機能は既定で有効になっています。 Supply Chain Management バージョン 10.0.29 では、この機能は必須であり、オフにすることはできません。 10.0.29 より前のバージョンを使用している場合、管理者は [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースで *追加の場所のゾーン* 機能を検索して、この機能のオン/オフを切り替えることができます。

## <a name="use-location-zones"></a>場所ゾーンの使用

1. **倉庫管理 \> 設定 \> 倉庫 \> 場所設定ウィザード** に移動します。
2. 次の値を設定します。

    - **倉庫** フィールドで、_62_ を選択します。
    - **ゾーン ID** フィールドで、_FLOOR_ を選択します。
    - **追加ゾーン 1** フィールドで、_PICKZONE1_ を選択します。
    - **追加ゾーン 2** フィールドで、_WEBSHOP1_ を選択します。
    - **場所プロファイル ID** フィールドで、_FLOOR_ を選択します。

3. **フロア** 明細行を選択します。
4. **開始番号** フィールドに _1_ を入力します。 **終了番号** フィールドに _3_ を入力します。
5. **通路** 明細行を選択します。
6. **開始番号** フィールドに _1_ を入力します。 **終了番号** フィールドに _5_ を入力します。
7. **作成** を選択します。
8. 新しい場所が追加されたことを示すメッセージが表示されます。 メッセージを表示するには、**メッセージを表示する** のボタンを選択します。
9. **倉庫管理 \> 設定 \> 倉庫 \> 場所** に移動します。 新しい場所が一覧に表示され、すべてのゾーン フィールド (既存のゾーン フィールドと新しい追加ゾーン フィールド) が使用可能になります。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
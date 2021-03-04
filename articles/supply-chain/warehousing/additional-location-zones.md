---
title: 追加の場所ゾーン
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management に追加された新しい場所ゾーンの概要を示します。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4432329"
---
# <a name="additional-location-zones"></a>追加の場所ゾーン

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management では、3 つの新しいゾーン フィールドを使用できます。 倉庫管理者は、これらを使用して追加の倉庫組織またはレイアウトを定義できます。 新しいゾーン フィールドは、手動で設定するか、または **場所設定** ウィザードを使用して設定できます。 これらは、場所テーブルを使用する任意のクエリまたはフィルター処理で使用できます。

ゾーン フィールドを使用するための追加の設定は必要ありません。

## <a name="turn-on-the-additional-location-zone-feature"></a>追加の場所ゾーン機能を有効にする

*追加の場所ゾーン* 機能を使用するには、システム上で有効にする必要があります。 管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。 **機能管理** ワークスペースで、この機能は次のようにリストされています。

- **モジュール:** *倉庫管理*
- **機能名:** *追加の場所ゾーン*

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
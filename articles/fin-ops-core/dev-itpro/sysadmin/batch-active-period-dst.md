---
title: 有効なバッチ期間における夏時間のサポート
description: このトピックでは、有効なバッチ期間における夏時間のサポートに関する情報を提供します。
author: karimelazzouni
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.custom: NotInToc
ms.assetid: a6685c6f-74bf-4f09-a19d-76130d7ce2da
ms.search.region: Global
ms.author: kaelazzo
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: 4b82b1ecb8b4e16b27911e0e2aee17fdf7ab96bfa9ad0d14044473b817580f28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729692"
---
# <a name="daylight-saving-time-support-for-active-batch-periods"></a>有効なバッチ期間における夏時間のサポート

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finance バージョン 10.0.12 には、[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md)で有効にできる、**バッチ ジョブの有効期間における夏時間のサポート** 機能が含まれています。 この機能を使用すると、[バッチ ジョブの有効な期間](activeperiod.md)における夏時間 (DST) のサポートが導入され、ユーザーはそれぞれの有効期間を異なるタイムゾーンに関連付けることができます。

> [!NOTE] 
> この機能は一方向の機能です。 つまり、電源をオンにした後にオフにすることはできません。

この機能をオンにすると、次の変化が発生します。

- **バッチ ジョブの有効期間** ページで、有効な期間ごとに **タイムゾーン** フィールドが追加されます。 このフィールドでは、有効な期間が使用するタイムゾーンを指定します。 既定では、有効なすべての期間において、世界協定時刻 (UTC) タイムゾーンが最初に使用されます。

    ![バッチ ジョブの有効期間ページのタイムゾーン フィールド。](./media/active-periods-dst.png)

- 既存の有効期間の開始時刻と終了時刻は、UTC タイムゾーンに従って調整されます。 有効期間は、以前の開始と終了と同じ時刻に開始および終了しますが、ユーザーの優先タイムゾーンが UTC ではない場合は、表示される時間が変わる可能性があります。
- 有効期間は、関連付けられているタイムゾーンの夏時間調整に従います。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
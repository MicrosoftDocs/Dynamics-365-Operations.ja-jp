---
title: 場所プロファイルではマイナス在庫は許可されませんが、マイナス手持ち在庫は許可されます
description: 場所プロファイルの [マイナス在庫を許可] オプションは [いいえ] に設定されていますが、マイナス手持ち在庫は許容されたままになります。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026675"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>場所プロファイルではマイナス在庫は許可されませんが、マイナス手持ち在庫は許可されます

KB 番号: 4613622

## <a name="symptoms"></a>現象

場所プロファイルの **マイナス在庫を許可** オプションは *いいえ* に設定されていますが、マイナス手持ち在庫は許容されたままになります。

## <a name="example-scenario"></a>シナリオ例

政府が規制したトランザクションの場合、システムはマイナス在庫を帳損に記録できる必要があります。 品目は、マイナスの在庫を指定した場所 (変更可能な場所など) にのみ表示可能にする。 ただし、品目モデル グループでマイナス在庫が許可されている場合、場所がマイナス在庫を許可するよう設定されているかどうかは関係ありません。 マイナス在庫を許可しないよう品目が設定されている場合、場所プロファイルの設定方法は関係ありません。

## <a name="resolution"></a>解像度

場所プロファイルの **マイナス在庫を許可** 設定は、ピッキングなどの倉庫プロセスにのみ適用されます。 ただし、マイナス在庫を許可するよう設定された品目モデル グループは、在庫管理モジュールおよび倉庫管理モジュールのすべてのプロセスに影響します。場所プロファイルは、この設定を上書きしません。

倉庫でマイナス在庫を保管できるかどうかを制御できます。 品目モデル グループがマイナス在庫を許可しないよう設定し、マイナス在庫を許可するには関連倉庫のみを設定します。

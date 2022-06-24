---
title: サービス期間の設定
description: この記事では、サービス期間の設定方法について説明します。 サービス間隔は、サービス注文を作成する場合に、サービス契約項目に対してサービス注文明細行が作成される頻度を表します。
author: sorenva
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b8a31af061b90aeddfb460f6e86c2c5636b280
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845956"
---
# <a name="set-up-service-intervals"></a>サービス期間の設定  

[!include [banner](../includes/banner.md)]

サービス間隔は、サービス注文を作成する場合に、サービス契約項目に対してサービス注文明細行が作成される頻度を表します。

1. **サービス管理** \> **設定** \> **サービス契約** \> **サービス期間** の順にクリックします。
2. 新しいサービス期間を作成します。
3. サービス期間の ID と説明を入力します。
4. **範囲** フィールドで範囲を選択します。
5. **頻度** フィールドに、頻度をタイプします。 サービス契約の期間を算出するには、この頻度を係数として範囲と掛け合わせます。
6. **Alt + S** キーを押してサービス期間を保存します。

## <a name="example"></a>例

10 日間のサービス期間を作成するとします。

**10 日間のサービス期間の作成**

1. **サービス管理** \> **設定** \> **サービス契約** \> **サービス期間** の順にクリックします。
2. 新しいサービス期間を作成します。
3. サービス期間の ID と説明を入力します。
4. **範囲** フィールドで **毎日** を選択します。
5. **頻度** フィールドに 10 を入力します。
6. **Alt + S** キーを押してサービス期間を保存します。

## <a name="related-articles"></a>関連記事

[サービス期間](service-intervals.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
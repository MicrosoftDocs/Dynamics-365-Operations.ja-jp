---
title: サービス期間の設定
description: サービス間隔は、サービス注文を作成する場合に、サービス契約項目に対してサービス注文明細行が作成される頻度を表します。
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54eba378548e1bef8ae9c3f4e7b202cf06aeff2d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431638"
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

## <a name="related-topics"></a>関連トピック

[サービス期間](service-intervals.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
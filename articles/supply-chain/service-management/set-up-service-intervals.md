---
title: "サービス期間の設定"
description: "サービス間隔は、サービス注文を作成する場合に、サービス契約項目に対してサービス注文明細行が作成される頻度を表します。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: 03ebf4fd4615eac77e6f990a2d4e7f7326c0d257
ms.contentlocale: ja-jp
ms.lasthandoff: 02/20/2018

---

# <a name="set-up-service-intervals"></a>サービス期間の設定  

[!include [banner](../includes/banner.md)]

サービス間隔は、サービス注文を作成する場合に、サービス契約項目に対してサービス注文明細行が作成される頻度を表します。

1. **サービス管理** \> **設定** \> **サービス契約** \> **サービス期間**の順にクリックします。
2. 新しいサービス期間を作成します。
3. サービス期間の ID と説明を入力します。
4. **範囲** フィールドで範囲を選択します。
5. **頻度** フィールドに、頻度をタイプします。 サービス契約の期間を算出するには、この頻度を係数として範囲と掛け合わせます。
6. **Alt + S** キーを押してサービス期間を保存します。

## <a name="example"></a>例

10 日間のサービス期間を作成するとします。

**10 日間のサービス期間の作成**

1. **サービス管理** \> **設定** \> **サービス契約** \> **サービス期間**の順にクリックします。
2. 新しいサービス期間を作成します。
3. サービス期間の ID と説明を入力します。
4. **範囲** フィールドで **毎日**を選択します。
5. **頻度** フィールドに 10 を入力します。
6. **Alt + S** キーを押してサービス期間を保存します。

## <a name="related-topics"></a>関連トピック

[サービス期間](service-intervals.md)  


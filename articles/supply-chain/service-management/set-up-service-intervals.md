---
title: サービス期間の設定
description: このトピックでは、サービス期間の設定方法について説明します。 サービス間隔は、サービス注文を作成する場合に、サービス契約項目に対してサービス注文明細行が作成される頻度を表します。
author: kamaybac
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0aeaef9fcf0c909638a9452633a321121e20814
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567850"
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
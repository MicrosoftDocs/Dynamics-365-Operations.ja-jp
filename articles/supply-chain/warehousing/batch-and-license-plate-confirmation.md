---
title: バッチおよびライセンス プレートの確認
description: このトピックでは、モバイル デバイスからバッチおよびライセンス プレートの確認を設定して適用する方法について説明します。
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efab5b11782fd2344fb5f532272007d187c1465b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563917"
---
# <a name="batch-and-license-plate-confirmation"></a>バッチおよびライセンス プレートの確認

[!include [banner](../includes/banner.md)]

バッチの確認では、適切なバッチがピッキングされていることをモバイル デバイスから確認することができます。 上の品目のみのバッチ作業の最初のピッキング時、上のバッチの表示は、検索階層内のバッチ範囲の場所を超えることを示し、ピッキングされているバッチが作業明細行のバッチと一致していることを確認する必要があります。 

ライセンス プレートの確認では、適切なライセンス プレートがピッキングされていることをモバイル デバイスから確認することができます。 ステージの場所からのピッキング作業時に、ピッキングされるライセンス プレートが作業に関連付けられているライセンス プレートと一致していることを確認する必要があります。 ライセンス プレートをスキャンして作業を起動する場合、この確認手順はスキップされます。

## <a name="where-it-applies"></a>該当する場合
確認は、以下のシナリオで適用されます。

- バッチ確認は、上の品目のバッチ作業の最初のピッキング時に適用されます。
- ライセンス プレートの確認は、ステージの場所からのピッキングに適用されます。

## <a name="set-up-batch-and-license-plate-confirmation"></a>バッチおよびライセンス プレートの確認の設定
モバイル デバイスのメニュー項目から、バッチとライセンス プレートの確認をコンフィギュレーションできます。  
1.  モバイル デバイス メニュー項目から、[作業確認の設定] に進みます。  
2.  バッチの確認またはライセンス プレートの確認のどちらかのオプションを選択します。 自動確認が有効でない作業タイプのピッキングでは、両方のオプションが有効です。  

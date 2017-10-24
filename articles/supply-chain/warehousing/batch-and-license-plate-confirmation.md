---
title: "バッチおよびライセンス プレートの確認"
description: "このトピックでは、モバイル デバイスからバッチおよびライセンス プレートの確認を設定して適用する方法について説明します。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6454335989fe03a7332b6fb956667850896ffaf4
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="batch-and-license-plate-confirmation"></a>バッチおよびライセンス プレートの確認

[!include[banner](../includes/banner.md)]

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


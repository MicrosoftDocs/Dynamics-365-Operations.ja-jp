---
title: バッチおよびライセンス プレートの確認
description: この記事では、モバイル デバイスからバッチおよびライセンス プレートの確認を設定して適用する方法について説明します。
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef0d528d23c1ee9424e35e29d39121d42ba548e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903727"
---
# <a name="batch-and-license-plate-confirmation"></a>バッチおよびライセンス プレートの確認

[!include [banner](../includes/banner.md)]

バッチの確認では、適切なバッチがピッキングされていることをモバイル デバイスから確認することができます。 *上記バッチ\[ロケーション\]* のみのバッチ作業の最初のピッキング時、上のバッチの表示は、検索階層内のバッチ範囲の場所を超えることを示し、ピッキングされているバッチが作業明細行のバッチと一致していることを確認する必要があります。

ライセンス プレートの確認では、適切なライセンス プレートがピッキングされていることをモバイル デバイスから確認することができます。 ステージの場所からのピッキング作業時に、ピッキングされるライセンス プレートが作業に関連付けられているライセンス プレートと一致していることを確認する必要があります。 ライセンス プレートをスキャンして作業を起動する場合、この確認手順はスキップされます。

## <a name="where-it-applies"></a>該当する場合

確認は、以下のシナリオで適用されます。

- バッチ確認は、上の品目のバッチ作業の最初のピッキング時に適用されます。
- ライセンス プレートの確認は、ステージの場所からのピッキングに適用されます。

> [!IMPORTANT]
> 補充は、ライセンス プレートの確認ではサポートされていません。 補充作業を実行している場合は、ライセンス プレートの確認ステップは作成されません。

## <a name="set-up-batch-and-license-plate-confirmation"></a>バッチおよびライセンス プレートの確認の設定

モバイル デバイスのメニュー項目から、バッチとライセンス プレートの確認をコンフィギュレーションできます。

1. モバイル デバイス メニュー項目から、[作業確認の設定] に進みます。  
1. バッチの確認またはライセンス プレートの確認のどちらかのオプションを選択します。 自動確認が有効でない作業タイプのピッキングでは、両方のオプションが有効です。  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

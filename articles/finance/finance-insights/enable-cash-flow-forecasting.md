---
title: キャッシュ フロー予測の有効化
description: このトピックでは、財務インサイトでキャッシュ フロー予測機能を有効にする方法について説明します。
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: cfcdbe76d640d1786b4622febf9157f5fb1c42f9
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/13/2022
ms.locfileid: "7969140"
---
# <a name="enable-cash-flow-forecasting"></a>キャッシュ フロー予測の有効化

[!include [banner](../includes/banner.md)]

このトピックでは、Finance Insights でキャッシュ フロー予測機能を有効にする方法について説明します。

> [!NOTE]
> キャッシュ フローで支払予測を使用するには、[顧客支払予測の有効化](enable-cust-paymnt-prediction.md) で説明されているように、顧客支払予測機能を設定する必要があります。
  
1. **機能管理** ワークスペースを開き、次の手順に従います:

    1. **更新プログラムの確認** を選択します。
    2. **すべて** タブで、**キャッシュ フロー予測** を検索します。 その機能が見つらない場合は、**(プレビュー) キャッシュ フロー予測** を検索します。 
    3. 機能をオンにします。

2. **現金および銀行管理 \> キャッシュ フロー予測の設定** に移動し、予測に含める流動資産勘定を追加します。 また、**売掛金勘定** タブと **買掛金勘定** タブの支払の流動資産勘定も設定します。 キャッシュ フロー予測は、必ず再計算してください。

    > [!NOTE]
    > 流動資産勘定が設定されていない場合は、キャッシュ フローを生成できません。
    >
    > キャッシュ フロー予測の設定方法の詳細については、[キャッシュ フロー予測](../cash-bank-management/cash-flow-forecasting.md)を参照してください。

3. **現金および銀行管理 \> 設定 \> 財務インサイト (プレビュー) \> キャッシュ フロー予測** に移動し、次の手順を実行します:

    1. **キャッシュ フロー予測** タブで、**機能の有効化** を選択します。
    2. **予測モデルの作成** を選択します。

キャッシュ フロー予測機能の詳細については、[キャッシュ フロー予測](cash-flow-forecast-intro.md) を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

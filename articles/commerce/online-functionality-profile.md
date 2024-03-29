---
title: オンライン機能プロファイルの作成
description: この記事では、Microsoft Dynamics 365 Commerce でオンライン機能プロファイルを作成する方法について説明します。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 5ce81900cd0648132748167d03906afc64e97f25
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276804"
---
# <a name="create-an-online-functionality-profile"></a>オンライン機能プロファイルの作成

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce のオンライン機能プロファイルの設定の概要を示します。

オンライン機能プロファイルは、オンライン チャネルに使用されるさまざまな設定を提供します。 各オンライン チャネルでは、オンライン機能プロファイルを指定する必要があります。

## <a name="create-an-online-functionality-profile"></a>オンライン機能プロファイルの作成

次の手順では、Commerce Headquarters アプリからオンライン機能プロファイルを作成する方法について説明します。

1. ナビゲーション ウィンドウで、**モジュール \> チャネル設定 \> オンライン ストア設定 \> 機能プロファイル** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **プロファイル** フィールドに、プロファイルの ID を入力します。
1. **説明** フィールドに、値を入力します (以下のサンプル画像の "Adventure Works プロファイル")。
1. **機能** セクション **カート**、**小売顧客**、または **チェックアウト** 設定を必要に応じて変更します。
1. アクション ウィンドウで、**保存** を選択します。

次の図は、オンライン機能プロファイルの例を示しています。
  
![オンライン機能プロファイルの例。](media/online-functionality-profile.png)

## <a name="functions"></a>関数

- **製品の集計**: この機能を有効にすると、同じ品目が複数回追加された場合に、カートで数量を更新できるようになります。
- **支払なしのチェックアウトを許可**: この機能を有効にすると、カートに追加された品目の価格が $0.00 になったときに、このシナリオが処理されます。
- **非同期モードで顧客を作成する**: これは、サードパーティの E コマース チャネルに適用されるレガシ設定であり、Dynamics 365 E コマース サイトには適用できません。

## <a name="additional-resources"></a>追加リソース

[チャネルの概要](channels-overview.md)

[チャネル設定の前提条件](channels-prerequisites.md)

[オンライン チャネルの設定](channel-setup-online.md)

[小売チャネルの設定](channel-setup-retail.md)

[コール センターのチャネルの設定](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: 小売機能プロファイルの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce に機能プロファイルを作成する方法について説明します。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 84423e1a7cf90cc6427e7e42005f52417abff091
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345059"
---
# <a name="create-a-retail-functionality-profile"></a>小売機能プロファイルの作成

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce に機能プロファイルを作成する方法について説明します。

コマース機能プロファイルは、オンライン チャネルに使用されるさまざまな設定を提供します。 各チャネルでは、機能プロファイルを指定する必要があります。

## <a name="create-a-functionality-profile"></a>機能プロファイルの作成

機能プロファイルを作成するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> チャネル設定 \> POS プロファイル \> 機能プロファイル** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **プロファイル** フィールドで、プロファイルの ID を入力します (以下のサンプル画像の "FN006")。
1. **説明** フィールドに、値を入力します (以下のサンプル画像の "Adventure Works プロファイル")。
1. **全般** セクションで、**ISO** ロケールの国を選択します。
1. **全般** セクションで、必要に応じてその他の設定を変更します。
1. **全般** セクションで、電子メール レシートの **レシート プロファイル ID** を選択します。
1. **機能** セクションで、必要に応じて設定を変更します。
1. **金額** セクションで、必要に応じて設定を変更します。
1. **情報コード** セクションで、必要に応じて設定を変更します。
1. **レシート番号** セクションで、必要に応じて設定を変更します。 
  
次の図は、機能プロファイルの例を示しています。
  
![機能プロファイルの例。](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>追加リソース

[情報コードおよび情報コード グループ](info-codes-retail.md)           

[新しいアドレス帳の作成](new-address-book.md) 

[画面レイアウトの概要](pos-screen-layouts.md)       

[Retail Hardware Station のコンフィギュレーションおよびインストール](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

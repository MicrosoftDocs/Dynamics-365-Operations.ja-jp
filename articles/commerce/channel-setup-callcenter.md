---
title: コール センターのチャネルの設定
description: このトピックでは、Microsoft Dynamics 365 Commerce に新しいコール センター チャネルを作成する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002453"
---
# <a name="set-up-a-call-center-channel"></a>コール センターのチャネルの設定


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce に新しいコール センター チャネルを作成する方法について説明します。

## <a name="overview"></a>概要

Dynamics 365 Commerce では、コール センターはアプリケーションで定義できる小売チャネルのタイプです。 コール センター エンティティのチャネルを定義すると、システムによって特定のデータと注文処理の既定値を販売注文に関連付けることができます。 会社では、Commerce の複数のコール センター チャネルを定義できます。 

新しいコール センター チャネルを作成する前に、[チャネル設定の前提条件](channels-prerequisites.md) を完了していることを確認してください。

## <a name="create-and-configure-a-new-call-center-channel"></a>新しいコール センター チャネルを作成およびコンフィギュレーションする

新しいコール センター チャネルを作成してコンフィギュレーションするには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> チャネル \> コール センター \> すべてのコール センター**の順に移動します。
1. アクション ウィンドウで、**新規**を選択します。
1. **名前**フィールドで、新しいチャネルの名前を指定します。
1. ドロップ ダウンから適切な**法人**を選択します。
1. ドロップ ダウンから適切な**倉庫**の場所を選択します。
1. **既定の顧客**フィールドで、有効な既定の顧客を指定します。
1. **電子メール通知プロファイル** フィールドに、有効な電子メール通知プロファイルを指定します。
1. **価格上書き**の情報コードを指定します。 このために、最初に情報コードを作成する必要があることに注意してください。
1. **保留コード**の情報コードを指定します。 このために、最初に情報コードを作成する必要があることに注意してください。
1. **クレジット**の情報コードを指定します。 このために、最初に情報コードを作成する必要があることに注意してください。
1. **保存** を選択します。

次の図は、新しいコール センター チャネルの作成を示しています。

![新しいコール センター チャネル](media/channel-setup-callcenter-1.png)

次の図は、コール センター チャネルの例を示しています。

![コール センター チャネルの例](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>追加のチャネル設定

コール センター チャネルの設定に必要な追加タスクには、支払方法および荷渡方法の設定が含まれています。

次の図は、**設定**タブの**荷渡方法**および**支払方法**の設定オプションを示しています。

![追加のコール センター チャネル設定アクション](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>支払方法の設定

支払方法を設定するには、このチャネルでサポートされている各支払タイプに対して、次の手順に従います。

1. アクション ウィンドウで、**設定**タブを選択して、**支払方法**を選択します。
1. アクション ウィンドウで、**新規**を選択します。
1. ナビゲーション ウィンドウで、目的の支払方法を選択します。
1. **全般**セクションで、**操作名**を指定し、その他の必要な設定を構成します。
1. 支払タイプに必要に応じて追加の設定を構成します。
1. アクション ウィンドウで、**保存**を選択します。

次の図は、現金支払い方法の例を示しています。

![支払方法の例](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>荷渡方法の設定

構成されたデリバリー モードは、**アクション ウィンドウ**の**設定**タブで**デリバリー モード**を選択することによって確認できます。  

デリバリー モードを変更または追加するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> 在庫管理 \> デリバリー モード**に移動します。
1. アクション ウィンドウで、**新規**を選択して新しいデリバリー モードを作成するか、既存のモードを選択します。
1. **小売チャネル** セクションで、**行の追加**を選択してチャネルを追加します。 各チャネルを個別に追加する代わりに、組織ノードを使用してチャネルを追加すると、チャネルの追加を効率化できます。

次の図は、デリバリー モードの例を示しています。

![荷渡方法の設定](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a>追加リソース

[チャネル設定の前提条件](channels-prerequisites.md)

[コール センターの販売機能](call-center-functionality.md)

[コール センターの注文処理オプションの設定](set-up-order-processing-options.md)

[コール センターのカタログ](call-center-catalogs.md)

[詐欺警告の設定および使用](set-up-fraud-alerts.md)

[コール センターの連続プログラムの設定](set-up-continuity-program.md)

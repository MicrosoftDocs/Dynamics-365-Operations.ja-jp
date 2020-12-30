---
title: オンライン チャネルの設定
description: このトピックでは、Microsoft Dynamics 365 Commerce に新しいオンライン チャネルを作成する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 07/02/2020
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
ms.openlocfilehash: 07225d97af76ea665fa28362cc205c6e8dc4fdf4
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2020
ms.locfileid: "4413904"
---
# <a name="set-up-an-online-channel"></a>オンライン チャネルの設定


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce に新しいオンライン チャネルを作成する方法について説明します。

## <a name="overview"></a>概要

Dynamics 365 Commerce は複数の小売チャンネルをサポートします。 これらの小売チャンネルには、オンライン ストア、コール センター、および小売用店舗 (従来型の店舗とも呼ばれる) が含まれます。 オンライン ストアは、小売店舗に加えて小売業者のオンライン ストアから製品を購入するオプションを顧客に提供します。

Commerce でオンライン ストアを作成するには、最初にオンライン チャネルを作成する必要があります。 新しいオンライン チャネルを作成する前に、[チャネル設定の前提条件](channels-prerequisites.md) を完了していることを確認してください。

新しいサイトを作成する前に、少なくとも 1 つのオンライン ストアをコマースで作成する必要があります。 詳細については、[E コマース サイトの作成](create-ecommerce-site.md)を参照してください。

## <a name="create-and-configure-a-new-online-channel"></a>新しいオンライン チャネルを作成およびコンフィギュレーションする

新しいオンライン チャネルを作成してコンフィギュレーションするには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> チャネル \> オンライン ストア** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **名前** フィールドで、新しいチャネルの名前を指定します。
1. **法人** ドロップダウンで、適切な法人を入力します。
1. **倉庫** ドロップダウンで、適切な倉庫を入力します。
1. **店舗タイム ゾーン** フィールドで、適切なタイム ゾーンを選択します。
1. **通貨** フィールドで、適切な通貨を選択します。
1. **既定の顧客** フィールドで、有効な既定の顧客を指定します。
1. **顧客アドレス帳** フィールドで、有効なアドレス帳を指定します。
1. **機能プロファイル** フィールドで、該当する場合は機能プロファイルを選択します。
1. **電子メール通知プロファイル** フィールドに、有効な電子メール通知プロファイルを指定します。
1. アクション ウィンドウで、**保存** を選択します。

次の図は、新しいオンライン チャネルの作成を示しています。

![新しいオンライン チャネル](media/channel-setup-online-1.png)

次の図は、オンライン チャネルの例を示しています。

![オンライン チャネルの例](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a>言語の設定

E コマース サイトで複数の言語をサポートする場合は、**言語** セクションを展開し、必要に応じて追加の言語を追加します。

## <a name="set-up-payment-account"></a>支払勘定の設定

**支払勘定** セクション内から、サードパーティの支払プロバイダーを追加できます。 Adyen 支払コネクタ設定の詳細については、[Adyen 向け Dynamics 365 Payment Connector](../retail/dev-itpro/adyen-connector.md) を参照してください。

## <a name="additional-channel-setup"></a>追加のチャネル設定

オンライン チャネルの設定に必要な追加タスクには、支払方法、荷渡方法、およびフルフィルメント グループの割り当ての設定が含まれています。

次の図は、**設定** タブの **荷渡方法**、**支払方法**、および **フルフィルメント グループの割り当て** の設定オプションを示しています。

![追加のオンライン チャネル設定アクション](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>支払方法の設定

支払方法を設定するには、このチャネルでサポートされている各支払タイプに対して、次の手順に従います。

1. アクション ウィンドウで、**設定** タブを選択し、**支払方法** を選択します。
1. アクション ウィンドウで、**新規** を選択します。
1. ナビゲーション ウィンドウで、目的の支払方法を選択します。
1. **全般** セクションで、**操作名** を指定し、その他の必要な設定を構成します。
1. 支払タイプに必要に応じて追加の設定を構成します。
1. アクション ウィンドウで、**保存** を選択します。

次の図は、現金支払い方法の例を示しています。

![支払方法の例](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>荷渡方法の設定

構成されたデリバリー モードは、**アクション ウィンドウ** の **設定** タブで **デリバリー モード** を選択することによって確認できます。  

デリバリー モードを変更または追加するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> 在庫管理 \> デリバリー モード** に移動します。
1. アクション ウィンドウで、**新規** を選択して新しいデリバリー モードを作成するか、既存のモードを選択します。
1. **小売チャネル** セクションで、**行の追加** を選択してチャネルを追加します。 各チャネルを個別に追加する代わりに、組織ノードを使用してチャネルを追加すると、チャネルの追加を効率化できます。

次の図は、デリバリー モードの例を示しています。

![荷渡方法の設定](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>フルフィルメント グループの割り当ての設定

フルフィルメント グループの割り当てを設定するには、次の手順に従います。

1. アクション ウィンドウで、**設定** タブを選択し、**フルフィルメント グループの割り当て** を選択します。
1. アクション ウィンドウで、**新規** を選択します。
1. **フルフィルメント グループ** ドロップダウン リストで、フルフィルメント グループを選択します。
1. **説明** ドロップダウン リストに、説明を入力します。
1. アクション ウィンドウで、**保存** を選択します。

次の図は、フルフィルメント グループの割り当ての設定の例を示しています。

![フルフィルメント グループの割り当ての設定](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>追加リソース

[チャネルの概要](channels-overview.md)

[チャネル設定の前提条件](channels-prerequisites.md)

[小売チャネルの設定](channel-setup-retail.md)

[コール センターのチャネルの設定](channel-setup-callcenter.md)

[Adyen 向け Dynamics 365 Payment Connector](../retail/dev-itpro/adyen-connector.md)

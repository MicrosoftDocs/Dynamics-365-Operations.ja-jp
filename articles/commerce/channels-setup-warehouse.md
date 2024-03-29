---
title: 倉庫の設定
description: この記事では、Microsoft Dynamics 365 Commerce で新しいチャネルと共に使用する倉庫の設定方法について説明します。
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
ms.openlocfilehash: 476f78d7fe1bc61c2c9b783ed1f82bc660248b02
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273642"
---
# <a name="warehouse-set-up"></a>倉庫の設定

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で新しいチャネルと共に使用する倉庫の設定方法について説明します。

各 Commerce チャネルには、関連付けられるコンフィギュレーション済みの倉庫が必要です。 次の手順では、Commerce チャネルの倉庫を設定するために最低限必要なコンフィギュレーションを提供します。 倉庫の設定に関する詳細については、[倉庫管理の概要](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)を参照してください。

## <a name="configure-a-warehouse-site"></a>倉庫サイトのコンフィギュレーション

倉庫を設定する前に、倉庫サイトをコンフィギュレーションする必要があります。

倉庫のサイトをコンフィギュレーションするには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> サイト** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **サイト** フィールドに値を入力します。
1. **名前** フィールドに値を入力します。
1. **一般** セクションで、適切な **タイム ゾーン** を設定します。
1. **住所** セクションに、住所を入力します。
1. アクション ウィンドウで、**保存** を選択します。

次の図は、倉庫サイトの例を示しています。

![倉庫サイトの例。](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>倉庫の設定

倉庫を設定するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 倉庫** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **倉庫** フィールドで値を入力します。  これが店舗への 1:1 マッピングである場合は、店舗名または地域の配送センターの名前を使用することを検討してください。
1. **名前** フィールドに値を入力します。
1. **サイト** ドロップダウン リストで、以前に作成した倉庫サイトを選択します。
1. **タイプ** フィールドで、**既定** を選択します。
    - **検査倉庫** を設定する場合は、最初に次の手順に従って、**タイプ** が **検査** に設定されている追加の倉庫を作成する必要があります。
    - **トランジット倉庫** を設定する場合は、最初に次の手順に従って、**タイプ** が **トランジット** に設定されている追加の倉庫を作成する必要があります。
1. アクション ウィンドウで、**保存** を選択します。

## <a name="set-up-inventory-aisles"></a>通路を設定します

在庫通路を設定するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 場所の設定 \> 在庫通路** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **倉庫** ドロップダウン リストで、以前に作成した倉庫を選択します。
1. **通路** フィールドに、名前を入力します (例: "Def")。
1. **名前** フィールドに、名前を入力します (例: "既定の通路")。
1. アクション ウィンドウで、**保存** を選択します。

## <a name="set-up-warehouse-inventory-locations"></a>倉庫の在庫場所の設定

標準、破損、および返品された在庫の倉庫の在庫場所を設定するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 倉庫** の順に移動します。
1. 以前に作成した倉庫を選択します。
1. アクション ウィンドウで、**編集** を選択します。
1. アクション ウィンドウで、**倉庫** を選択し、**在庫場所** を選択します。
1. アクション ウィンドウで、**新規** を選択します。 **倉庫** ドロップダウン リストには、既定で新しい倉庫を指定する必要があります。
    1. **通路** ボックスに、前に指定した通路の名前を入力します。 
    1. **手動更新** を **はい** に設定する
    1. **場所** ボックスに、倉庫の名前を入力します。
    1. アクション ウィンドウで、**保存** を選択します。
 1. アクション ウィンドウで、**新規** を選択します。  **倉庫** ドロップダウン リストには、既定で新しい倉庫を指定する必要があります。
    1. **通路** ボックスに、前に指定した通路の名前を入力します。  
    1. **手動更新** を **はい** に設定する
    1. **場所** ボックスに、「破損」と入力します。
    1. アクション ウィンドウで、**保存** を選択します。
 1. アクション ウィンドウで、**新規** を選択します。  **倉庫** ドロップダウン リストには、既定で新しい倉庫を指定する必要があります。
    1. **通路** ボックスに、前に指定した通路の名前を入力します。 
    1. **手動更新** を **はい** に設定する
    1. **場所** ボックスに、「返品」と入力します。
    1. アクション ウィンドウで、**保存** を選択します。
    
次の図は、サンフランシスコの倉庫在庫場所の設定を示しています。

![在庫場所の設定例。](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>倉庫の設定の完了

倉庫の設定を完了するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 倉庫** の順に移動します。
1. 以前に作成した倉庫を選択します。
1. アクション ウィンドウで、**編集** を選択します。
1. **在庫および倉庫管理** で:
    1. **既定の受入場所** を上記で作成した既定の場所に設定します。
    1. **既定の払出場所** を上記で作成した既定の場所に設定します。
1. **住所** セクションで、倉庫の住所を入力します。
1. **小売** セクションで: 
    1. **既定の返品場所** ボックスに、以前に作成した返品場所を入力します。
    1. **格納** を **はい** に設定します。
    1. **重量** を **1.00** に設定します。 
    1. **保管分析コード** ボックスに、以前に作成した既定の場所を入力します。
1. **倉庫** セクションで、**現物マイナス在庫** を **はい** に設定します。
1. アクション ウィンドウで、**保存** を選択します。

次の図は、コンフィギュレーション済倉庫の詳細を示しています。

![コンフィギュレーション済倉庫の例。](media/warehouse-sample.png)

## <a name="additional-resources"></a>追加リソース

[倉庫管理の概要](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[チャネルの概要](channels-overview.md)

[チャネル設定の前提条件](channels-prerequisites.md)

[小売チャネルの設定](channel-setup-retail.md)
    
[オンライン チャネルの設定](channel-setup-online.md)

[コール センターのチャネルの設定](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]

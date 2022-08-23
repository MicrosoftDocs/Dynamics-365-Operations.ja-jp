---
title: 組織階層へのチャネルの追加
description: この記事では、Microsoft Dynamics 365 Commerce の組織階層にチャネルを追加する方法について説明します。
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
ms.openlocfilehash: 9def2d7c3cf17ecd9b74ce41f56bc3220a754597
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278600"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>組織階層へのチャネルの追加


[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の組織階層にチャネルを追加する方法について説明します。

## <a name="overview"></a>概要

チャネルは、1 つ以上の組織階層に関連付けられている必要があります。 チャネルを作成する前に、組織階層が設定されていることを確認する必要があります。  

組織階層の作成方法に関する詳細は、[組織階層](channels-org-hierarchies.md) を参照してください。

## <a name="select-a-hierarchy"></a>階層の選択

階層を選択するには、次の手順を実行します。

1. ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 組織階層** の順に移動します。
1. リストから、チャネルを追加する組織階層を選択します。
1. アクション ウィンドウで、**表示** を選択して階層の詳細を表示します。

次の図は、選択した階層の組織階層の詳細を示しています。

![選択した階層の組織階層の詳細。](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>階層ノードへのチャネルの追加

階層ノードにチャネルを追加するには、次の手順に従います。

1. アクション ウィンドウで、**編集** を選択します。
1. チャネルを追加する階層ノードを選択し、**挿入** ドロップダウン リストから、**小売チャネル** を選択します。 
1. 追加するチャネルを選択し、**OK** ボタンを選択します。
1. アクション ウィンドウで、**保存** を選択します。
1. アクション ウィンドウで、**発行** を選択し、過去の **有効日** を指定して、このアクションを直ちに有効にします。

次の図は、チャネルを選択して階層ノードに追加する方法を示しています。

![チャネルを選択して階層ノードを追加します。](media/channel-add-to-org-hierarchy-2.png)

次の図は、さまざまなチャネルが追加された階層を示しています。

![さまざまなチャネルが追加された階層。](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>追加リソース

[チャネルの概要](channels-overview.md)

[チャネルの設定の前提条件](channels-prerequisites.md)

[組織と組織階層の概要](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[組織階層の計画](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[組織階層](channels-org-hierarchies.md)

[小売チャネルの設定](channel-setup-retail.md)
    
[オンライン チャネルの設定](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

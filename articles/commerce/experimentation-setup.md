---
title: 実験の設定
description: このトピックでは、サードパーティ サービスで実験を設定する方法について説明します。
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0f7db0ce009f6ee7603952891aacfdc16fcde016
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930236"
---
# <a name="set-up-an-experiment"></a>実験の設定

[仮説を定義し、使用する成功メトリックスを決定](experimentation-identify.md) したら、サードパーティ サービスで実験を設定する必要があります。 次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。 追加の手順については、個別のトピックで説明します。

[![実験ユーザー体験 - 設定](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>サードパーティ サービスで実験を設定する
この時点で、サードパーティ サービスを選択して実験を実行および監視し、実験コネクタを設定する必要があります。 これらの前提条件は、[Dynamics 365 Commerce での実験](experimentation-overview.md) で一覧表示されています。

サードパーティ サービスで実験を作成するために必要な手順に従います。 コネクタが適切に構成されている場合、サードパーティ サービスで設定した実験の完全なリストは、約 5 分以内にサイト ビルダーに表示されます。

## <a name="set-up-your-success-metrics"></a>成功メトリックスの設定
各実験には、バリエーションの影響を測定し、仮説を検証するためのメトリックスが必要です。 次の手順に従って、Dynamics 365 Commerce からの実際のテレメトリ イベントを使用して、サードパーティ サービスのメトリックスの計算を有効にします。

1. サイト ビルダーで、左側のナビゲーション ウィンドウの**ページ** タブを選択して、メトリックスを収集するページを選択します。 
1. 追跡するページまたはモジュールの右側のプロパティ ウィンドウで、**追跡するイベント ID** セクションに移動します。
1. **表示**を選択します。 すべてのイベント ID の一覧が表示されます。 追跡するイベントをコピーし、そのイベント キーをサードパーティ サービスの指定された場所に貼り付けます。 複数のイベントが必要な場合は、一度に 1 つのキーをコピーします。 
    - ページビューや収益追跡など、使用可能なすべてのイベントと属性を表示する方法については、[診断とトラブルシューティングの Commerce コンポーネント イベント](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) を参照してください。
1. 必要に応じて、サードパーティ サービスで、メトリックスを追跡するためのその他の手順を実行します。

## <a name="previous-step"></a>前のステップ
[仮説を識別して実験のメトリックスを決定する](experimentation-identify.md) 


## <a name="next-step"></a>次のステップ
[実験を接続して編集する](experimentation-connect-edit.md)
---
title: 実験のステータスを確認する
description: このトピックでは、Dynamics 365 Commerce の実験のライフサイクルにおける実験の状態について説明します。
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: eea67ddc1718902198b74614ee1a910fc6e29c1d
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097073"
---
# <a name="review-the-status-of-an-experiment"></a>実験のステータスを確認する
Dynamics 365 Commerce の実験の設定と実行には、多くの手順が含まれます。 実験のライフサイクルの詳細については、[Dynamics 365 Commerce での実験](experimentation-overview.md) を参照してください。

実験がライフサイクルのどこにあるかを知るには、Commerce サイト ビルダーの左側ナビゲーション ペインにある **実験** を選択します。 実験リストは、Commerce と、実験の作成、バリエーションの割り当て、データの分析に使用されているサードパーティ サービスの両方の各実験の状態と共に表示されます。

**Commerce の状態** 列に、次の値が表示される場合があります。 
- **ドラフト** - 実験は Commerce のページまたはフラグメントに接続されており、編集中です。
- **公開済** - 実験のバリエーションを Web サイトに表示する準備が整いました。 実験がサードパーティ サービスで実行されている場合、Web サイトのユーザーには、サードパーティ サービスによって選択されたページまたはフラグメントのバリエーションが表示されます。
- **未公開** - この実験は、Web サイトでは使用できなくなりました。 実験がサードパーティ サービスで実行されている場合でも、Web サイトのユーザーには、既定のバージョンのページまたはフラグメントのみが表示されます。
- **完了** - 実験はコースを実行し、バリエーションはすべての Web サイト ユーザーに公開されるようにレベルが上げられました。

同様に、 **サードパーティの状態** 列には、サードパーティ サービスでの実験の状態を示す次の値が表示される場合があります。
- **ドラフト** - 実験はサードパーティ サービスで設定されていますが、まだ開始されていません。
- **実行中** - 実験はサードパーティ サービスで開始され、データを収集しています。
- **一時停止** - 実験は一時停止され、データを収集していません。 データを再度収集するには、実験を再開する必要があります。
- **アーカイブ済** - 実験はコースを実行し、将来の参照用にサードパーティ サービスでカタログ化されています。

次の図は、両方の状態のセットと、それらが互いにどのように関連しているかを示します。

[![実験の状態](./media/experimentation_statuses.svg)](./media/experimentation_statuses.svg#lightbox)

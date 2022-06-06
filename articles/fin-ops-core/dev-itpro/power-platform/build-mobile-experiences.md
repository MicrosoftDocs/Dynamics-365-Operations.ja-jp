---
title: モバイル エクスペリエンスの作成
description: このトピックでは、財務と運用アプリ データを使用して Power Apps のモバイル エクスペリエンスを作成するために必要な高レベルの手順について説明します
author: jasongre
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jasongre
ms.dyn365.ops.version: ''
ms.search.validFrom: 2023-06-01
ms.openlocfilehash: 43acda48e4ce97b14c297e3a2017c828f9f22d08
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811834"
---
# <a name="building-mobile-experiences-over-finance-and-operations-data"></a>財務と運用データを超えたモバイル エクスペリエンスの作成 

[!include [banner](../includes/banner.md)]

今日のデジタル世界では、ユーザーがどこにいても生産性を発揮できるようにするため、モバイル デバイスで利用可能である必要がある 1 つ以上の財務と運用アプリ内で、ビジネス プロセスが発生する可能性があります。 財務と運用 (Dynamics 365) モバイル アプリの廃止により、([プラットフォーム機能の削除または廃止](../get-started/removed-deprecated-features-platform-updates.md#finance-and-operations-dynamics-365-mobile-application-and-mobile-platform) を参照)、財務と運用データを超えたモバイル エクスペリエンスの作成に関する推奨方法では、Power Platform 統合、つまり仮想テーブルおよび Power Apps で利用可能なツールを利用しています  

## <a name="implementation-steps"></a>実装の手順
財務と運用データのトップでモバイル エクスペリエンスを作成するには、高いレベルの手順に従います: 
1.  モバイル エクスペリエンスに必要なデータとアクションをカバーする[仮想テーブル](virtual-entities-overview.md) が存在することを確認します。 これらは直ぐに使用可能か、または独自の仮想テーブルを作成する必要があるかもしれません。 これは、モバイル エクスペリエンスが財務と運用アプリから適切なデータを取得し、モバイル エクスペリエンスに必要なアクションを実行するために許可する重要な作業です。 
2.  必要な仮想テーブル (複数) に接続する Power Apps に、[新しいアプリの作成](/power-apps/maker/) を実行します。
3.  Power Apps にモバイル エクスペリエンスを作成すると、[キャンバス アプリまたはモデル駆動型アプリを Power Apps モバイルで実行](/power-apps/mobile/run-powerapps-on-mobile) が直接できます。



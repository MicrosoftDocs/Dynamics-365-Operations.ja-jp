---
title: サービス更新の可用性
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations の各種のリリース オプションについて説明します。
author: meeramahabala
manager: AnnBe
ms.date: 03/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2017-10-31
ms.dyn365.ops.version: Platform update 11
ms.openlocfilehash: 73b2ed3329321c2265dbf1cd700109614ef52722
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537415"
---
# <a name="service-update-availability"></a>サービス更新の可用性

[!include [banner](../includes/banner.md)]

Dynamics 365 for Finance and Operations では、コストのかかるアップグレードを数年おきに実行するのではなく。継続的な自動サービス更新と新機能をご利用いただけます。 サービスの更新は上位互換性を保持しているため、更新のたびにコードをマージする必要がありません。  リグレッションテストには次のようなツールを活用することをお勧めします Regression Suite Automation Tool (RSAT) 。

組織が更新プログラムを受信する方法を管理することができます。 たとえば、ファーストリリース プログラムに加入すると、いち早く更新プログラムを受け取ることができます。 更新プログラムはご利用の環境に手動で適用することが可能です(self-update)。また、初期設定の更新スケジュールをままであっても、ライフサイクルサービスを使用してスケジュール設定行うと自動更新を受信します。 このトピックでは、さまざまなリリース オプションと、組織でそれらを使用する方法について説明します。

*サービスの更新*には、規制の更新を含むサービスの重要な改良であるアプリケーション (財務、レポート、小売を含む) とプラットフォームの変更の両方が含められます。 

## <a name="release-processes"></a>プロセスのリリース

それぞれの新しいリリースは、Dynamics 365 for Finance and Operations チームによって設計、開発されます。 新しいリリースはまずフィーチャーチームによって検証され、次に Dynamic 365 for Finance and Operations および Retail チームによって検証されます。 このとき、広範なテストがさまざまなトポロジで行われます。 互換性チェックでは、下位互換性を確保するためのテストも実行されます。 さらに、 [リリース検証プログラム](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUQVdKVkVORjVDNloxTEkwS1JUSUxWN1pSWi4u) はお客様がご利用いただけます。 このプログラムを使用することにより、データベースおよびベンチマークのために使用され、品質保証の追加レイヤーを提供するオートメーションでテストされるコードなどのコンポーネントを共有できます。

プレビュー アーリー アクセス プログラム (PEAP) は、 [インサイダー プログラム](https://experience.dynamics.com/) を通じて参加しているパートナー、顧客、および ISV が利用できます。  PEAPプログラムに参加することで、これからリリースされるサービス更新の試作版をいち早く見て取ることができます。  プレビュー サービス アップデートを通してできることは、機能のカスタマイズの検証、新機能の経験、Microsoftへのフィードバック提供です。  この段階では、サービス更新を開発環境、またはテスト環境に展開する必要があります。  このリリースを運用環境で使用することはできません。 PEAPプログラムに参加するには [インサイダープログラム](https://experience.dynamics.com/) から登録します。 

ファースト リリース プログラムははすべてのお客様に公開されます。 ファースト リリース プログラムに参加したお客様は、本稼働に至るまでのサービス更新に携わることのできる選ばれたグループとなることができます。  Microsoftは、このサービス更新をUATサンド ボックスへと展開し、7日後に更新プログラムを運用環境へと展開します。  このプログラムに参加しているお客様にはさらなる特典として、更新が適用された後の環境の問題発生をモニターする専属のマイクロソフトのエンジニアが付きます。  ファースト リリースに参加するには [インサイダープログラム](https://experience.dynamics.com/) から登録してください。  

サービスの更新は多くの場合、Lifecycle services (LCS) のアクション センターを使用して行われます。  サービスの更新が利用可能な場合は、運用環境を含むすべての環境に手動で適用できます。  サービスの更新が指定されたサンド ボックスまたは運用環境に適用されていない場合、Microsoftは LCSプロジェクトの「更新の設定」に基づいて自動的に更新を適用します。 より詳しい情報は、 [Lifecycle Servicesによるサービスの更新の構成](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/configure-service-updates) をご確認ください。

## <a name="release-cadence"></a>リリースの頻度
Microsoftは、毎月サービスの更新をリリースすることに取り組んでいます (3月と 9月は除きます) 。  これらのサービスの更新は、Microsoftが自動更新を適用する約2週間前から、手動で更新を適用できるようになります。  

顧客は、年間少なくとも4つのサービス更新プログラムのを適用する必要があり、一度につき2回までの連続した更新を保留にすることができます。  サービスの更新の保留は、サンド ボックスUAT、運用環境、または両環境に適用できます。  サービスの更新の保留期間が終了した後、顧客がしかるべきサービスの更新を行っていない場合は、MicrosoftはLCSの設定に基づき最新のサービスの更新を自動で適用します。 サービスの更新を保留する方法の詳細については、次を参照してください。 [Lifecycle Servicesを通じてサービスの更新を一時停止する](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/pause-service-updates) 。

### <a name="targeted-release-schedule-dates-subject-to-change"></a>対象となるリリース スケジュール (日程は変更される可能性があります)

> [!NOTE] 
> サンド ボックスの自動更新は、運用環境が更新される7日間前に行われます。

| バージョン | プレビューの可用性 (PEAP) | 使用可能 (自己更新) | 自動更新のスケジュール (LCS 更新設定を介する)|
|---------|-----------------|---------------------------|---------------------|
|10.0<br>プラットフォーム update 24 |  2019 年 2 月 1 日 | 2019年3月18日の週 | 運用環境: 開始日 4月1日 |
|10.0.1<br>プラットフォーム update 25| 2019年3月4日の週 | 2019年4月8日の週 | 運用環境: 開始日 5月1日 |
|10.0.2<br>プラットフォーム update 26| 2019年4月8日の週 | 2019年5月13日の週 | 運用環境: 開始日 6月1日  |
|10.0.3<br>プラットフォーム update 27| 2019年5月6日の週 | 2019年6月10日の週 | 運用環境: 開始日 7月1日  |
| 10.0.4<br>プラットフォーム update 28| 2019年6月3日の週 | 2019年7月8日の週 | 運用環境: 開始日 8月1日  |

> [!NOTE]
> ファースト リリース プログラムに参加されているお客様には、サービスの更新が利用可能になった時点で [ソフトウェア ライフサイクル ポリシー](../../dev-itpro/migration-upgrade/versions-update-policy.md) が適用されます。
> 
> 詳細は、 [ワン バージョン サービスの更新に関する FAQ](one-version.md) を参照してください。  

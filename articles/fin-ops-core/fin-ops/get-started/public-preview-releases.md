---
title: サービス更新の可用性
description: このトピックでは、異なるリリース オプションに関する情報を提供します。
author: ShellyBakke
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: smiller
ms.search.validFrom: 2017-10-31
ms.dyn365.ops.version: Platform update 11
ms.openlocfilehash: ddeb26c11f868cab07c6c91c37ed4face11acf2a
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923468"
---
# <a name="service-update-availability"></a>サービス更新の可用性

[!include [banner](../includes/banner.md)]

Microsoftは、予測可能なサービス更新を提供することを約束します。 これらのサービス更新は、Microsoftが自動更新を適用する約2週間前から、手動で更新を実行できるようになります。 

顧客は、年間で最大 8 つのサービス更新プログラムを適用することができ、年間で最低 2 つのサービス更新プログラムを適用する必要があります。 顧客は、一度に最大3つまでの更新を続けて一時停止することができます。 サービス更新の保留は、ユーザー受け入れテスト (UAT) サンド ボックス、運用環境、または両環境に適用できます。 サービスの更新の保留期間が終了した後、顧客がしかるべきサービスの更新を行っていない場合、Microsoft は Lifecycle Services (LCS) で利用可能になっている構成の選択に基づき最新のサービスの更新を自動で適用します。 サービスの更新を保留する方法の詳細については、次を参照してください。 [Lifecycle Servicesを通じてサービスの更新を一時停止する](../../dev-itpro/lifecycle-services/pause-service-updates.md) 。

> [!NOTE] 
> サービス更新は、3月、6月、9月、12月の間には提供されません。 

### <a name="targeted-release-schedule-dates-subject-to-change"></a>対象となるリリース スケジュール (日程は変更される可能性があります)

> [!NOTE] 
> サンド ボックスの自動更新は、運用環境が更新される7日間前に行われます。  サービスの終了は、新しい累積的なサービス更新が提供されない日付を示します。

|          バージョン          | プレビューの可用性 (PEAP) | 一般公開 (手動更新) | 自動更新のスケジュール (LCS 更新設定に基づく) 生産開始日 |   サービス終了   |
|:-------------------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|          10.0.24          |       2021 年 12 月 3 日      |          2022 年 1 月 14 日         |                           2022 年 2 月 4 日                           |   2022 年 4 月 15 日   |
|          10.0.23          |       2021 年 10 月 15 日      |         2021 年 12 月 10 日         |                           2021 年 12 月 31 日                          |   2022 年 3 月 18 日   |
|          10.0.22          |      2021 年 9 月 3 日      |          2021 年 10 月 22 日         |                           2021 年 11 月 5 日                           |  2022 年 1 月 14 日  |
|          10.0.21          |        2021 年 8 月 2 日       |         2021 年 9 月 17 日        |                            2021 年 10 月 1 日                           |  2021 年 12 月 10 日 |
|          10.0.20          |         2021 年 5 月 28 日        |           2021 年 7 月 16 日           |                             2021 年 7 月 30 日                             |  2021 年 10 月 22 日  |
|          10.0.19          |        2021 年 4 月 23 日       |            2021 年 6 月 18 日           |                             2021 年 7 月 2 日                             | 2021 年 9 月 17 日 |
|          10.0.18          |        2021 年 3 月 5 日        |           2021 年 4 月 16 日          |                            2021 年 4 月 30 日                            |    2021 年 7 月 16 日   |
|          10.0.17          |       2021 年 2 月 1 日      |           2021 年 3 月 19 日          |                             2021 年 4 月 2 日                            |    2021 年 6 月 11 日   |
|          10.0.16          |      2020 年 11 月 20 日      |          2021 年 1 月 22 日         |                           2021 年 2 月 1 日                           |   2021 年 4 月 30 日   |



            
> [!NOTE]
> ファーストリリース プログラムに参加されているお客様には、サービスの更新が利用可能になった時点で [ソフトウェア ライフサイクル ポリシー](../../dev-itpro/migration-upgrade/versions-update-policy.md) が適用されます。

https://experience.dynamics.com で Insider プログラムに参加して、PEAPプログラムにサインアップしょう。 ノミネートが受け入れられたら、プログラムに参加します。

パブリック プレビューは、Lifecycle Services の共有アセット ライブラリを介して、展開可能なパッケージとして使用できるようになります。 詳細は、 [ワン バージョン サービスの更新に関する FAQ](one-version.md) を参照してください。 

## <a name="service-update-overview"></a>サービス更新プログラムの概要
サービス更新は、新しい機能や仕様を提供する継続的な自動更新です。 数年ごとにコストのかかるアップグレードの実行が不要になります。 サービスの更新は上位互換性を保持しているため、更新のたびにコードをマージする必要がありません。  Regression Suite Automation Tool (RSAT) などのツールを使用して回帰テストを行うことをお勧めします。

組織が更新プログラムを受信する方法を管理することができます。 例えば、ファースト リリース プログラムに加入すると、いち早く更新プログラムを受け取ることができます。 更新プログラムはご利用の環境に手動で適用することが可能です (自動更新)。また、既定のリリース スケジュールのままであっても、LCS を使用してスケジュール設定行うと自動更新を受信します。

サービスの更新には、規制の更新を含むサービスの重要な改良である、アプリケーションとプラットフォーム両方の変更が含まれます。 

## <a name="release-processes"></a>プロセスのリリース

それぞれの新しいリリースは、Dynamics 365 チームによって設計および開発されます。 新しいリリースはまずフィーチャー チームによって検証され、次に Finance and Operations チームによって検証されます。 このとき、広範なテストがさまざまなトポロジで行われます。 互換性チェックでは、下位互換性を確保するためのテストも実行されます。 さらに、 [リリース検証プログラム](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUQVdKVkVORjVDNloxTEkwS1JUSUxWN1pSWi4u) はお客様がご利用いただけます。 このプログラムを使用することにより、データベースおよびベンチマークのために使用され、品質保証の追加レイヤーを提供するオートメーションでテストされるコードなどのコンポーネントを共有できます。

プレビュー アーリー アクセス プログラム (PEAP) は、[PEAP 調査](https://aka.ms/PEAP)を通じて参加しているパートナー、顧客、および ISV が利用できます。  PEAPプログラムに参加することで、これからリリースされるサービス更新の試作版をいち早く見て取ることができます。  プレビュー サービス アップデートを通してできることは、機能のカスタマイズの検証、新機能の経験、Microsoftへのフィードバック提供です。  この段階では、サービス更新を開発環境、またはテスト環境に展開する必要があります。  このリリースを運用環境で使用することはできません。 PEAP プログラムに参加するには、[PEAP 調査](https://aka.ms/PEAP)から登録をしてください。 

ファースト リリース プログラムははすべてのお客様に公開されます。 ファースト リリース プログラムに参加したお客様は、本稼働に至るまでのサービスアップデートに携わることのできる最初の選抜グループとなることができます。  Microsoftは、このサービス更新をUATサンド ボックスへと展開し、7日後に更新プログラムを運用環境へと展開します。 このプログラムに参加しているお客様にはさらなる特典として、更新が適用された後の環境の問題発生を監視するマイクロソフトの専任技術者が付きます。 ファースト リリースに参加するには、[ファースト リリース調査](https://aka.ms/FirstReleaseFnO)から登録してください。  

サービスの更新は多くの場合、LCS のアクション センターを使用して行われます。  サービスの更新が利用可能な場合は、運用環境を含むすべての環境に手動で適用できます。  サービスの更新が指定されたサンド ボックスまたは運用環境に適用されていない場合、Microsoft は LCS プロジェクトの更新の設定に基づいて自動的に更新を適用します。 より詳しい情報は、 [Lifecycle Servicesによるサービスの更新の構成](../../dev-itpro/lifecycle-services/configure-service-updates.md) をご確認ください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

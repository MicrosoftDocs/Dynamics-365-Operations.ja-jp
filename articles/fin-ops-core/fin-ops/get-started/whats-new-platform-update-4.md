---
title: Dynamics 365 for Operations プラットフォーム更新プログラム 4 (2017 年 2 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 4 の新機能または変更された機能について説明します。 このバージョンは 2017 年 2 月にリリースされ、ビルド番号は 7.0.4425.16161 です。
author: sericks007
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 271823
ms.assetid: a98f6291-347c-4616-ad80-84d3eb648cba
ms.search.region: global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 391d07d89ce3a43e1a278b7cc45f300e2a27e183
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812453"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-platform-update-4-february-2017"></a>Dynamics 365 for Operations プラットフォーム更新プログラム 4 (2017 年 2 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 4 の新機能または変更された機能について説明します。 このバージョンは 2017 年 2 月にリリースされ、ビルド番号は 7.0.4425.16161 です。

## <a name="overview"></a>概要

Microsoft Dynamics クラウド プラットフォームの継続的な更新サイクルに移行したことをお知らせします。 今月、いくつかのエキサイティングなアップデートが提供されています:

- **毎月の更新プログラム**: 頻度を毎月へと移行し、新しいシステムや既存のシステムを最新の状態に保つのに役立つより簡単な更新プロセスを提供しています。
- **埋め込み Power BI レポートは、すべてのユーザーに許可されている**: 埋め込み Microsoft Power BI レポートはすべてのユーザーに許可されています。 追加機能は、Power BI Pro ライセンスを持つユーザーが使用できます。
- **Power BI レポートが埋め込まれているワークスペースのビルドおよびリリース**: Power BI レポートが埋め込まれているワークスペースをビルドおよびリリースして、ユーザーにインタラクティブで視覚的に魅力的なエクスペリエンスを提供できます。
- **モビリティ**: モバイル フレームワークを更新して、iOS と Android デバイスをサポートする独自のオンラインとオフラインのエクスペリエンスを構築できます。
- **視覚的スケジューリング**: ガント チャートの統合を更新し、新しい視覚アイコン、ローカライズされた形式、ユーザーの効率性の更新、および改善されたリソース管理機能を追加しました。
- **フィードバック**: Microsoft Dynamics 365 for Operations の改善のためにフィードバックをお寄せください。

## <a name="monthly-updates"></a>毎月の更新プログラム

ご承知の通り、クラウド プラットフォームは更新プログラム 3 の時点で [ロック](whats-new-platform-update-3.md) されています。 ロックされているプラットフォームでは、拡張機能を使用して豊富なカスタマイズを実行できるだけでなく、コストのかかるコードのアップグレードなしで更新ができるようになります。 update 4 以降、クラウド プラットフォームのが毎月の更新プログラムをリリースします。 したがって、ボタンをクリックするだけで、最新のイノベーションを使って新しい環境や既存の環境を最新の状態に保つことができます。

既存の [LCS](https://lcs.dynamics.com/) 環境に最新の月次プラットフォーム更新プログラムをインストールするには、共用資産ライブラリを開き、 **ソフトウェア展開可能なパッケージ** タブを選択します。ここでは、次の図に示すように、プラットフォーム更新プログラム 4 パッケージの展開の準備ができていることが確認できます。 このパッケージをプロジェクトのアセット ライブラリにインポートしてから、更新フローを介して特定の環境に適用することができます。 詳細については、[最新のプラットフォーム更新プログラムの環境への適用](../../dev-itpro/migration-upgrade/upgrade-latest-platform-update.md)のトピックを参照してください。

[![プラットフォーム更新 4 パッケージ](./media/1111111-1024x171.png)](./media/1111111.png)

新しい環境では、トポロジには更新プログラム 4 が含まれます。

[![更新 4 を含むトポロジ](./media/2222222222.png)](./media/2222222222.png)

[Dynamics 365 for Operations バージョン 1611](whats-new-platform-update-3.md)では、ラットフォーム モデルをオーバーレイできません。 したがって、このリリースからすべての更新がバイナリであるため、**プラットフォーム X++ 更新プログラム** タイルは不要になりました。 Dynamics 365 for Operations バージョン 1611 より前のバージョンを使用しているお客様は、引き続きプラットフォーム モデルに対するカスタマイズのために**プラットフォーム X++ 更新プログラム** タイルを表示します。 バイナリ更新プログラムは累積的であるため、常に最新の更新プログラムを適用することをお勧めします。 詳細については、[LCS ブログ](https://blogs.msdn.microsoft.com/lcs/2017/01/26/january-2017-release-notes/) を参照してください。 Microsoft Dynamics 365 for Operations プラットフォーム更新プログラム 4 でのその他の機能の概要を次に示します。

## <a name="embedded-power-bi-reports-are-licensed-for-all-users"></a>埋め込み Power BI レポートは、すべてのユーザーに許可されています

[Power BI Embedded](../../dev-itpro/analytics/embed-power-bi-workspaces.md) は、すべてのユーザーが Dynamics 365 for Operations アプリケーションにバンドルされている分析データの豊富なグラフィカル ビューにアクセスできるようにします。 レポートは、Dynamics 365 for Operations アプリケーションに組み込まれています。 それらにアクセスするために必要な追加のライセンスはありません。

PowerBI.com サービス統合を通じて提供される既存の[タイルピン留めエクスペリエンス](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)のサポートは継続されます。 このエンベデッド エクスペリエンス以外の PowerBI.com の機能にアクセスするには、Pro ライセンスを別途取得する必要があります。

## <a name="build-and-release-workspaces-that-have-embedded-power-bi-reports"></a>Power BI レポートが埋め込まれているワークスペースのビルドおよびリリース

フル ページの、Power BI 駆動による対話型レポートをワークスペースに埋め込むことができるようになりました。 Power BI がサポートする強力なインフォグラフィックやビジュアル (サード パーティによって提供される多くのコントロールを含む) を使用することで、ワークスペースは非常に視覚的でありながらインタラクティブな体験をユーザーに提供することができます。

[![Power BI レポートが埋め込まれているワークスペース](./media/3333333333-1024x551.png)](./media/3333333333.png)

ユーザーが power user またはビジネス アナリストである場合は、Power BI ツールを使用して、既製のレポートを調整したり、新しいレポートを作成することができます。 ユーザーが開発者であり、製品の豊富なナビゲーション エクスペリエンスを提供するためにユーザーがワークスペースとして作成したレポートを使用できます。 パートナーおよび独立系ソフトウェア ベンダー (ISV) コミュニティーの一員である場合は、Power BI エクスペリエンスを含む豊富なワークスペースを構築し、それらのワークスペースをソリューションの一部としてリリースすることができるようになりました。

ユーザーが ISV またはシステム インテグレーターである場合は、Microsoft Dynamics Lifecycle Services (LCS) ソリューションの一部として、(ナビゲーション エクスペリエンスと共に) [Power BI の有効化されたワークスペースをパッケージ化](../../dev-itpro/analytics/power-bi-embedded-integration.md) することができます。 顧客は同じ体験をしますが、PowerBI.com サブスクリプションは必要はありません。 このソリューションは、Dynamics 365 for Operations でのみ動作します。

これらの機能およびその他の Power BI 機能に関する詳細については、[BI ブログ](https://blogs.msdn.microsoft.com/dynamicsaxbi/) を参照してください。

## <a name="mobility"></a>モビリティ

Dynamics 365 for Operations のモバイル フレームワークを大幅に向上させました。これにより、パートナーは、固有で完全に機能的なモバイル エクスペリエンスとなるワークスペースを構築できます。 これらの新機能により、ユーザーはオンラインとオフラインの両方で Dynamics 365 for Operations とより簡単に対話できます。 モバイルフ レームワークは、iOS と Android デバイスをサポートするようになりました。 詳細については、次回の [Mobility ブログ](https://blogs.msdn.microsoft.com/Dynamics365forOperationsMobile/) を参照してください。

[![モバイル フレームワークを使用して構築されたワークスペース](./media/444444444444-1024x533.png)](./media/444444444444.png)

## <a name="visual-scheduling"></a>視覚的スケジューリング

今回のリリースで、[ビジュアル スケジューリング](../../dev-itpro/user-interface/gantt-development-guide.md)を更新しました。

- ガント チャートで明示的に活動を整理することができるようになりました。 ガント チャート内の活動および同じプロジェクト内の移動タスクの順序を設定することができます。
- ビジュアル アイコンをタスクに対して使用できます。 たとえば、警告およびエラーのアイコンがあります。
- 日付と時刻の書式がローカライズされました。
- 選択した複数のタスク上でドラッグ アンド ドロップ操作を行うことができます。
- リソース能力バーは、予約超過がある時間間隔を明確に示します。

[![視覚的スケジューリング](./media/55555555555-1024x539.png)](./media/55555555555.png)

## <a name="feedback"></a>フィードバック

フィードバックを常に大切に扱います。 この更新処理の一環として、定期的に製品の推奨を評価するように要求されます。 お客様の経験の継続な向上に役立たせるために、このフィードバックのご提供をお願いいたします。 改善可能な領域の詳細情報を提供することも推奨します。

[![フィードバックの確認](./media/6666666666-1024x453.png)](./media/6666666666.png)

---
title: 実験のプレビューと発行
description: この記事では、Dynamics 365 Commerce から実験をプレビューおよび公開する方法について説明します。
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 5da7a4e3c17057278d02ebd45702d1de404f0dc6
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946145"
---
# <a name="preview-and-publish-an-experiment"></a>実験のプレビューと発行

この記事では、[実験を接続してバリエーションを編集](experimentation-connect-edit.md) した後、Dynamics 365 Commerce で実験をプレビューして公開する方法について説明します。 次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。 追加の手順については、個別の記事で説明します。

[ ![実験ユーザー体験 - プレビューと公開。](./media/experimentation_preview_publish.svg)](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>実験のバリエーションをプレビューする
バリエーションをプレビューして、希望どおりに表示されるまで編集を続けることができます。

Commerce サイト ビルダーでの実験のバリエーションを確認するには、以下の手順に従ってください。

1. コマンド バーの下にあるバリエーションのドロップダウン メニューを使用して、プレビューするコンテンツを選択します。 
1. コマンド バーで、**プレビュー** を選択します。 公開されたときのコンテンツがどのように表示されるかのプレビューが表示されます。
1. 異なるバリエーションをプレビューするには、バリエーション ドロップダウン メニューからそのバリエーションを選択し、**プレビュー** をもう一度選択します。

## <a name="publish-your-experiment"></a>実験の公開
公開グループを使用して実験の公開時期をスケジュールしておらず、すぐに公開する場合は、コマンド バーの **公開** を選択します。 実験に属するすべてのバリエーションが公開されます。
    
> [!IMPORTANT]
> ページに未発行の URL がある場合は、最初に URL を公開する必要があります。そうしないと、Web サイトのユーザーには表示されません。 詳細については、[ページの保存、プレビュー、および公開](save-preview-publish-page.md) を参照してください。
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>公開グループを使用して、実験がいつ公開されるかをスケジュールする
サイト ビルダーで作成したバリエーションは、発行グループを使用して、公開をスケジュールできます。 発行グループ内では、左側のナビゲーション ペインで **実験** を選択することにより、ページまたはフラグメントを試験に関連付けることができます。 また、この処理は **ページ** や **フラグメント** を選択して、[実験を接続してバリエーションを編集する](experimentation-connect-edit.md)に記載の指示に従うことでも実施できます。 公開グループの詳細については、[公開グループの使用](publish-groups.md) を参照してください。

実験で公開グループを使用する場合は、注意すべき重要な考慮事項がいくつかあります。
- 実験が実行されているページまたはフラグメントを公開グループに追加すると、その実験は公開グループのページまたはフラグメントから実験が削除されます。
- 実際のサイトのページに関連付けられている実験は、公開グループ内のページでは使用できません。またその逆も同様です。 同様に、実際のサイトでの実験が実行されているページは、公開グループの他の実験では使用できません。またその逆も同様です。
- 公開グループを公開またはスケジュールすると、公開グループに関連付けられている実験があるかどうかにかかわらず、公開グループのすべてのコンテンツが公開されます。
- 公開グループは、実際のサイトに公開された後も引き続き存続されるため、公開グループの実験も存続します。 したがって、他の実験を同じページまたはフラグメントに関連付けることはできません。 この制限を回避するには、実験が存続している公開グループを削除します。 同様に、公開グループにも存在する実際のサイトの実験を削除する場合は、最初に公開グループから実験を削除します。

### <a name="force-variations-for-testing"></a>テストにおける強制的な変動

実験がライブになったら、実験 ID とバリエーション ID を既定のページ URL に追加して、テストまたは自動化の目的でバリエーションを強制的に適用できます。 たとえば、既定のページ URL が `https://fabrikam.com/modern/homepage` の場合は、`https://fabrikam.com/modern/homepage?exp=18012910471|18024360464` などの URL を使用してバリエーションを強制できます。 上記で説明した **プレビュー** エクスペリエンスのプレビュー URL から、実験のバリエーションの実験 ID とバリエーション ID を取得できます。

## <a name="previous-step"></a>前のステップ
[接続して実験を編集する](experimentation-connect-edit.md)

## <a name="next-step"></a>次のステップ
[実験の実行と監視](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

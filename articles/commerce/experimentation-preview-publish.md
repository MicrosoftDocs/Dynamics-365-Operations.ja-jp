---
title: 実験のプレビューと発行
description: このトピックでは、Dynamics 365 Commerce から実験をプレビューおよび公開する方法について説明します。
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
ms.openlocfilehash: 91e2e4840a2d53f195d881279050b6415d48b070
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930237"
---
# <a name="preview-and-publish-an-experiment"></a>実験のプレビューと発行

このトピックでは、[実験を接続してバリエーションを編集](experimentation-connect-edit.md) した後、Dynamics 365 Commerce で実験をプレビューして公開する方法について説明します。 次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。 追加の手順については、個別のトピックで説明します。

[ ![実験ユーザー体験 - プレビューと公開](./media/experimentation_preview_publish.svg)](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>実験のバリエーションをプレビューする
バリエーションをプレビューして、希望どおりに表示されるまで編集を続けることができます。

1. サイト ビルダーで、コマンド バーの下にあるバリエーション ドロップダウン メニューを使用して、プレビューするコンテンツを選択します。 
1. トップ バーで、**プレビュー**を選択します。 公開されたときのコンテンツがどのように表示されるかのプレビューが表示されます。
1. 異なるバリエーションをプレビューするには、バリエーション ドロップダウンからそのバリエーションを選択し、**プレビュー**をもう一度選択します。

## <a name="publish-your-experiment"></a>実験の公開
公開グループを使用して実験の公開時期をスケジュールしておらず、すぐに公開する場合は、コマンド バーの**公開**を選択します。 実験に属するすべてのバリエーションが公開されます。
    
> [!IMPORTANT]
> ページに未発行の URL がある場合は、最初に URL を公開する必要があります。そうしないと、Web サイトのユーザーには表示されません。 詳細については、[ページの保存、プレビュー、および公開](save-preview-publish-page.md) を参照してください。
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>公開グループを使用して、実験がいつ公開されるかをスケジュールする
サイト ビルダーで作成したバリエーションは、発行グループを使用して、公開をスケジュールできます。 公開グループ内で、**実験**タブ、**ページ**または**フラグメント** タブに移動して、ページまたはフラグメントを実験に接続できます。詳細については、[実験を接続してバリエーションを編集する](experimentation-connect-edit.md) トピックを参照してください。 公開グループの詳細については、[公開グループの使用](publish-groups.md) を参照してください。

実験で公開グループを使用する場合は、注意すべき重要な考慮事項がいくつかあります。
- 実験が実行されているページまたはフラグメントを公開グループに追加すると、その実験は公開グループのページまたはフラグメントから実験が削除されます。
- 実際のサイトのページに関連付けられている実験は、公開グループ内のページでは使用できません。またその逆も同様です。 同様に、実際のサイトでの実験が実行されているページは、公開グループの他の実験では使用できません。またその逆も同様です。
- 公開グループを公開またはスケジュールすると、公開グループに関連付けられている実験があるかどうかにかかわらず、公開グループのすべてのコンテンツが公開されます。
- 公開グループは、実際のサイトに公開された後も引き続き存続されるため、公開グループの実験も存続します。 したがって、他の実験を同じページまたはフラグメントに関連付けることはできません。 この制限を回避するには、実験が存続している公開グループを削除します。 同様に、公開グループにも存在する実際のサイトの実験を削除する場合は、最初に公開グループから実験を削除します。

## <a name="previous-step"></a>前のステップ
[実験を接続して編集する](experimentation-connect-edit.md)

## <a name="next-step"></a>次のステップ
[実験の実行と監視](experimentation-run-monitor.md)

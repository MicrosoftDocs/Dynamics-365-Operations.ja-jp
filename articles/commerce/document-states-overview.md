---
title: ドキュメントの状態とライフサイクル
description: この記事では、Microsoft Dynamics 365 Commerce のページ要素のさまざまなドキュメントの状態について説明します。
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: intro-internal
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 350b3236eec6ad6520025bf44b22f12366f1e266
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269919"
---
# <a name="document-states-and-lifecycle"></a>ドキュメントの状態とライフサイクル

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce のページ要素のさまざまなドキュメントの状態について説明します。

## <a name="document-state-descriptions"></a>ドキュメントの状態の説明

[ページ要素](page-elements-overview.md) の記事では、コンテンツ管理システム (CMS) 内のさまざまなドキュメント タイプを一覧表示します。 これらのドキュメント タイプは、オーサリング ツールで複数の状態を持つことができます。 ドキュメントの状態によって、データの競合を防ぎ、バージョン管理を行うことができます。 これらは、ドキュメントを変更できるユーザー、ドキュメントを変更できる場合、および他のユーザーが変更を表示できる場合を決定します。

次の表は、コマースのページ要素の可能なドキュメント状態を示しています。

| ドキュメントの状態      | サイト ビルダー アクション        | 説明                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| チェックアウト済み         | **編集** を選択します。           | 該当するドキュメントが、チェックアウトされています。 ドキュメントがこの状態の間は、他の認証されたシステム ユーザーがドキュメントを変更することはできず、ドキュメントに加えた変更は自分だけに表示されます。 |
| 保存されました               | **保存** を選択します。           | チェックアウトしたドキュメントに対して行われた変更はデータベースに保存されますが、ドキュメントはまだチェックインまたは公開されていません。 保存された変更は、作成者が **編集完了** を選択するまで、他の認証済みシステム ユーザーには表示されません。 品目が公開されるまで、外部ユーザーには表示されません。 |
| 破棄済チェックアウト | **編集の破棄** を選択します。  | チェックアウトしたドキュメントへのすべての変更が破棄され、品目はチェックインされた最後のバージョンに戻ります。 |
| チェックインされました          | **編集完了** を選択します。 | 編集したドキュメントがチェックインされます。 すべての変更は、他の認証済みシステム ユーザーに表示され、それらのユーザーはドキュメントを編集できます。 各チェックインでは、品目の履歴にドキュメント バージョンのレコードが作成されます。 |
| 公開済           | **公開** を選択します。        | ドキュメントが発行され、変更が実際のサイトにプッシュされ、外部ユーザーによって検出可能になります。 **編集完了** を選択して、最初にチェックインした場合にのみ、アイテムを発行できます。 |

## <a name="additional-resources"></a>追加リソース

[コンテンツを追加する方法](add-manage-content.md)

[ページ モデルの用語集](page-elements-overview.md)

[公開グループの作業](publish-groups.md)

[クロスチャネル共有の有効化と使用](cross-channel-sharing.md)

[モジュールで動作](work-with-modules.md)

[フラグメントで動作](work-with-fragments.md)

[テンプレートとレイアウトの概要](templates-layouts-overview.md)

[サイト ナビゲーションのカスタマイズ](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: ドキュメントの状態とライフサイクル
description: このトピックでは、Microsoft Dynamics 365 Commerce のページ要素のさまざまなドキュメントの状態について説明します。
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b4f1c462f734b2d58843308f0f877fe18a4d9af7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002984"
---
# <a name="document-states-and-lifecycle"></a>ドキュメントの状態とライフサイクル


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のページ要素のさまざまなドキュメントの状態について説明します。

## <a name="document-state-descriptions"></a>ドキュメントの状態の説明

[ページ要素](page-elements-overview.md)のトピックでは、コンテンツ管理システム (CMS) 内のさまざまなドキュメント タイプを一覧表示します。 これらのドキュメント タイプは、オーサリング ツールで複数の状態を持つことができます。 ドキュメントの状態によって、データの競合を防ぎ、バージョン管理を行うことができます。 これらは、ドキュメントを変更できるユーザー、ドキュメントを変更できる場合、および他のユーザーが変更を表示できる場合を決定します。

次の表は、コマースのページ要素の可能なドキュメント状態を示しています。

| ドキュメントの状態 | 説明 |
|---|---|
| チェックアウトされました | CMS 品目がチェックアウトされると、他の認証されたシステム ユーザーがそれを編集することはできません。 品目に対して行った変更は、そのユーザーに対してのみ表示されます。 |
| チェックインされました | CMS 項目をチェック インすると、他の認証されたシステム ユーザーはすべての変更を参照できます。その後、そのユーザーは、その品目をチェックアウトして編集することができます。 各チェックインでは、品目の履歴にドキュメント バージョンのレコードが作成されます。 |
| 公開済 | CMS 品目が公開されると、サイトにプッシュされ、認証されていない外部ユーザーによってインターネット上で検出可能になります。 品目は、チェックインされている場合にのみ公開できます。 |
| 保存されました | チェックアウト済みの CMS 品目に対して行われた変更は、品目がチェックインまたは公開される前に CMS に保存できます。 これらの保存された変更内容は、品目がチェックインされるまで、他の認証されたシステム ユーザーには表示されません。 品目が公開されるまで、外部ユーザーには表示されません。 |
| 破棄済チェックアウト | チェックアウトされた CMS 項目を破棄すると、保存されていたすべての変更が削除され、品目は最後にチェックインされたバージョンに戻ります。 |

## <a name="additional-resources"></a>追加リソース

[コンテンツを追加する方法](add-manage-content.md)

[ページ モデルの用語集](page-elements-overview.md)

[公開グループで動作](publish-groups.md)

[モジュールで動作](work-with-modules.md)

[フラグメントで動作](work-with-fragments.md)

[テンプレートとレイアウトの概要](templates-layouts-overview.md)

[サイト ナビゲーションのカスタマイズ](customize-site-navigation.md)

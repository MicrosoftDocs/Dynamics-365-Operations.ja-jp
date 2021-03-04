---
title: ビジネス ドキュメント管理の新しいドキュメント ユーザー インターフェイス
description: このトピックでは、電子申告 (ER) フレームワークのビジネス ドキュメント管理機能で新しいドキュメント ユーザー インターフェイス (UI) を使用する方法について説明します。
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2cb6e0da4af07b9b8486bf1e5bda29523cbd08e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681355"
---
# <a name="new-document-user-interface-in-business-document-management"></a>ビジネス ドキュメント管理の新しいドキュメント ユーザー インターフェイス

[!include [banner](../includes/banner.md)]

ビジネス ドキュメント管理により、ビジネス ユーザーは Microsoft 365 サービスまたは適切な Microsoft Office デスクトップ アプリケーションを使用して、ビジネス ドキュメント テンプレートを編集することができます。 編集にはデザインの変更や新しい配置が含まれ、、ユーザーが追加のデータを含めるためのプレースホルダーを追加するのにソース コードを変更する必要はありません。 ビジネス ドキュメント管理の使用方法の詳細については、[ビジネス ドキュメント管理の概要](er-business-document-management.md) を参照してください。

新しいドキュメント ユーザー インターフェイス (UI) は、より明確で使いやすくなっています。 **ビジネス ドキュメント** エリアには、現在のプロバイダーに対して使用可能なテンプレートのみが表示されます。

**新しいドキュメント** ボタンを使用すると、ユーザーは別のプロバイダーによって提供される電子申告 (ER) 形式コンフィギュレーションのテンプレートの作成および編集ができます。 このトピックの例において、プロバイダーは Microsoft です。

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>ビジネス ドキュメント管理の新しいドキュメント UI を有効にする

ビジネス ドキュメント管理の新しいドキュメント UI の使用を開始するには、**機能管理** ワークスペースで、**ビジネス ドキュメント管理の Office 同様の UI エクスペリエンス** を有効にする必要があります。

すべての法人に対してこの機能を有効にするには、次の手順に従います。

1. **機能管理** ワークスペースの **新規** タブで、リスト内の **ビジネス ドキュメント管理の Office 同様の UI エクスペリエンス** を選択します。
2. **直ちに有効化** を選択し、選択した機能をオンにします。
3. ページを更新して、新しい機能にアクセスします。

### <a name="edit-templates-that-are-owned-by-other-providers"></a>他のプロバイダーが所有するテンプレートを編集

1. **ビジネス ドキュメント管理** ワークスペースで、**新規ドキュメント** を選択します。

    ![ビジネス ドキュメント管理のワークスペース](./media/BDM_overview_new_template1.png)

2. ダイアログ ボックスでテンプレートとして使用するドキュメントを選択し、**ドキュメントの作成** を選択します。

    ![ビジネス ドキュメントのダイアログボックス](./media/BDM_overview_new_template2.png)

3. 新規のダイアログボックスの **タイトル** フィールドで、必要に応じてタイトルを変更します。 このタイトル テキストは、自動的に作成される新しい ER 形式コンフィギュレーションに名前を付けるために使用されます。 このコンフィギュレーション (**顧客 FTI レポート (GER) コピー**) のドラフト バージョンには、編集したテンプレートが含まれ、現在のユーザーに対して ER 形式を実行するために使用されます。 他のすべてのユーザーは、基本 ER 形式コンフィギュレーションからの元のテンプレートを使用して、この ER 形式を実行します。
4. **名前** フィールドで、自動的に作成される編集可能なテンプレートの最初のリビジョンの名前を変更します。
5. **コメント** フィールドで、自動的に作成される編集可能なテンプレートのリビジョンの注釈を更新します。
6. **OK** を選択して、編集プロセスの開始を確認します。

    ![ドキュメント作成のダイアログボックス](./media/BDM_overview_new_template3.png)

**新規ドキュメント** ボタンは、ユーザーは別のプロバイダーによって提供される電子申告 (ER) 形式コンフィギュレーションのテンプレートの作成および編集のために使用されます。 この例において、プロバイダーは Microsoft です。 **新規ドキュメント** を選択すると、現在のプロバイダーと他のプロバイダーが所有するすべてのテンプレートが表示されます。 テンプレートを選択すると、編集用に開かれます。 編集したテンプレートは、自動的に生成される新規 ER 形式コンフィギュレーションで保存されます。

詳細については、[ビジネス ドキュメント管理の概要](er-business-document-management.md) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
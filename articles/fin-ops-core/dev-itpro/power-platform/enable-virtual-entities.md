---
title: Microsoft Dataverse 仮想エンティティを有効化する
description: この記事では、Microsoft Dataverse で財務と運用アプリの仮想エンティティを有効にする方法について説明します。
author: jaredha
ms.date: 09/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-10-14
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 77c774185e2cc9983eb6620391c52850ace82e20
ms.sourcegitcommit: 20df336e6483d1537da4cb5c687008c4dde8ed48
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2022
ms.locfileid: "9554307"
---
# <a name="enable-microsoft-dataverse-virtual-entities"></a>Microsoft Dataverse 仮想エンティティを有効化する

[!include[banner](../includes/banner.md)]



財務と運用アプリで利用可能な多くのエンティティは、データ プロトコル (OData) が有効になっているため、既定ではエンティティを Microsoft Dataverse の仮想エンティティとして利用することはできません。 Dataverse の財務と運用アプリ仮想エンティティの構成が完了すると、Dataverse 環境で仮想エンティティを有効にできます。 管理者は、どのエンティティを仮想エンティティとして公開し、Dataverse で使用できるようにするかを決定できます。

> [!NOTE]
> Dataverse での財務と運用アプリの仮想エンティティの構成は、仮想エンティティを有効にするための前提条件です。 この構成は、Microsoft Power Platform 環境にリンクされている財務と運用アプリ環境に対して自動的に行われます。 リンクされていない環境の場合、仮想エンティティを有効にする前に手動で構成を完了する必要があります。 Dataverse で財務と運用アプリの仮想エンティティを構成するためのステップ バイ ステップの手順については、[Dataverse 仮想エンティティを構成する](admin-reference.md)を参照して下さい。

## <a name="generate-virtual-entities"></a>仮想エンティティの生成

1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開き、**環境** タブを選択します。
2. **環境** の一覧で、財務と運用アプリ環境に関連付けられている Power Platform 環境を選択します。
3. 環境ページの **詳細** セクションで **環境 URL** リンクを選択して Power Platform 環境を開きます。
4. ページの右上で、**設定** のギア アイコンを開き、**詳細設定** を選択します。
5. ページの右上で、**設定** ページを開き、**高度な検索** フィルター アイコンを選択します。
6. **高度な検索** ページの **検索対象** ドロップダウン リストで、**利用可能な財務と運用エンティティ** を選択します。 
7. 結果を特定のエンティティに制限する追加のフィルター条件を入力し、**結果** を選択します。

    ![エンティティのカタログ。](../media/fovecatalog.png)

8. 有効にするエンティティを検索して開きます。
9. **表示** チェック ボックスを選択して、変更を保存します。

    ![エンティティに選択された表示チェックボックス。](../media/foveenable.png)

仮想エンティティが生成され、すべての適切なメニューに表示されます。 例えば、**高度な検索** ダイヤログ ボックスに表示されます。

## <a name="refresh-virtual-entity-metadata"></a>仮想エンティティ メタデータの更新

財務と運用アプリのエンティティ メタデータが変更されたと予想される場合、仮想エンティティ メタデータを強制的に更新できます。 強制的に更新するには、**更新** チェックボックスを選択し、変更を保存します。 財務と運用アプリの最新のエンティティ定義が Dataverse に同期され、仮想エンティティが更新されます。

## <a name="disable-virtual-entities"></a>仮想エンティティの無効化

財務と運用アプリの仮想エンティティは、マネージド ソリューションに存在し、Maker Portal から直接削除することはできません。 仮想エンティティを無効にして Dataverse 環境から仮想エンティティ メタデータを削除するには、次の手順に従います。

1. この記事の [仮想エンティティの生成](enable-virtual-entities.md#generate-virtual-entities) セクションの手順1 から 8 に従ってエンティティを検索して開きます。
1. **表示** チェックボックスをクリアします。
1. 変更を保存します。

## <a name="reference-virtual-entities"></a>仮想エンティティの参照

すべての仮想エンティティは **MicrosoftOperationsERPVE** ソリューションで生成され、API によって管理されます。 ソリューション内のアイテムは、エンティティの表示または非表示に応じて変更されます。 とはいえ、ソリューションは引き続き依存できる管理ソリューションです。 

標準のアプリケーション ライフサイクル管理 (ALM) フローは、このソリューションから仮想エンティティへの標準参照を取得します。 これを実行するには、独立系ソフトウェア仕入先 (ISV) ソリューションの **既存の追加** アクションを使用します。 仮想エンティティは、ソリューションの依存関係の不足として表示され、ソリューションのインポート時にチェックされます。 インポート時に、指定の仮想エンティティが存在しない場合は、自動的に表示されます。 追加の作業は必要ありません。

仮想エンティティを使用するには、次の手順に従います。

1. Dataverse で、通常どおり消費ロジックを含む別個のソリューションを作成します。 ソリューションの作成に関する追加情報については Power Platform ドキュメントの[ソリューションの作成](/powerapps/maker/data-platform/create-solution)を参照してください。
2. **既存の追加** \> **エンティティ** を選択します。 
3. **既存のテーブルの追加** リストで、参照したい仮想エンティティを選択します。
4. 追加する資産の選択を求めるメッセージが表示されたら、カスタマイズするフォーム、ビュー、またはその他の要素を選択し、**完了** を選択します。

開発ツールを使って、フォームなどの仮想エンティティの既存の要素を変更できます。 また、新しいフォームやビュー、その他の要素を追加することもできます。

![ソリューション。](../media/fovesolution.png)

ソリューションをエクスポートすると、**MicrosoftOperationsERPVE** ソリューションで生成された仮想エンティティへのハード依存関係が含められます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]


---
title: Microsoft Power Automate 内のビジネス イベント
description: この記事では、アプリケーション コネクタを介して Microsoft Power Automate で使用可能となるビジネス イベントに関する情報を提供します。
author: Sunil-Garg
ms.date: 10/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: Platform update 24
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: ebaf7f447c3f0ef04dcfb37532809327372d9aad
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068309"
---
# <a name="business-events-in-microsoft-power-automate"></a>Microsoft Power Automate 内のビジネス イベント

[!include[banner](../includes/banner.md)]

財務と運用コネクタと Microsoft Dataverse コネクタは、Microsoft Power Automate 内のビジネス イベントを消費するために使用できます。 財務と運用コネクタには **ビジネス イベントの発生時** というトリガーがあります。 Dataverse コネクタには、**アクションが実行される場合** というトリガーがあります。 これらのトリガーのいずれかを、財務と運用アプリ内で使用できる任意のビジネス イベントの購読に使用できます。 どちらのトリガーも同じ機能を提供しますが、実行の仕方は少し異なります。

Dataverse コネクタによって、財務と運用アプリ内のデータ イベントを購読するための、**行が追加、変更、または削除される場合** というトリガーを使用できます。 このトリガーにより、選択された財務と運用アプリ エンティティに対するイベントを作成、更新、または削除 (CUD) することにより Power Automate フローがトリガーされるようになります。

## <a name="prerequisite"></a>前提条件

ビジネス イベントについて理解することは重要です。 詳細については[ビジネス イベント](home-page.md) のドキュメントを参照してください。

## <a name="subscribing-to-business-events"></a>ビジネス イベントの購読

### <a name="using-the-finance-and-operations-connector"></a>財務と運用コネクタを使用する

財務と運用コネクタは、サブスクリプションを確立するために財務と運用アプリと直接通信しますが、実行時に Dataverse によってトリガーされます。 コネクタは、Azure Active Directory (Azure AD) テナント上の任意の財務と運用アプリのインスタンスに接続できます。 

**ビジネス イベントの発生時** というトリガーをフローに追加した後、以下の情報を提供する必要があります。

- **インスタンス** – ビジネス イベントが発生するインスタンスのホスト名を指定します。 環境インスタンスは指定されたドロップダウン メニューで利用可能である必要がありますが、環境が一覧表示されていない場合はカスタム値として入力することができます。
- **カテゴリ** - ビジネス イベントのカテゴリを選択します。 財務と運用アプリのビジネス イベント カタログ内の一意のビジネス イベント カテゴリの一覧が表示されます。
- **ビジネス イベント**- フローをトリガーする必要があるビジネス イベントを選択します。 一覧に表示されるビジネス イベントはすべて、財務と運用アプリのビジネス イベント カタログで選択したカテゴリのビジネス イベントです。
- **法人** - ビジネス イベントが購読されている法人を指定します。 フローは法人でビジネス イベントが発生するときにトリガーされます。 既定では、このフィールドは空白で、ビジネス イベントは **すべて** の法人で購読されます。

![ビジネス イベント発生時というトリガー。](../media/businessevents_FinOpsConnector.png)

フローが保存されると、選択したビジネス イベントに対するサブスクリプションが環境インスタンスに追加されます。 サブスクリプション プロセスの一部として、必要なエンドポイントが設定され、対応するビジネス イベントが有効にされます。

### <a name="using-the-dataverse-connector"></a>Dataverse コネクタの使用

財務と運用アプリのビジネス イベントは、Dataverse コネクタの **アクションが実行される場合** というトリガーを通しても公開されます。 このトリガーは、**Catalog** テーブルおよび **CatalogAssignment** テーブルを使用して Dataverse で構成されたアクションおよびテーブル操作を公開します。 このコンフィギュレーションは、財務と運用アプリのビジネス イベントに限定されない、Dataverse でのより汎用性のあるビジネス イベント フレームワークを提供します。 財務と運用アプリのビジネス イベント カタログのビジネス イベントは、Dataverse ビジネス イベント カタログと同期されます。 したがって、財務と運用アプリのビジネス イベントを購読して、Power Automate フローでビジネス ロジックを開始できます。 Dataverse ビジネス イベント フレームワークでのカタログの詳細については、[Catalog テーブルおよび CatalogAssignment テーブル](/powerapps/developer/data-platform/catalog-catalogassignment) を参照してください 。

Dataverse コネクタの **アクションが実行される場合** というトリガーで財務と運用アプリのビジネス イベントを使用するには、Microsoft Power Platform 統合を財務と運用アプリ環境に対して有効にする必要があり、それによって財務と運用アプリ環境が Dataverse 環境に接続されます。 財務と運用アプリ環境の Microsoft Power Platform 統合を有効にする方法の詳細については、[Microsoft Power Platform 統合の有効化](../power-platform/enable-power-platform-integration.md)を参照してください。 

> [!NOTE]
> Microsoft Power Platform 統合では、財務と運用アプリと Microsoft Power Platform 環境の間に 1 対 1 の接続があります。 この関係のため、財務と運用コネクタの **ビジネス イベントの発生時** というトリガーとして、複数の財務と運用アプリ環境は選択できません。 トリガーは、Microsoft Power Platform 統合に対して選択された財務と運用アプリ環境に自動的に接続します。

**アクションが実行される場合** というトリガーを Power Automate でフローに追加した後、以下の情報を提供する必要があります。

- **カタログ** - **財務と運用** を選択します。 これにより、財務と運用ビジネス イベントが Dataverse ビジネス イベント カタログとして公開されます。
- **カテゴリ**- 目的のビジネス イベントのカテゴリを選択します。 財務と運用アプリのビジネス イベント カタログ内の一意のビジネス イベント カテゴリの一覧が表示されます。
- **テーブル名**- アクションが特定のテーブルに関連する場合に、関連するテーブルを選択します。 通常、値は財務と運用アプリ ビジネス イベントに対して **(なし)** になります。
- **アクション名**- フローをトリガーする必要があるアクションまたはビジネス イベントを選択します。 ドロップダウン リストには、財務と運用アプリのビジネス イベント カタログで選択したカテゴリのすべての同期されたビジネス イベントが表示されます。

![Microsoft Dataverse コネクタの、アクションが実行される場合というトリガー。](../media/businessevents_DataverseConnector.png)

Power Automate での **アクションが実行される場合** というトリガーの使用方法の詳細については、[アクションを含むトリガー フロー](/power-automate/dataverse/action-trigger) を参照してください 。

> [!NOTE]
> Power Automate エンドポイントは、手動で構成することはできません。 上記の説明に従って、エンドポイントは Power Automate で自動的に作成されます。

## <a name="subscribing-to-data-events"></a>データ イベントの購読

Dataverse で仮想エンティティとして有効な財務と運用アプリ エンティティが Dataverse コネクタの **行が追加、変更または削除される場合** というトリガーに含まれます。 Power Automate でトリガーをフローに追加する場合、フローをトリガーするテーブルのテーブル名を定義します。 **テーブル名** の一覧には、Microsoft Power Platform 統合を通して Microsoft Power Platform 環境に接続されている財務と運用アプリ環境から Dataverse で仮想エンティティとして公開される、すべての財務と運用アプリ エンティティの一覧が含まれます。 仮想エンティティを有効化する方法については、[Dataverse 仮想エンティティの有効化](../power-platform/enable-virtual-entities.md) を参照してください。

![Microsoft Dataverse コネクタの行が追加、変更または削除されるというトリガー。](../media/businessevents_DataEventConnector.png)

> [!NOTE]
> **テーブル名** フィールドに **mserp** を入力することで、テーブルの一覧をフィルター処理して、環境に対して有効で使用可能な財務と運用アプリ仮想エンティティのみを表示できます。

詳細なオプションに関する情報など、Dataverse コネクタの **行が追加、変更または削除される** というトリガーを使用する方法の詳細については、[行が追加、変更または削除される場合のトリガー フロー](/power-automate/dataverse/create-update-delete-trigger) を参照してください。

## <a name="unsubscribing-from-business-events"></a>ビジネス イベントの購読解除

トリガーが削除されるか、フローがオフになっている場合は、ビジネス イベントのエンドポイントが自動的に削除されます。

## <a name="adjusting-flow-parameter-limits"></a>フロー パラメーターの制限の調整

複数のフローは、同一もしくは異なる法人内の同じビジネス イベントを購読することができます。 1 つのイベントごとの既定のエンドポイント制限は、10 です。 必要に応じて、**ビジネス イベント パラメーター** ページの **イベントごとに許可されるエンドポイント** を調整します。

## <a name="other-ways-to-consume-business-events-in-power-automate"></a>Power Automate 内のビジネス イベントを消費する他の方法

前のセクションでは、コネクタ内でトリガーを使用することにより Power Automate から直接ビジネス イベントを購読する方法について説明しました。 ただし、[Microsoft Power Automate 用イベント グリッド コネクタ](/connectors/azureeventgrid/) を使用することにより、Microsoft Azure Event Grid から Microsoft Power Automate 内のビジネス イベントを消費することもできます。

実装内の他の統合で既に使用されている場合、イベント グリッドは Power Automate 内のビジネス イベントを消費するための実行可能なアプローチである可能性があります。 同じ法人内のビジネス イベントが複数のフローをトリガする必要がある場合、イベント グリッドからビジネス イベントを消費することを検討する必要があります。

このアプローチは、コネクタが Power Automate 内のビジネス イベントで使用可能である場合、ビジネス イベントのエンドポイントとして使用されるメッセージングまたはイベント プラットフォームに対して適用することができます。

Microsoft Flow でビジネス イベントを使用する方法については [Microsoft Flow でビジネス イベントを消費する](how-to/how-to-flow.md) を参照してください。 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]


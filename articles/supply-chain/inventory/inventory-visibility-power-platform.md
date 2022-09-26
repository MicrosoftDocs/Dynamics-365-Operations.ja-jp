---
title: 在庫の視覚化アプリ
description: この記事では、Inventory Visibility アプリの使用方法について説明します。
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 674adb70cc4372a8c5ca8c75ed3ef840d8ec7b79
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520867"
---
# <a name="use-the-inventory-visibility-app"></a>Inventory Visibility アプリを使用する

[!include [banner](../includes/banner.md)]

この記事では、Inventory Visibility アプリの使用方法について説明します。

在庫の視覚化は、視覚化のためのモデル駆動型アプリを提供します。 アプリには、**コンフィギュレーション**、**運用の可視性**、および **在庫集計** の 3 つのページが含まれます。 次の機能があります:

- 手持構成と仮引当構成を行うユーザー インターフェイス (UI) を提供します。
- さまざまな分析コードの組み合わせによるリアルタイムの手持在庫のクエリがサポートされます。
- 引当要求を転記するための UI を提供します。
- すべての分析コードと共に、製品の手持在庫のビューを提供します。
- 事前定義された分析コードと共に、製品の手持在庫リストのビューを提供します。


## <a name="prerequisites"></a>必要条件

開始する前に、[在庫視覚化のインストールと設定](inventory-visibility-setup.md)で示されているように、在庫視覚化アドインのインストールと設定を行います。

## <a name="open-the-inventory-visibility-app"></a>在庫視覚化アプリを開く

在庫視覚化アプリを開くには、Power Apps 環境にサインインして **在庫視覚化** を開きます。

## <a name="configuration"></a><a name="configuration"></a>構成

在庫視覚化アプリの **構成** ページでは、手持構成と仮引当構成を設定できます。 アドインをインストールすると、既定の構成に Microsoft Dynamics 365 Supply Chain Management (`fno` データ ソース) 用の既定の設定が含まれるようになります。 既定の設定を確認できます。 今後は、業務要件や外部システムの在庫転記要件に基づき、複数のシステム間で在庫変更を転記、整理、およびクエリする方法を標準化するように構成を変更することができます。

ソリューションの構成方法の詳細については、[在庫視覚化の構成](inventory-visibility-configuration.md)を参照してください。

## <a name="operational-visibility"></a>運用可視化

**運用可視化** ページは、さまざまな分析コードの組み合わせに基づいた、リアルタイムの手持在庫クエリの結果を提供します。 *OnHandReservation* 機能が有効になっている場合、**運用可視化** ページから引当要求を転記することもできます。

### <a name="on-hand-query"></a>手持在庫クエリ

**手持在庫クエリ** タブに、リアルタイムの手持在庫クエリの結果が表示されます。

**運用可視化** ページの **手持在庫のクエリ** タブを開くと、システムは資格情報を要求し、Inventory Visibility サービスを照会するために必要なベアラー トークンを取得することができます。 **BearerToken** フィールドにベアラー トークンを貼り付け、ダイアログ ボックスを閉じることができます。 その後、手持在庫クエリ要求を転記することができます。

ベアラー トークンが有効でないか、または期限切れの場合、新しいトークンを **BearerToken** フィールドに貼り付ける必要があります。 正しい **クライアント ID**、**テナント ID**、**クライアント シークレット** の値を入力し、**更新** を選択します。 システムは自動的に有効な新しいベアラー トークンを取得します。

手持在庫クエリを転記するには、要求の本文にクエリを入力します。 [転記メソッドを使用したクエリ](inventory-visibility-api.md#query-with-post-method)で説明されているパターンを使用します。

![手持在庫クエリの設定](media/inventory-visibility-query-settings.png "手持在庫クエリの設定")

### <a name="reservation-posting"></a>引当の転記

**運用可視化** ページの **引当の転記** タブを使用して、引当要求を転記します。 引当要求を転記する前に、*OnHandReservation* 機能を有効にする必要があります。 この機能の詳細と有効にする方法については、[Inventory Visibility の引当](inventory-visibility-reservations.md) を参照してください。

引当要求を転記するには、要求の本文に値を入力する必要があります。 [1 つの予約イベントの作成](inventory-visibility-api.md#create-one-reservation-event)で説明されているパターンを使用します。 その後、**転記** を選択します。 要求応答の詳細を表示するには、**詳細の表示** を選択します。 応答の詳細から `reservationId` の値も取得できます。

## <a name="inventory-summary"></a><a name="inventory-summary"></a>在庫集計

**在庫概要** ページは、すべての分析コードと共に、製品の在庫概要を提供します。 これは、*手持在庫合計* エンティティ用にカスタマイズされたビューです。 在庫概要データは、在庫品目一覧から定期的に同期されます。

**在庫概要** ページを有効にして、同期頻度を設定するには次の手順に従います。

1. **構成** ページを開きます。
1. **機能管理 & 設定** タブを開きます。
1. **OnHandMostSpecificBackgroundService** 機能の 切り替えスイッチを *はい* に設定します。
1. この機能を有効にすると、**サービス構成** セクションが使用できる状態になり、**OnHandMostSpecificBackgroundService** 機能を構成するための行が含まれます。 この設定により、在庫概要データを同期する頻度を選択できます。 **値** 列の **上へ** ボタンおよび **下へ** ボタンを使用して、同期間の時間を変更します (最大で 5 分)。 その後、**保存** を選択します。

    ![OnHandMostSpecificBackgroundService 設定](media/inventory-visibility-ohms-freq.png "OnHandMostSpecificBackgroundService 設定")

1. すべての変更 を保存するには、**構成の更新** を選択します。


> [!NOTE]
> *OnHandMostSpecificBackgroundService* 機能は、機能を有効にした後に発生した手持在庫の変更のみを追跡します。 機能を有効にしてから変更していない製品のデータは、在庫サービス キャッシュから Dataverse 環境に同期されません。 **在庫集計** ページに必要なすべての手持在庫情報が表示されていない場合は、Supply Chain Management を開き、**在庫管理 > 定期処理タスク > Inventory Visibility の統合** に移動し、バッチ ジョブを無効にしてから再度有効にします。 これにより、最初のプッシュが実行され、次の 15 分ですべてのデータが *Inventory OnHand Sum* エンティティに同期されます。 *OnHandMostSpecificBackgroundService* 機能を使用する場合は、手持在庫変更を作成し、**Inventory Visibility 統合** バッチ ジョブを有効にする前に、この機能をオンにすることをお勧めします。

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-the-inventory-visibility-onhand-query"></a>合理化された手持在庫クエリのプリロード

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management では、現在の手持在庫に関する多くの情報が格納され、さまざまな目的に利用できます。 ただし、日常業務やサード パーティ統合の多くは、これらの詳細の小さなサブセットのみを必要とし、すべてをシステムに照会すると、膨大なデータ セットになり、作成や転送に時間がかかる可能性があります。 したがって、Inventory Visibility サービスは、最適化された情報を継続的に利用できるように、合理化された一連の手持在庫データを定期的にフェッチして格納できます。 格納された手持在庫の詳細は、構成可能なビジネス基準に基づいてフィルター処理され、最も関連性の高い情報のみが含まれるようになります。 フィルター処理された手持在庫のリストは Inventory Visibility サービスでローカルに格納され、定期的に更新されるため、クイック アクセス、オンデマンド データ エクスポート、および外部システムとの合理化された統合をサポートします。

> [!NOTE]
> この機能の現在のプレビュー バージョンでは、サイトと場所を含むプリロードされた結果のみ提供できます。 機能の最終バージョンでは、他の分析コードを選択して結果とともにプリロードできることが想定されています。

**Inventory Visibility 集計のプリロード** ページには、*On-hand Index Query Preload Results* エンティティのビューが表示されます。 *Inventory summary* エンティティとは異なり、*On-hand Index Query Preload Results* エンティティは、選択した分析コードと共に製品の手持在庫リストを提供します。 Inventory Visibility により、プリロードされた集計データは 15 分おきに同期されます。

**Inventory Visibility 集計のプリロード** タブにデータを表示するには、**コンフィギュレーション** ページの **機能管理** タブで *OnHandIndexQueryPreloadBackgroundService* 機能を有効にし、**コンフィギュレーションの更新** を選択する必要があります ([Inventory Visibility の構成](inventory-visibility-configuration.md) も参照)。

> [!NOTE]
> *OnhandMostSpecificBackgroudService* 機能と同様に、*OnHandIndexQueryPreloadBackgroundService* 機能は、機能を有効にした後に発生した手持在庫の変更のみを追跡します。 機能を有効にしてから変更していない製品のデータは、在庫サービス キャッシュから Dataverse 環境に同期されません。 **在庫集計** ページに必要なすべての手持在庫情報が表示されていない場合は、**在庫管理 > 定期処理タスク > Inventory Visibility の統合** に移動し、バッチ ジョブを無効にしてから再度有効にします。 これにより、最初のプッシュが実行され、すべてのデータが次の 15 分で *On-hand Index Query Preload Results* エンティティに同期されます。 この機能を使用する場合は、手持在庫変更を作成し、**Inventory Visibility 統合** バッチ ジョブを有効にする前に、この機能をオンにすることをお勧めします。

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a>在庫集計のフィルター処理および参照

Dataverse が提供する **高度なフィルター** を使用することにより、自分にとって重要な行を示す個人用ビューを作成できます。 高度なフィルター オプションを使用すると、単純なものから複雑なものまで、さまざまなビューを作成できます。 グループ化され、入れ子になった条件をフィルターに追加することもできます。 高度なフィルターの使用方法の詳細については、[高度なグリッド フィルターを使用した個人用ビューの編集または作成](/powerapps/user/grid-filters-advanced) を参照してください。

**在庫集計** ページには、グリッドの上に 3つのフィールド (**既定の分析コード**、**カスタム分析コード**、**メジャー**) があり、表示される列を制御するために使用できます。 また、列ヘッダーを選択して、その列で現在の結果をフィルター処理または並べ替えることもできます。 次のスクリーン ショットでは、**在庫の集計** ページで使用できる分析コード、フィルター、結果数、"さらに読み込む" の フィールドが強調表示されています。

![在庫集計ページ。](media/inventory-visibility-onhand-list.png "在庫集計ページ")

集計データの読み込みに使用する分析コードがあらかじめ定義されているため、**Inventory Visibility 集計のプリロード** ページには分析コード関連の列が表示されます。 *分析コードはカスタマイズできません&mdash;システムは、プリロードされた手持在庫リストのサイトと場所の分析コードのみをサポートしています。* **Inventory Visibility 集計のプリロード** ページには、分析コードが既に選択されている以外は、**在庫集計** ページと同様のフィルターがあります。 次のスクリーン ショットでは、**Inventory Visibility 集計のプリロード** ページで使用できるフィルター フィールドが強調表示されています。

![Inventory Visibility 集計のプリロード ページ。](media/inventory-visibility-preload-onhand-list.png "Inventory Visibility 集計のプリロード ページ")

**Inventory Visibility 集計のプリロード** および **在庫集計** ページの下部には、"50 レコード (29 選択)" や "50 レコード" などの情報が表示されます。 この情報は、**高度なフィルター** の結果から現在読み込まれているレコードを参照しています。 「29 件選択済み」というテキストは、列ヘッダー フィルターを使用して読み込まれたレコードに対して選択されたレコード数を表します。 Dataverse からさらに多くのレコードを読み込むために使用できる **さらに読み込む** ボタンもあります。 読み込まれるレコードの既定の数は 50 です。 **さらに読み込む** を選択すると、次に使用可能な 1,000 レコードがビューに読み込まれます。 **さらに読み込む** ボタン上の数は、現在読み込まれているレコードと **高度なフィルター** の結果のレコード総数を示しています。

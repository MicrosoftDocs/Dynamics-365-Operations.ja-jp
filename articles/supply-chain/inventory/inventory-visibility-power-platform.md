---
title: 在庫の視覚化アプリ
description: この記事では、Inventory Visibility アプリの使用方法について説明します。
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a360b8beaad2bf6916c22765131e37f90e40282b
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306176"
---
# <a name="use-the-inventory-visibility-app"></a>Inventory Visibility アプリを使用する

[!include [banner](../includes/banner.md)]


この記事では、Inventory Visibility アプリの使用方法について説明します。

在庫の視覚化は、視覚化のためのモデル駆動型アプリを提供します。 アプリには、**コンフィギュレーション**、**運用の可視性**、および **在庫集計** の 3 つのページが含まれます。 次の機能があります:

- 手持構成と仮引当構成を行うユーザー インターフェイス (UI) を提供します。
- さまざまな分析コードの組み合わせによるリアルタイムの手持在庫のクエリがサポートされます。
- 引当要求を転記するための UI を提供します。
- すべての分析コードを使用して製品の手持在庫のカスタマイズ ビューを提供します。

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

**手持在庫クエリ** タブを選択すると、システムは資格情報を要求し、在庫視覚化サービスを照会するために必要なベアラー トークンを取得することができます。 **BearerToken** フィールドにベアラー トークンを貼り付け、ダイアログ ボックスを閉じることができます。 その後、手持在庫クエリ要求を転記することができます。

ベアラー トークンが有効でないか、または期限切れの場合、新しいトークンを **BearerToken** フィールドに貼り付ける必要があります。 正しい **クライアント ID**、**テナント ID**、**クライアント シークレット** の値を入力し、**更新** を選択します。 システムは自動的に有効な新しいベアラー トークンを取得します。

手持在庫クエリを転記するには、要求の本文にクエリを入力します。 [転記メソッドを使用したクエリ](inventory-visibility-api.md#query-with-post-method)で説明されているパターンを使用します。

![手持在庫クエリの設定](media/inventory-visibility-query-settings.png "手持在庫クエリの設定")

### <a name="reservation-posting"></a>引当の転記

**引当の転記** タブを使用して、引当要求を転記します。 引当要求を転記する前に、*OnHandReservation* 機能を有効にする必要があります。 この機能の詳細については、[在庫可視性の確保](inventory-visibility-reservations.md)を参照してください。

引当要求を転記するには、要求の本文に値を入力する必要があります。 [1 つの予約イベントの作成](inventory-visibility-api.md#create-one-reservation-event)で説明されているパターンを使用します。 その後、**転記** を選択します。 要求応答の詳細を表示するには、**詳細の表示** を選択します。 応答の詳細から `reservationId` の値も取得できます。

## <a name="inventory-summary"></a><a name="inventory-summary"></a>在庫集計

**在庫概要** ページは、すべての分析コードと共に、製品の在庫概要を提供します。 これは、*手持在庫合計* エンティティ用にカスタマイズされたビューです。 在庫概要データは、在庫品目一覧から定期的に同期されます。

### <a name="enable-the-inventory-summary-and-set-the-synchronization-frequency"></a>在庫概要を有効にして同期頻度を設定する

**在庫概要** ページを有効にして、同期頻度を設定するには次の手順に従います。

1. **構成** ページを開きます。
1. **機能管理 & 設定** タブを開きます。
1. **OnHandMostSpecificBackgroundService** 機能の 切り替えスイッチを *はい* に設定します。
1. この機能を有効にすると、**サービス構成** セクションが使用できる状態になり、**OnHandMostSpecificBackgroundService** 機能を構成するための行が含まれます。 この設定により、在庫概要データを同期する頻度を選択できます。 **値** 列の **上へ** ボタンおよび **下へ** ボタンを使用して、同期間の時間を変更します (最大で 5 分)。 その後、**保存** を選択します。
1. すべての変更 を保存するには、**構成の更新** を選択します。

![OnHandMostSpecificBackgroundService 設定](media/inventory-visibility-ohms-freq.PNG "OnHandMostSpecificBackgroundService 設定")

> [!NOTE]
> *OnHandMostSpecificBackgroundService* 機能は、機能を有効にした後に発生した製品の手持在庫変更のみを追跡します。 機能を有効にしてから変更していない製品のデータは、在庫サービス キャッシュから Dataverse 環境に同期されません。 **在庫集計** ページに必要なすべての手持在庫情報が表示されていない場合は、**在庫管理 > 定期処理タスク > Inventory Visibility の統合** に移動し、バッチ ジョブを無効にしてから再度有効にします。 これにより、最初のプッシュが実行され、次の 15 分ですべてのデータが *Inventory OnHand Sum* エンティティに同期されます。 この機能を使用する場合は、手持在庫変更を作成し、**Inventory Visibility 統合** バッチ ジョブを有効にする前に、この機能をオンにすることをお勧めします。

### <a name="work-with-the-inventory-summary"></a>在庫概要を使って作業する

Dataverse が提供する **高度なフィルター** を使用することにより、自分にとって重要な行を示す個人用ビューを作成できます。 高度なフィルター オプションを使用すると、単純なものから複雑なものまで、さまざまなビューを作成できます。 グループ化され、入れ子になった条件をフィルターに追加することもできます。 **高度なフィルター** の使用方法の詳細については、[高度なグリッド フィルターを使用した個人用ビューの編集または作成](/powerapps/user/grid-filters-advanced)を参照してください。

カスタマイズ ビューの上部には、**既定の分析コード**、**カスタム分析コード**、および **測定** の 3 つのフィールドが表示されます。 これらのフィールドを使用して、表示する列を制御できます。

現在の結果をフィルター処理または並べ替えるための列のヘッダーを選択できます。

カスタマイズ ビューの下部に、「50 レコード (29 件選択済み)」または「50 レコード」などの情報が表示されます。 この情報は、**高度なフィルター** の結果から現在読み込まれているレコードを参照しています。 「29 件選択済み」というテキストは、列ヘッダー フィルターを使用して読み込まれたレコードに対して選択されたレコード数を表します。

ビューの下部にある **さらに読み込む** ボタンにより、Dataverse からさらに多くのレコードを読み込むことができます。 読み込まれるレコードの既定の数は 50 です。 **さらに読み込む** を選択するとき、次に使用可能な 1,000 レコードがビューに読み込まれます。 **さらに読み込む** ボタン上の数は、現在読み込まれているレコードと **高度なフィルター** の結果のレコード総数を示しています。

![在庫集計](media/inventory-visibility-onhand-list.png "在庫集計")

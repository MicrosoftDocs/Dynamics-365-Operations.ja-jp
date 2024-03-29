---
title: 梱包とストレージへのさまざまな分析コードの設定
description: この記事では、指定した各分析コードを使用するプロセス (梱包、ストレージ、または入れ子になった梱包) を指定する方法について説明します。
author: Mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e2cfcc13f397f57413be1773683daf1f828beaf8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334448"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>梱包とストレージへのさまざまな分析コードの設定

[!include [banner](../../includes/banner.md)]

一部の品目は、複数の異なるプロセスで物理的な分析コードをそれぞれ異なる方法で追跡する必要があるなどの方法で梱包または格納されます。 *梱包製品分析コード* 機能を使用すると、製品ごとに 1 つ以上のタイプの分析コードを設定できます。 各分析コード タイプは、一連の物理的測定 (重量、幅、奥行、高さ) を提供し、これらの物理的測定値が適用されるプロセスを設定します。 この機能が有効な場合、システムは次のタイプの分析コードをサポートします。

- *ストレージ* - 保管分析コードを場所の容積測定スペースと共に使用して、各品目をさまざまな倉庫の場所に保管できる数量を決定します。
- *梱包* - 梱包分析コードは、コンテナ詰めと手動梱包プロセスで使用され、各品目がさまざまなコンテナ タイプに収まる数を決定します。
- *入れ子になった梱包* - 入れ子になった梱包分析コードは、梱包プロセスに複数のレベルが含まれる場合に使用されます。

*梱包製品分析コード* 機能を無効 にした場合でも、*ストレージ* 分析コードがサポートされます。 これらは、Supply Chain Management の **物理分析コード** ページを使用して設定します。 これらの分析コードは、梱包と入れ子になった梱包分析コードが指定されていないすべてのプロセスで使用されます。

*梱包* と *入れ子になった梱包* 分析コードは、**梱包製品分析コード** 機能を有効にした場合に追加される *物理的な製品分析コード* ページを使用 して設定されます。
この記事では、この機能の使い方を説明するシナリオについて説明します。

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>梱包製品分析コード機能をオンにする

この機能は使用する前にシステムでオンにする必要があります。 管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。 この機能は、次のようにして表示されます。

- **モジュール:** *倉庫管理*
- **機能名:** *梱包製品分析コード*

## <a name="example-scenario"></a>シナリオ例

### <a name="set-up-the-scenario"></a>シナリオを設定する

シナリオ例を実行する前に、このセクションの説明に従ってシステムを準備する必要があります。

#### <a name="enable-demo-data"></a>デモ データを有効にする

ここで指定されたデモ レコードと値を使用してシナリオを実行するには、標準 [デモ データ](../../fin-ops-core/fin-ops/get-started/demo-data.md) がインストールされているシステムを使用する必要があります。 また、開始する前に *USMF* 法人を選択する必要があります。

#### <a name="add-a-new-physical-dimension-to-a-product"></a>製品への新しい物理的分析コードの追加

次の手順に従って、製品の新しい物理的分析コードを追加します。

1. **製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。
1. 製品を **品目番号** *A0001* で選択します。
1. アクション ペインの **在庫の管理** タブを開いて、**倉庫** グループから、**現物製品分析コード** を選択します。
1. **現物製品分析コード** ページが開きます。 アクション ペインで、**新規** を選択して新規分析コードをグリッドに追加して、次のフィールドを設定します。
    - **現物分析コードの種類** - *梱包*
    - **物理単位** - *個数*
    - **重量** - *4*
    - **重量単位** - *kg*
    - **Depth** - *3*
    - **高さ** - *4*
    - **幅** - *3*
    - **長さ** - *cm*
    - **容積単位** - *cm3*

**容積** フィールドは、**奥行き**、**高さ**、および **幅** の設定に基づいて自動的に計算されます。

#### <a name="create-a-new-container-type"></a>新規コンテナー タイプの作成

**倉庫管理 \>設定 \>コンテナー \>コンテナー タイプ** の順に移動して、次の設定を使用して新規レコードを作成します。

- **コンテナー タイプ コード** - *短いボックス*
- **説明** - *短いボックス*
- **最大正味重量** - *50*
- **容量** - *144*
- **長さ** - *6*
- **幅** - *6*
- **高さ** - *4*

#### <a name="create-a-container-group"></a>コンテナーグループの作成

**倉庫管理 \>設定 \>コンテナー \>コンテナー グループ** の順に移動して、次の設定を使用して新規レコードを作成します。

- **コンテナー グループ ID** - *短いボックス*
- **説明** - *短いボックス*

**詳細** セクションをクリックして、新しい行を追加します。 **コンテナタイプ** を *短いボックス* に設定します。

#### <a name="set-up-a-container-build-template"></a>コンテナー構築テンプレートのセットアップ

**倉庫管理 \> 設定 \> コンテナー \> コンテナー ビルド テンプレート** の順に移動して、**箱** を選択します。 **コンテナ グループ ID** を *短いボックス* に変更します。

### <a name="run-the-scenario"></a>シナリオの実行

前のセクションの説明に従ってシステムを準備できたら、次のセクションの説明に従ってシナリオを実行できます。

#### <a name="create-a-sales-order-and-create-a-shipment"></a>販売注文の作成と出荷の作成

このプロセスでは、高さが 3 未満の品目 *梱包* 分析コードに基づいて出荷を作成します。

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **販売注文の作成** ダイアログ ボックスでは、次の値を設定します。

    - **顧客アカウント:** *US-001*
    - **倉庫:** *63*

1. **OK** を選択して販売注文を作成し、ダイアログ ボックスを閉じます。
1. 新しい販売注文が開かれます。 **販売注文明細行** クイック タブのグリッドに、新しい空の明細行を含める必要があります。 この明細行で、次の値を設定します。

    - **品目番号:** *A0001*
    - **数量:** *5*

1. **販売注文行** クイック タブで、**在庫 \> 予約** を選択します。
1. **引当** ページの、アクション ウィンドウで **ロットの引当** を選択して、在庫を引当てします。
1. ページを閉じます。
1. アクション ペインの **倉庫** タブで、**倉庫へのリリース** を選択して、倉庫の作業を作成します。
1. **販売注文明細行** クイック タブで、**倉庫 \> 出荷の詳細** を選択します。
1. アクション ペインで、**輸送** タブを開き、**コンテナーの表示** を選択します。 2 つの *短いボックス* コンテナに品目がコンテナ化されたのを確認します。

#### <a name="place-an-item-into-storage"></a>品目をストレージに配置する

1. モバイル デバイスを開き、倉庫 63 にログインして **在庫 \>調整** に移動します。
1. **Loc** = *SHORT-01* と入力します。 新規ライセンス プレートを **品目** = *A0001* と **数量** = *1 個* で作成します。
1. **OK** を選択します。 "品目 A0001 が場所の指定した分析コードに合わないため、場所 SHORT-01 に失敗しました" というエラーが表示されます。 これは、製品の *ストレージ* タイプ分析コードが、場所プロファイルで指定された分析コードよりも大きいためです。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
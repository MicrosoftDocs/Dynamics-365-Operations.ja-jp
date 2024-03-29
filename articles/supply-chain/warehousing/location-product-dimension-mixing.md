---
title: 場所の製品分析コードの混在
description: この記事では、場所の製品分析コードの混在に関する情報を提供します。 この場所プロファイルの機能は、ファッション業界などで、製品バリアントまたは分析コードを持つ製品を使用した場合に、場所の管理を改善するのに役立ちます。 特定の場所のプロファイルに対して、構成、色、スタイル、およびサイズを混在させることができるかどうか、またはこれらの分析コードのいずれかまたはそれらの組み合わせを同じ場所に配置できるかどうかを決定できます。
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 9daf6061d56ef004753114aaffa8eb580cea1186
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885728"
---
# <a name="location-product-dimension-mixing"></a>場所の製品分析コードの混在

[!include [banner](../includes/banner.md)]

場所の製品分析コードの混合は、ファッション業界などで、製品バリアントまたは分析コードを持つ製品を使用した場合に、場所の管理を改善するのに役立つ場所プロファイルの機能です。 特定の場所のプロファイルに対して、構成、色、スタイル、およびサイズを混在させることができるかどうか、またはこれらの分析コードのいずれかまたはそれらの組み合わせを同じ場所に配置できるかどうかを決定できます。

## <a name="turn-the-location-product-dimension-mixing-feature-on-or-off"></a>場所の製品分析コードの混合機能オンまたはオフにする

この記事で説明する機能を使用するには、システムの *場所の製品分析コードの混在* 機能をオンにする必要があります。 Supply Chain Management 10.0.25 では、この機能は必須なため、オフにすることはできません。 10.0.25 より以前のバージョンを使用している場合、管理者は [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースで *場所の製品分析コードの混在* 機能を検索して、この機能をオンまたはオフにすることができます。

## <a name="setup"></a>設定

倉庫の場所は、場所のプロパティに関連したプロファイルを有している必要があります。 そのため、同じ場所プロファイルを使用するすべての場所では、設定後に製品分析コードの混合を許可できます。

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>製品分析コードの混合を許可するための場所プロファイルの構成

1. **倉庫管理 \> 設定 \> 倉庫 \> 場所プロファイル** に移動します。
1. 場所プロファイルの一覧で **バルク** を選択します。
1. アクション ウィンドウで、**編集** を選択します。
1. **一般** クイック タブで、**場所の製品分析コード固有の混合を有効にする** オプションを *はい* に設定します。

    > [!NOTE]
    > **品目の混合を許可する** オプションが *いいえ* に設定されている場合にのみ、このオプションを *はい* に設定できます。

1. **許可された製品分析コードの混合** クイック タブで、**サイズ** オプションを *はい* に設定します。 この記事で説明するシナリオでは、異なる **サイズ** 分析コードが設定されている製品に対してのみ混合を実行できます。 ただし、他のオプションも使用可能です。
1. **保存** を選択します。

### <a name="create-a-new-product-master-and-product-variants"></a>新しい製品マスターおよび製品バリアントの作成

1. **製品情報管理 \> 製品 \> 製品マスター** に移動します。
1. アクション ウィンドウで、**新規** を選択して新しい製品マスターを作成します。
1. **新しい製品** ダイアログ ボックスに次の値を設定します。

    - **製品タイプ :** *品目*
    - **製品サブタイプ :** *製品マスター*
    - **製品番号 :** *B0001*
    - **製品名:** *B0001 サイズ*
    - **製品分析コード グループ :** *サイズ*
    - **構成テクノロジ :** *事前に定義されたバリアント*

1. **OK** を選択します。
1. **製品の詳細** ページの、**一般** クイック タブで、次の値を設定します。

    - **バリアントの自動生成 :** *はい*
    - **サイズ グループ :** *CASUALDHIR*

1. 事前に定義されたバリアントを表示するには、アクション ウィンドウで **製品バリアント** を選択します。

    **製品バリアント** ページが表示され、サイズ グループの構成のバリアント一覧が表示されます。

### <a name="release-products-to-the-usmf-company"></a>USMF 会社に製品をリリースする

1. アクション ウィンドウで、**製品のリリース** を選択します。
1. **リリースする製品の選択** ページで、製品番号 *B0001* が一覧に表示されていることを確認し、**次へ** を選択します。
1. **次へ** を選択して、リリースする製品バリアントを確認します。
1. **リリースする会社を選択** ページで *USMF* を選択し、**次へ** を選択して選択を確定します。
1. **選択の確認** ページで、**完了** を選択してリリースを完了します。

    「処理が完了しました」というメッセージが表示されます。

### <a name="update-a-released-product-in-the-usmf-company"></a>USMF 会社のリリースされた製品を更新する

1. **USMF** 会社にサイン インしていることを確認してください。
1. **製品情報管理 \> 製品 \> リリース済製品** の順に選択して、リリース済の製品の作成を完了します。
1. 品目番号 *B0001* を検索して選択し、**リリース済製品の詳細** ページを開きます。
1. アクション ウィンドウで、**編集** を選択します。
1. **一般** クイック タブで、**品目モデル グループ** フィールドが *FIFO* に設定されていることを確認します。
1. アクション ウィンドウで、**製品** タブの **設定** グループで、**分析コード グループ** を選択します。
1. 次の値を設定します。

    - **保管分析コード グループ :** *Ware*
    - **追跡用分析コード グループ :** *なし*

1. **OK** を選択します。
1. アクション ウィンドウで、**製品** タブの **設定** グループで、**引当階層** を選択します。
1. **引当階層** フィールドを *既定値* に設定し、**OK** を選択します。
1. **一般** クイック タブの **管理** セクションで、選択内容が更新されていることを確認します。
1. **購入** クイック タブの **価格** フィールドに *10* と入力します。
1. **品目グループ** フィールドの **原価の管理** クイック タブで、*オーディオ* と入力します。
1. **購入** クイック タブの **価格** フィールドに *10* と入力します。
1. **倉庫** クイック タブの **単位順序グループ ID** フィールドに、*ea* と入力します。
1. **保存** を選択します。

### <a name="create-a-location-directive"></a>場所のディレクティブを作成する

1. **倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。
1. 左ウィンドウの **作業指示書タイプ** フィールドで *発注書* を選択します。
1. 一覧で、*24 PO Direct* という名前の場所ディレクティブを選択します。
1. **場所ディレクティブ アクション** クイック タブで、**新規** を選択してグリッドに明細行を追加します。
1. 新しい明細行で、次の値を設定します。

    - **シーケンス番号 :** *1*

        新しい明細行は、既に存在する明細行の前にある必要があります。 変更を加えるには、ツール バーの **上へ移動** または **下へ移動** ボタンを使用するか、既存の明細行の **シーケンス番号** 値を *2* に変更します。

    - **名前 :** *バルク場所プロファイルに配置*
    - **固定の場所の使用 :** *固定の場所および固定されていない場所*
    - **マイナス在庫を許可 :** *このチェック ボックスをオフにする (許可しない)*
    - **バッチが有効 :** *このチェックボックスをオフにする (許可しない)*
    - **戦略 :** *なし*

1. 新しい明細行が選択されたままの状態で、グリッドの上にある **クエリの編集** を選択します。
1. 製品クエリ ダイアログ ボックスの **範囲** タブで **追加** を選択して、グリッドに明細行を追加します。
1. 新しい明細行で、次の値を設定します。

    - **テーブル:** *場所*
    - **派生テーブル :** *場所*
    - **フィールド:***場所のプロファイル ID*
    - **基準:** *BULK*

1. **OK** を選択します。
1. **場所ディレクティブ** ページで、**保存** を選択します。

> [!NOTE]
> **場所ディレクティブ アクション** クイック タブの **戦略** フィールドで、 *連結* 場所戦略を使用すると、**場所のプロファイル** の **許可された製品分析コードの混合** の設定が上書きされ、この動作が設定で許可されていない場合でも、品目は同じ場所に配置されます。

### <a name="create-a-mobile-device-menu-item"></a>品目のモバイル デバイス メニューの作成

1. **倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。
1. アクション ウィンドウで、**新規** を選択して、並べ替えに使用するメニュー項目を作成します。
1. ヘッダーで、次の値を設定します。

    - **メニュー項目名 :** *発注書明細行受取*
    - **タイトル :** *発注書明細行受取*
    - **モード:** *作業*
    - **既存の作業を使用する :** *いいえ*

1. **一般** クイック タブで、次の値を設定します。

    - **作業の作成プロセス :** *購買注文明細行の受取とプットアウェイ*
    - **ライセンスプレートの生成:** *はい*

1. **保存** を選択します。

### <a name="configure-the-mobile-device-menu"></a>モバイル デバイスのメニューの構成

1. **倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー** の順に移動します。
1. メニューの一覧で **入庫** を選択します。
1. アクション ウィンドウで、**編集** を選択します。
1. **使用可能なメニューとメニュー項目** の一覧で、**発注書明細行受取** メニュー項目を検索して選択します。
1. 右矢印ボタンを選択して、**発注書明細行受取** メニュー項目を **メニュー構造** の一覧に移動します。 このようにして、選択したメニューに新しいメニュー項目を追加します。
1. **保存** を選択します。

## <a name="scenario"></a>シナリオ

このデモ シナリオでは、場所プロファイルで品目の混合が許可されていない場合でも、 *場所の製品分析コードの混合* 機能が有効になっている場合に、どのように 2 つの異なる製品バリアントを同じ場所に配置できるかについて説明します。 この場合は、**サイズ** バリアントを基準として使用します。

開始する前に、*バルク* 場所プロファイルを使用する空の場所が倉庫 *24* にあることを確認してください 。

### <a name="create-a-purchase-order"></a>発注書の作成

次の 3 つの明細行がある発注書を作成します。同じ製品番号で異なる **サイズ** バリアントの 2 つの明細行と、バリアントを持たない異なる製品の 3 番目の明細行です。

1. **買掛金勘定 \> 発注書 \> すべての発注書** に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **発注書の作成** ダイアログ ボックスで、次の値を設定します。

    - **仕入先勘定 :** *1001*
    - **倉庫:** *24*

1. **OK** を選択します。
1. 発注書が作成され、**発注書明細行** クイック タブに新しい明細行が追加されます。 発注書番号をメモします。
1. 新しい明細行で、次の値を設定します。

    - **品目番号:** *B0001*
    - **サイズ** *L*
    - **数量:** *2*

1. グリッドの上の **明細行の追加** を選択して、2 つ目の発注書明細行を追加し、次の値を設定します。

    - **品目番号:** *B0001*
    - **サイズ** *XL*
    - **数量:** *2*

1. **明細行の追加** を選択して、3 つ目の発注書明細行を追加し、次の値を設定します。

    - **品目番号:** *A0001*
    - **数量:** *1*

1. **保存** を選択します。

### <a name="receive-purchase-order-lines-in-the-warehouse-management-mobile-app"></a>倉庫管理モバイル アプリで発注書明細行を受領する

1. 倉庫 *24* を有効にしたユーザーとして、倉庫管理モバイル アプリにログインします。
1. **入庫** メニューを選択します。
1. **発注書明細行受取** を選択します。
1. **PONUM** フィールドを選択してから、発注書番号を入力します。
1. 入力を確認するには、ページの下部にある確認ボタン (✔) を選択します。
1. 入庫する発注書の明細行番号を入力します。 **LINENUM** フィールドを選択し、数字パッドを使用して *1* を入力します。
1. 入力内容を確認します。
1. 入庫する数量を入力します。 プラス記号 (**+**) ボタンを2回選択すると、**数量** フィールドの値が *2* に増加します。
1. 入力内容を登録するには、ページの下部にあるボタン (✔) を選択し、ボタン (✔) をもう一度選択して入力内容を確認します。
1. **発注書 : 配置** ページの情報を表示します。 このページには、プットアウェイ (作業 1) のために作成された作業が表示されます。

    入庫品目がプットアウェイされる場所、ライセンス プレート、品目、サイズ、および完了した **発注書明細行受取** の数量が表示されます。

1. プットアウェイ作業を確認します。
1. ステップ 4 ~ 11 を、発注書明細行 2 に対して繰り返します。 ただし、手順 8 では *1* の数量を指定します。

    作業 1 と同じ場所に新しいプットアウェイ作業 (作業 2) が作成されます。

1. ステップ 4 ~ 11 を、発注書明細行 2 に対して再度繰り返します。 ただし、手順 8 では *1* の残りの数量を指定します。

    作業 1 および 2 と同じ場所に新しいプットアウェイ作業 (作業 3) が作成されます。 この挙動の仕組みとしては、*連結* 場所ディレクティブ戦略が使用されており、*バルク***場所プロファイル** 設定の **許可された製品分析コードの混合** クイック タブにより、**サイズ** バリアントを 1 つの場所に混在させることができるためです。

1. ステップ 4 ~ 11 を、発注書明細行 3 に対して繰り返します。 手順 8 では、品目番号 *A0001* に *1* の数量を指定します。

    新しいプットアウェイ作業 (作業 4) は、発注書明細行 1 および 2 に使用される場所とは別の場所に作成されます。 この挙動は、場所プロファイルでは製品の混合が許可されていませんが、同じ製品マスターの分析コードの混合は許可されているために発生します。

1. ページの上部にあるメニュー ボタン (ハンバーガー またはハンバーガー ボタンと呼ばれることもあります) を選択し、**キャンセル** を選択して、**発注書明細行の受取** を終了します。

> [!TIP]
> このシナリオを繰り返すことができますが、今回は、*バルク***場所プロファイル** の、**製品分析コードの混合を許可する** クイック タブの下にある **サイズ** - *いいえ* を設定して、どの製品分析コードも混合しないようにします。 この場合、発注書の受取の際に、各製品バリアントが新しい場所に配置されます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
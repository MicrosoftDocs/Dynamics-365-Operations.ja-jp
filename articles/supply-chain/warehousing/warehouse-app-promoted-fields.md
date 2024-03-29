---
title: Warehouse Management モバイル アプリの手順に昇格したフィールドを構成する
description: この記事では、Warehouse Management モバイル アプリのタスク フローで任意のステップに対して特定情報のレベルを上げてハイライトする方法について説明します。
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepSelectPromotedFields, WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour, WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e2d65f20febaf9bd1d143414054b121f8decb7c0
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689833"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Warehouse Management モバイル アプリの手順に昇格したフィールドを構成する

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> この記事で説明する機能は、新しい Warehouse Management モバイル アプリにのみ適用されます。 これらは非推奨となっている古い倉庫アプリには影響しません。

この記事では、Warehouse Management モバイル アプリのタスク フローで任意のステップに対して特定情報のレベルを上げてハイライトする方法について説明します。 この機能は、作業者がフローに沿って作業をおこなう際に、最も重要なフィールドで彼らの注意に注目する手助けができます。 各プロセスの各手順で、管理者はどのフィールドのレベルを上げるのか、どのフィールドを強調表示するのかを選択できます。

## <a name="enable-promoted-fields-in-your-system"></a>自分のシステムで昇格したフィールドを有効にする

Supply Chain Management バージョン 10.0.28 以前を実行している場合、昇格したフィールドを設定できるようになる前に、次の手順を完了して、Warehouse Management モバイル アプリで必要な機能を有効にして、必須フィールド名を生成する必用があります。 Supply Chain Management バージョン 10.0.29 以降を実行している場合、これらの機能は必須であり、オフにできないので、この手順を省略できます。

1. **システム管理者 \> ワークスペース \> フィーチャー管理** の順に移動します。 このページの詳細については、[機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。
1. システムで *倉庫アプリのステップ指示* 機能が有効になっていることを確認します。 この機能は、*Warehouse Management アプリの昇格したフィールド* 機能の前提条件です。 Supply Chain Management バージョン 10.0.29 の場合、これはは必須でオフにすることはできません。 *倉庫アプリのステップの手順* 機能の詳細については、[Warehouse Management モバイル アプリ](mobile-app-titles-instructions.md) を参照してください。
1. システムで *倉庫アプリのプロモーション フィールド* 機能が有効になっていることを確認します。 これは、この記事で説明する機能です。 Supply Chain Management バージョン 10.0.29 の場合、これはは必須でオフにすることはできません。
1. **Warehouse Management \> 設定 \> モバイル デバイス \> Warehouse アプリのフィールド名** の順に移動して、**デフォルト設定を作成する** を選択することで Warehouse Management mobile アプリのフィールド名を更新します。 Warehouse Management モバイル アプリを使用する法人 (会社) ごとにこの手順を繰り返します。 詳細情報については、[Warehouse Management モバイル アプリのフィールドを構成する](configure-app-field-names-priorities-warehouse.md) を参照してください。

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>メニュー特定のオーバーライドで昇格したフィールドを構成する

昇格したフィールドを設定するには、次の手順を使います。

1. [Warehouse Management モバイルアプリのステップ タイトルと手順のカスタマイズ](mobile-app-titles-instructions.md) で説明されている手順とメニュー固有の上書きを作成します 。
1. **ステップ ID** と **メニュー項目名** の値の組み合わせを検索し、**ステップ ID** 列で値を選択します。
1. 表示されたページで、**昇格したフィールドを選択** クイック タブで、ツールバーの **フィールドの選択** を選択します。
1. **昇格されたフィールド** ダイアログ ボックスで、レベルを上げたいフィールドを選択します。 また、選択したフィールドは 2 つまで強調表示できます。 強調表示されたフィールドは、Warehouse Management モバイル アプリで太字で表示されます。 フィールドを選択する際、一部のスクリーンは昇格されたフィールドを 1 つか 2 つだけ表示できる大きさであることに注意してください。 これらの設定を使用する方法を示す例については、この記事の後のシナリオを参照してください。

    > [!NOTE]
    > **使用可能なフィールド** リストは、メニュー項目に表示できるフィールドに限定されています。 ただし、他の要因 (品目構成など) によって、フィールドが実際に Warehouse Management モバイル アプリに表示されるかどうかが決ります。 昇格したフィールドを構成した場合は、選択したフィールドだけが Warehouse Management モバイル アプリのメイン ページに表示されます。 ただし、作業員は、詳細ページを変更することで残りのフィールドを表示できます。

1. **OK** を選択して設定を適用します。 選択したフィールドが **昇格されたフィールドを選択** クイック タブに表示されます。

## <a name="example-scenario"></a>シナリオ例

### <a name="enable-sample-data"></a>サンプルデータの有効化

指定されたサンプル レコードと値を使用してこのシナリオ全体を実行するには、標準の[デモ データ](../../fin-ops-core/fin-ops/get-started/demo-data.md)がインストールされているシステムを使用する必要があります。 開始する前に、**USMF** 法人も選択する必要があります。

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>ライセンス プレート上に昇格したステップで販売ピッキングを構成する

この手順では、ライセンス プレート ステップの **販売ピッキング** メニュー項目に昇格したフィールドと強調表示されたフィールドを設定します。

1. **倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのステップ** の順に移動します。
1. *LicensePlateId* という名前のステップ ID を検索して選択します。
1. アクション ウィンドウで、**ステップ構成の追加** を選択します。
1. ドロップダウン ダイアログ ボックスで、*メニュー品目* フィールドを使用して **販売ピッキング** を検索および 選択します。
1. **OK** を選択します。
1. 作成した上書きの詳細ページが表示されます。 **昇格したフィールドの選択** クイック タブで、ツール バーの **フィールドの選択** を選択します。
1. **昇格したフィールド** ダイアログ ボックスで、昇格するフィールドと強調表示するフィールドを選択できます。 **使用できるフィールド** の一覧で、次のフィールドを見つけて選択し、ボタンを使用して **選択されたフィールド** の一覧に移動します。

    - 場所
    - 品目
    - 製品名
    - 在庫状態

1. 上矢印および下矢印ボタンを使用して、**選択したフィールド** 一覧内のフィールドの順序をカスタマイズします。 Warehouse Management モバイル アプリでは、フィールドが設定した順序で表示されます。
1. **場所** フィールドを選択し、**強調表示** を選択します。
1. **OK** を選択して、構成を保存します。

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>Warehouse Management モバイル アプリの昇格されたフィールドを表示する

この手順では、Warehouse Management モバイル アプリを開き、手順に従って、前の手順で昇格および強調表示したフィールドを表示します。

1. Microsoft Dynamics 365 Supply Chain Management で、追跡されるライセンス プレートで指定されている場所からピックするピック ステップが必要になる販売注文を作成します。 その後倉庫に販売注文をリリースします。 生成された作業 ID をメモします。
1. Warehouse Management モバイル アプリを開いて、倉庫 24 にサインインします。 (標準デモ データでは、ユーザー IDとして *24*、パスワードとして *1* を使用してサインインします。)
1. **出荷** メニューを選択し、**販売ピッキング** メニュー品目を選択します。
1. 画面のデータ入力指示に従って、手順 1 で生成された作業 ID を入力します。
1. **ライセンス プレートをスキャンする** という内容のステップでは、詳細ページに加えた変更が表示されます。 このフィールドは、昇格したフィールドに対して設定した順序で表示され、**場所** フィールドは太字で表示されます。

---
title: ウェーブ ラベルの再印刷と無効化
description: この記事では、既存のウェーブ ラベルを無効にして再印刷する方法について説明します。
author: perlynne
ms.date: 07/09/2020
ms.topic: article
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSWaveTableListPage, WHSWorkException, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelLayout, WHSWaveLabelType, WHSWaveLabelTemplateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: f9f057d9985fb8431ec7c9ced23f2cd3c476570d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871836"
---
# <a name="reprint-and-void-wave-labels"></a>ウェーブ ラベルの再印刷と無効化

[!include [banner](../includes/banner.md)]

この記事では、ウェーブ処理によって生成されるラベルを管理する方法について説明します。 (詳細な説明と構成手順については、[ウェーブ ラベル印刷のコンフィギュレーション](../warehousing/configure-wave-label-printing.md) を参照してください。)

ウェーブ ラベルは、いつでも再印刷できます。 たとえば、既存のラベルが紛失または破損した場合、1 枚のラベルを印刷する必要が生じる場合があります。 または、一連のウェーブ ラベル全体の数および/または構成が変更された場合 (例えば、在庫不足やその他の理由などによって)、倉庫の作業者または監督は、ラベルのロール全体を再印刷する必要が生じる場合があります。 多くの場合、カートン数だけが変更された場合でも、各ラベルの "カートン X/Y" セクションで正確な合計数を維持するために、ロール全体を再印刷する必要があります。

ウェーブ ラベルの再印刷機能は、次の機能をサポートしています:

- 倉庫管理アプリとリッチ クライアントの両方からラベルを再印刷します。
- ラベルを無効にして、同時に再印刷します。 (たとえば、ラベルを無効にする機能は、ショート ピックのシナリオに組み込まれています。)
- ウェーブ ラベル履歴をクリーンアップします。

この記事では、ウェーブ ラベルの再印刷機能を使用する方法を例を挙げて示すシナリオをまとめて紹介します。

> [!IMPORTANT]
> この記事で説明するシナリオを実行するには、[ウェーブ ラベル印刷のコンフィギュレーション](../warehousing/configure-wave-label-printing.md) で説明されているように、最初に関連するウェーブ印刷機能をオンにし構成する必要があります。 この記事のいくつかのシナリオでは、最初にその記事のシナリオを実行して、前提条件のサンプル データを生成する必要があります。

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>シナリオ 1: Web クライアントからラベルを再印刷する

次のページから、ウェーブ ラベルを表示および再印刷できます。 各ページのアクション ペインにある **出荷** タブの **関連情報** グループで、**ウェーブ ラベル** を選択します。

- すべての出荷 \> 出荷詳細
- すべての貨物 \> 貨物の詳細
- すべてのウェーブ
- ウェーブ ラベル
- ウェーブ ラベル履歴

Web クライアントからウェーブ ラベルを再印刷するには、次の手順を実行します。

1. **倉庫管理 \> 出庫ウェーブ \> 出荷ウェーブ \> すべてのウェーブ** の順に移動します。
1. ラベルを再印刷するウェーブを選択します。
1. アクション ペインにある **ウェーブ** タブの **印刷** グループで、**ウェーブ ラベル** を選択します。
1. 次の手順のいずれか、または両方を実行します:

    - ラベルを再印刷するには、**プリンター名** フィールドでプリンターを選択します。 (ラベル再印刷せずにウェーブ ラベルの詳細を更新するだけの場合は、このフィールドを空白のままにします。)
    - ラベルを更新するには、**ウェーブ ラベルの詳細の更新** チェック ボックスを選択します。 (前のラベルを再印刷するだけの場合は、このチェック ボックスをオフのままにします。)

    > [!NOTE]
    > ウェーブ ラベルが印刷または再印刷されるたびに、そのデータは適切なウェーブ ラベル レイアウトによって変換され、すべてのプレースホルダーが実際の値に置き換えられます。 結果の文字列は、ウェーブ ラベル履歴にレコードとして保存されます。 **ウェーブ ラベルの詳細の更新** チェック ボックスがオフの場合、ラベルの再印刷時に、保存されている Zebra プログラミング言語 (ZPL) データが使用されます。 **ウェーブ ラベルの詳細の更新** チェック ボックスがオンの場合、新しい文字列が生成されます。 既存のウェーブ ラベルも再計算され、余分なラベル (たとえば、関連する作業明細行がキャンセルまたは変更された場合など) が **無効** としてマークされ、再印刷されません。

1. **OK** を選択して、選択を確定します。

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>シナリオ 2: 倉庫管理アプリからラベルを再印刷する

このシナリオは通常、ラベル ロールが紛失または破損した場合に適用されます。 従業員が 1 枚のラベルと複数のラベルを再印刷できるように、モバイル デバイスのメニュー項目を設定する方法を示す例を提供します。 次に、モバイル デバイスで作業中に、これらの新しいメニュー項目を使用する方法を示します。

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>モバイル デバイスに必要なメニュー項目とメニューを設定する

作業者がモバイル デバイスからラベルを再印刷する前に、この機能を提供するメニュー項目を設定して、それらの項目を倉庫管理アプリ メニューに追加する必要があります。

#### <a name="create-new-mobile-device-menu-items"></a>新しいモバイル デバイス メニュー項目を作成する

次の手順に従って、倉庫管理アプリからラベルを再印刷するためのメニュー項目の新しいコレクションを作成します。

1. **倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。
1. メニュー項目を作成し、次の値を設定します:

    - **メニュー項目名:** *1 枚のウェーブ ラベルを再印刷*
    - **タイトル:** *1 枚のウェーブ ラベルを再印刷*
    - **モード:** *間接*
    - **活動コード:** *1 枚のウェーブ ラベルを再印刷*

1. 2 番目のメニュー項目を作成し、次の値を設定します:

    - **メニュー項目名:** *ラベルを再印刷 (品目)*
    - **タイトル:** *ウェーブ ラベルを再印刷 (品目)*
    - **モード:** *間接*
    - **活動コード:** *複数のウェーブ ラベルを再印刷*
    - **作業一覧のグループ化フィルターの表示:** *はい*
    - **システム グループ化フィールド:** *ShipmentID*
    - **システム グループ化ラベル:** *出荷 ID*
    - **印刷モード:** *製品*

1. アクション ペインで **フィールド リスト** を選択すると、作業者が正しいラベルロールを識別できるように表示されるフィールドを選択できるページを開きます。
1. 最大 7 つのフィールドを表示できます。 ドロップダウン リストを使用して、使用可能な各位置に表示されるフィールドを選択します。 不要なフィールドは空白のままにします。 

    次に例を示します。

    - **表示フィールド:** *LabelItemId*
    - **表示フィールド 2:** *LabelItemName*
    - **表示フィールド 3:** *InventQty*
    - **表示フィールド 4:** *LabelUnitId*

1. ページを閉じます。
1. 3 番目のメニュー項目を作成し、次の値を設定します:

    - **メニュー項目名:** *ラベルを再印刷 (Enum)*
    - **タイトル:** *ウェーブ ラベルを再印刷 (Enum)*
    - **モード:** *間接**
    - **活動コード:** *複数のウェーブ ラベルを再印刷*
    - **作業一覧のグループ化フィルターの表示:** *はい*
    - **システム グループ化フィールド:** *ShipmentID*
    - **システム グループ化ラベル:** *出荷 ID*
    - **印刷モード:** *列挙型*

1. アクション ペインで、**フィールド リスト** を選択し、ドロップダウン リストを使用して、作業者が正しいラベル ロールを識別できるように表示されるフィールドを選択します (たとえば、*LabelItemId*、*LabelItemName*、*InventQty*、*LabelUnitId*、および *NumberOfLabels*)。
1. ページを閉じます。
1. 4 番目のメニュー項目を作成し、次の値を設定します:

    - **メニュー項目名:** *ラベルを再印刷 (最後)*
    - **タイトル:** *ウェーブ ラベルを再印刷 (最後)*
    - **モード:** *間接*
    - **活動コード:** *複数のウェーブ ラベルを再印刷*
    - **作業一覧のグループ化フィルターの表示:** *はい*
    - **システム グループ化フィールド:** *ShipmentID*
    - **システム グループ化ラベル:** *出荷 ID*
    - **印刷モード:** *最後の正常なウェーブ ラベル ID*

1. アクション ペインで、**フィールド リスト** を選択し、ドロップダウン リストを使用して、作業者が正しいラベル ロールを識別できるように表示されるフィールドを選択します (たとえば、*LabelItemId*、*LabelItemName*、*InventQty*、*LabelUnitId*、および *NumberOfLabels*)。
1. ページを閉じます。

#### <a name="set-up-the-mobile-device-menu"></a>モバイル デバイス メニューを設定する

新しいメニュー項目を倉庫管理アプリ メニューに追加するには、次の手順に従います。

1. **倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー** の順に移動します。
1. 既存の **出荷** メニューを選択します。
1. 左側の一覧で、作成したばかりの再印刷メニュー項目を見つけ、右矢印ボタンを使用して右側の一覧に追加します。
1. ページを閉じます。

### <a name="use-cases"></a>ユース ケース

ここで説明するユース ケースは、作業者がウェーブ ラベルを再印刷できるように設定したさまざまなモバイル デバイス メニュー項目の使用方法を示す例を示しています。

これらのユース ケースを実行する前に、次の前提条件を満たす必要があります:

- デモ データをインストールし、**USMF** 法人を選択する必要があります。
- [ウェーブ ラベル印刷のコンフィギュレーション](../warehousing/configure-wave-label-printing.md) で説明されているように、ウェーブ ラベルの印刷を構成し、いくつかのラベルを生成する必要があります。

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>ユース ケース 2.1: 1 枚のウェーブ ラベルに傷があり、再印刷する必要があります。

1. 倉庫 *62* にアクセスするユーザーとして倉庫管理アプリにサインインします。 (標準デモ データでは、ユーザー ID *62* とパスワード *1* を使用してサインインできます。)
1. **出荷 \> 1 枚のウェーブ ラベルを再印刷** に移動します。
1. ウェーブ ラベル ID を入力またはスキャンします。
1. 再印刷するプリンターを選択します。
1. **OK** を選択してアクションを確定します。

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>ユース ケース 2.2: 同一品目の複数の箱のいくつかのラベルが破損しており、再印刷が必要です。 各ラベルには製品バー コードがありますが、列挙または SSCC 番号はありません。

1. 倉庫 *62* へのアクセス権を持つユーザーとして倉庫管理アプリにサインインします。 (標準デモ データでは、ユーザー ID *62* とパスワード *1* を使用してサインインできます。)
1. **出荷 \> ラベルを再印刷 (品目)** に移動します。
1. 出荷 ID を入力またはスキャンします。
1. 再印刷する正しいラベル ロールのあるタイルを選択します。
1. 既存のラベルから製品バー コードをスキャンして、正しい明細行が選択されていることを確認します。
1. 再印刷するラベルの数を入力します。
1. 再印刷するプリンターを選択します。
1. **OK** を選択してアクションを確定します。

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>ユース ケース 2.3: プリンターの紙詰まりのため、箱のラベルの一部が印刷されませんでした。 ラベルには列挙があるので、再印刷するカートンの範囲を定義できます。

1. 倉庫 *62* へのアクセス権を持つユーザーとして倉庫管理アプリにサインインします。 (標準デモ データでは、ユーザー ID *62* とパスワード *1* を使用してサインインできます。)
1. **出荷 \> ラベルを再印刷 (Enum)** に移動します。
1. 出荷 ID を入力またはスキャンします。
1. 再印刷する正しいラベル ロールのあるタイルを選択します。
1. ラベルを再印刷する最初のカートンを入力します。
1. ラベルを再印刷する最後のカートンを入力します。 または、このフィールドを空白のままにして、指定した最初のカートンの後にあるすべてのカートンのラベルを再印刷します。
1. 再印刷するプリンターを選択します。
1. **OK** を選択してアクションを確定します。

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>ユース ケース 2.4: プリンターの紙詰まりのため、箱のラベルの一部が印刷されませんでした。 最後の正常なラベルには、バー コードとして印刷されるウェーブ ラベル ID があります。

1. 倉庫 *62* へのアクセス権を持つユーザーとして倉庫管理アプリにサインインします。 (標準デモ データでは、ユーザー ID *62* とパスワード *1* を使用してサインインできます。)
1. **出荷 \> ラベルを再印刷 (最後)** に移動します。
1. 出荷 ID を入力またはスキャンします。
1. 再印刷する正しいラベル ロールのあるタイルを選択します。
1. 最後の正常なウェーブ ラベルのウェーブ ラベル ID を入力またはスキャンします。 アプリは、ラベルが再印刷される最初のカートンとしてシーケンスの次のラベルを識別します。
1. ラベルを再印刷する最後のカートンを入力します。 または、このフィールドを空白のままにして、指定した最初のカートンの後にあるすべてのカートンのラベルを再印刷します。
1. 再印刷するプリンターを選択します。
1. **OK** を選択してアクションを確定します。

## <a name="scenario-3-short-pick-and-reprint"></a>シナリオ 3: ショート ピックと再印刷

このシナリオを実行する前に、次の前提条件を満たす必要があります:

- デモ データをインストールし、**USMF** 法人を選択する必要があります。
- [ウェーブ ラベル印刷のコンフィギュレーション](../warehousing/configure-wave-label-printing.md) で説明されているように、ウェーブ ラベルの印刷を構成し、いくつかのラベルを生成する必要があります。

### <a name="set-up-work-exceptions"></a>作業例外を設定します

作業例外は、ショート ピッキングの動作を制御します。 以下の手順に従って、作業例外を設定します。

1. **倉庫管理 \> 設定 \> 作業 \> 作業例外** の順に移動します。
1. 以下の設定をしたレコードを作成します:

    - **作業例外コード:** *ショート ピックと印刷*
    - **例外タイプ:** *ショート ピック*
    - **ウェーブ ラベルの再印刷を提案:** *はい*

### <a name="void-and-reprint-after-a-short-pick"></a>ショート ピック後に、無効にして再印刷する

1. 倉庫 *62* へのアクセス権を持つユーザーとして倉庫管理アプリにサインインします。 (標準デモ データでは、ユーザー ID *62* とパスワード *1* を使用してサインインできます。)
1. 最初にウェーブ ラベルが印刷されていたときに作成された販売注文作業の作業処理フローを開きます。
1. **ショート ピック** を選択します。
1. このシナリオに対して作成した作業例外コードを選択します。
1. 正しい例外を選択した場合は、**無効にして再印刷** チェック ボックスが使用可能になります。 このボックスを選択にして確定します。 確定すると、**ラベル ビルド ID** フィールドで識別されるラベル ロール シーケンス は、変更された作業明細行の数量に基づいて再計算されます。 その後、指定されたプリンターで再印刷されます。

## <a name="additional-resources"></a>追加リソース

- [サイクル ラベル印刷](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
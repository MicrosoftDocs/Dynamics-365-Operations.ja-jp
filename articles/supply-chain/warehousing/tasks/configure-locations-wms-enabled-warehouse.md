---
title: WMS に対応した倉庫の場所のコンフィギュレーション
description: このガイドでは、新しい WMS に有効な倉庫 (倉庫管理プロセス (WMS) を使用する倉庫) の場所の設定をコンフィギュレーションする方法を示します。
author: perlynne
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cce7ea0c06938d2ce038853a262f843ec76fe4c
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219661"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>WMS が有効な倉庫での場所のコンフィギュレーション

[!include [banner](../../includes/banner.md)]

このガイドでは、新しい WMS に有効な倉庫 (倉庫管理プロセス (WMS) を使用する倉庫) の場所の設定をコンフィギュレーションする方法を示します。 通常、このプロセスを実行するのは倉庫マネージャーです。 このガイドは、デモ データの会社 USMF で、または独自のデータで実行できます。 少なくとも 1 つのサイトがコンフィギュレーションされていることが前提条件です。


## <a name="create-a-new-warehouse"></a>新しい倉庫の作成
1. **ナビゲーション ウィンドウ > モジュール > 在庫管理 > 設定 > 在庫詳細 > 倉庫** の順に移動します。
2. **新規** をクリックします。
3. **倉庫** フィールドに値を入力します。
4. **名前** フィールドに値を入力します。
5. **サイト** フィールドで、既存のサイトの値を選択、または入力します。
6. **倉庫** セクションを展開します。
7. **倉庫管理プロセスの使用オプション** を「はい」に設定します。 この設定により、倉庫作業やモバイル デバイスを使用して、倉庫管理プロセス (WMS) を実行することができます。
8. ページを閉じます。

## <a name="define-a-location-format"></a>場所形式の定義
1. **ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > 倉庫 > 場所形式** の順に移動します。 場所形式は、倉庫内で使用されるさまざまな場所の在庫置場の位置に、固有の一貫した名前を作成するために使用するネーミング方式です。 通路番号などの場所のコンポーネントの識別が容易になるように、場所形式の一部として区切りを使用すると便利です。 この例では、4 つのコンポーネントで名前を作成します。 たとえば、通路、ラック、棚、および在庫置場にすることができます。
2. **新規** をクリックします。
3. **場所形式** フィールドに値を入力します。
4. **名前** フィールドに値を入力します。
5. **区分の説明** フィールドに値を入力します。 場所の名前の最初のコンポーネントが表すものについて説明します。 たとえば、「通路」にすることができます。
6. **長さ** フィールドに数値を入力します。 これにより、場所の名前のこの部分の文字数が決まります。 名前のすべてのコンポーネントの合計が、区切りを含み、10 文字を超えることができないことに注意してください。    
7. **区切り** フィールドに値を入力します。 これにより、名前の 1 番目と 2 番目のコンポーネントの間で使用する文字や記号が決まります。  
8. **詳細** セクションで、**新規** をクリックします。
9. **区分の説明** フィールドに値を入力します。
10. **長さ** フィールドに数値を入力します。
11. **区切り** フィールドに値を入力します。
12. **詳細** セクションで、**新規** をクリックします。
13. **区分の説明** フィールドに値を入力します。
14. **長さ** フィールドに数値を入力します。
15. **区切り** フィールドに値を入力します。
16. **詳細** セクションで、**新規** をクリックします。
17. **区分の説明** フィールドに値を入力します。
18. **長さ** フィールドに数値を入力します。
19. **保存** をクリックします。
20. ページを閉じます。

## <a name="define-location-types"></a>場所のタイプの定義
1. **ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > 倉庫 > 在庫場所タイプ** の順に移動します。 在庫場所タイプは、異なる倉庫管理プロセスを制御するためのフィルター処理オプションとして使用できます。 少なくとも、出荷の倉庫管理プロセスを定義するためにステージングおよび最終配送場所タイプを作成する必要があります。 
2. **新規** をクリックします。
3. **場所** タイプ フィールドに値を入力します。
4. **説明** フィールドで、値を入力します。
5. ページを閉じます。

## <a name="define-location-profile"></a>場所プロファイルの定義
1. **ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > 倉庫 > 場所プロファイル** の順に移動します。 場所プロファイルの定義は非常に重要です。 グループ化された場所の能力は、保管される在庫と保管方法に関連するポリシーとともに、ここで制御できます。 場所プロファイルは、異なる倉庫管理プロセスを制御するためのフィルター処理オプションとして使用できます。 少なくとも、WMS を有効にするために、ユーザーの場所のプロファイルを作成する必要があります。
2. **新規** をクリックします。
3. **場所プロファイル ID** フィールドに値を入力します。
4. **名前** フィールドに値を入力します。
5. **場所形式** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、目的のレコードを見つけ、選択します。
7. 一覧で、選択された行のリンクをクリックします。
8. **場所タイプ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
9. 一覧で、目的のレコードを見つけ、選択します。
10. 一覧で、選択された行のリンクをクリックします。
11. **混合在庫状態を許可** チェック ボックスをオンまたはオフにします。 この場所プロファイルによりグループ化する場所で混合在庫状態の値を許可する場合は、このオプションを有効にします。 
12. **バッチ日数ルールの上書き** チェック ボックスをオンまたはオフにします。 このルールに従わない在庫バッチを混在できるようにし、在庫バッチの有効期限が異なる日数のルールを上書きするには、このオプションを有効にします。  
13. **循環棚卸を許可** チェック ボックスをオンまたはオフにします。 この場所プロファイルによりグループ化するすべての場所で循環棚卸プロセスを許可するには、このオプションを有効にします。 
14. **分析コード** セクションを展開または折りたたみます。 [分析コード] タブでは、各場所内の積載能力の詳細な計算を有効にするために、パラメーターと方法を定義することができます。  
15. ページを閉じます。

## <a name="enable-warehouse-management-parameters"></a>倉庫管理パラメーターの有効化
1. **ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > 倉庫管理パラメーター** の順に移動します。 倉庫の作業を処理するには、ユーザーの場所プロファイルのパラメーターでステージング場所のタイプおよび最終出荷場所タイプを設定する必要があります。定義した最終出荷場所タイプで出荷プロセスが終了するとすぐに、関連する出荷トランザクションが「ピッキング済」に更新されます。
2. **場所プロファイル** セクションを展開します。
3. **ユーザーの場所** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、選択された行のリンクをクリックします。
5. **在庫場所タイプ** セクションを展開します。
6. **ステージング場所のタイプ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、選択された行のリンクをクリックします。
8. **最終出荷場所のタイプ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
9. 一覧で、選択された行のリンクをクリックします。
10. ページを閉じます。

## <a name="define-warehouse-zone-groups"></a>倉庫ゾーン グループの定義
1. **ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > 倉庫ゾーン グループ** の順に移動します。 倉庫ゾーンは、異なる倉庫管理プロセスを制御するためのフィルター処理オプションとして使用できます。 ゾーンを定義する前に、ゾーン グループを作成する必要があります。   
2. **新規** をクリックします。
3. **ゾーン グループ ID** フィールドに値を入力します。
4. **ゾーン グループ名** フィールドに値を入力します。
5. ページを閉じます。

## <a name="define-warehouse-zones"></a>倉庫ゾーンの定義
1. **ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > 倉庫 > ゾーン** の順に移動します。
2. **新規** をクリックします。
3. **ゾーン ID** フィールドに値を入力します。
4. **ゾーン名** フィールドに値を入力します。
5. **ゾーン グループ ID** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、目的のレコードを見つけ、選択します。
7. 一覧で、選択された行のリンクをクリックします。
8. ページを閉じます。

## <a name="create-locations-using-the-location-setup-wizard"></a>場所設定ウィザードを使用した場所の作成
1. **ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 設定 > 倉庫 > 場所設定ウィザード** の順に移動します。
2. **倉庫** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、目的のレコードを見つけ、選択します。
4. 一覧で、選択された行のリンクをクリックします。
5. **ゾーン ID** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、目的のレコードを見つけ、選択します。
7. 一覧で、選択された行のリンクをクリックします。
8. **場所プロファイル ID** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
9. 一覧で、目的のレコードを見つけ、選択します。
10. 一覧で、選択された行のリンクをクリックします。
11. 一覧で、選択された行をマークします。
12. **開始番号** フィールドに数値を入力します。 [開始番号] と [終了番号] フィールドで、作成された場所の数を定義します。 たとえば、場所形式の 4 つの明細行すべてで、[開始番号] に「1」を設定し、[終了番号] に「3」を設定する場合、81 の場所が作成されます (3 x 3 x 3 x 3)。   
13. **終了番号** フィールドに数値を入力します。
14. 一覧で、目的のレコードを見つけ、選択します。
15. **開始番号** フィールドに数値を入力します。
16. **終了番号** フィールドに数値を入力します。
17. 一覧で、目的のレコードを見つけ、選択します。
18. **開始番号** フィールドに数値を入力します。
19. **終了番号** フィールドに数値を入力します。
20. 一覧で、目的のレコードを見つけ、選択します。
21. **開始番号** フィールドに数値を入力します。
22. **終了番号** フィールドに数値を入力します。
23. [作成] をクリックします。

## <a name="create-locations-manually"></a>手動での場所の作成
1. **倉庫管理 > 設定 > 倉庫 > 場所** の順に移動します。 倉庫内の場所は手動で簡単に作成できます。 場所の名前と場所プロファイル ID は、必須の値です。 
2. **新規** をクリックします。
3. **倉庫** フィールドに値を入力します。
4. **場所** フィールドで、値を入力します。 ここに新しい場所を作成する場合、既存の名前を選択するのではなく、新しい固有の名前を入力する必要があることに注意してください。
5. **場所プロファイル ID** フィールドに値を入力します。
6. ページを閉じます。

## <a name="define-pack-size-categories"></a>梱包サイズ カテゴリの定義
1. **倉庫管理 > 設定 > 倉庫 > 梱包サイズ カテゴリ** の順に移動します。 梱包サイズ カテゴリは、物理的な梱包サイズが類似している品目をグループ化するために使用できます。 この例では、梱包サイズ カテゴリは、倉庫の特定のゾーン内でのピッキング場所で能力を制御するために使用されます。 梱包サイズ カテゴリ ID は、在庫限度として使用するためにリリース済製品エンティティに割り当てる必要があることに注意してください。  
2. **新規** をクリックします。
3. **梱包サイズ カテゴリ ID** フィールドに値を入力します。
4. **梱包サイズ カテゴリ名** フィールドに値を入力します。
5. ページを閉じます。

## <a name="define-location-stocking-limits"></a>場所別在庫限度の設定
1. **倉庫管理 > 設定 > 倉庫 > 場所別在庫限度** の順に移動します。 場所別在庫限度は、在庫を配送する物理的能力がない場所に在庫の配置を要求する作業が作成されないことを確認するのに役立ちます。  
2. **新規** をクリックします。
3. **倉庫** フィールドに値を入力します。
4. **場所プロファイル ID** フィールドに値を入力します。
5. **梱包サイズ カテゴリ ID** フィールドに値を入力します。
6. **数量** フィールドに、数値を入力します。
7. **保存** をクリックします。
8. ページを閉じます。

## <a name="define-fixed-picking-locations"></a>固定のピッキング場所の定義
1. **倉庫管理 > 設定 > 倉庫 > 固定の場所** の順に移動します。 製品または製品バリアントごとに使用される場所を定義できます。 同じ倉庫内の同じ製品に複数の固定の場所を作成することができます。     
2. **新規** をクリックします。
3. **品目番号** フィールドに値を入力します。
4. **倉庫** フィールドに値を入力します。
5. **場所** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、選択された行のリンクをクリックします。
7. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

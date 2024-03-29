---
title: エンジニアリングの変更管理機能のチュートリアル
description: この記事では、エンジニアリング変更管理の使用方法を示す、エンド ツー エンドのチュートリアルを示します。
author: t-benebo
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 65ff30632a54b0b7cadbfe663698d466d41abe47
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334898"
---
# <a name="engineering-change-management-feature-walkthrough"></a>エンジニアリングの変更管理機能のチュートリアル

[!include [banner](../includes/banner.md)]

この記事では、エンジニアリング変更管理の使用方法を示す、エンド ツー エンドのチュートリアルを示します。 最も重要なシナリオは次のとおりです。

- 基本機能の構成
- エンジニアリング会社が新しいエンジニアリング製品を作成する方法
- エンジニアリング会社が社内の会社に対してエンジニアリング製品をリリースする方法
- 地域の会社がエンジニアリング会社からリリースされた製品を確認および承認する方法
- ローカル会社が標準トランザクションでエンジニアリング製品を使用する方法
- 販売注文にエンジニアリング製品を追加する方法
- エンジニアリング変更要求を作成してエンジニアリング製品に変更を依頼する方法
- エンジニアリング変更オーダーを作成して、要求された変更をスケジュールし実装する方法
- 変更された製品のリリース方法

この記事のすべての演習では、Microsoft Dynamics 365 Supply Chain Management に用意されている標準的なサンプル データを使用します。 また、各手順は前の手順に基づいて構築されています。 したがって、特にエンジニアリング変更管理機能を使用したことがない場合は、最初から最後までのこの演習をおこなうことをお勧めします。 これにより、この機能を完全に理解することができます。

## <a name="set-up-for-the-sample-scenario"></a>このサンプル シナリオに設定する

この記事で説明されているサンプル シナリオに従うには、最初にデモ データを使用できるようにし、いくつかのカスタム レコードを追加して、機能を準備する必要があります。

この記事の残りの部分で演習を行う前に、次のすべてのサブセクションの手順を実行してください。 また、これらのサブサイトでは、自分の組織のエンジニアリング変更管理を設定する際に使用するいくつかの重要な設定ページも紹介します。

### <a name="make-standard-demo-data-available"></a>標準デモ データを有効化する

標準の [デモ データ](../../fin-ops-core/fin-ops/get-started/demo-data.md) がインストールされているシステムで作業します。 標準のデモ データによって、複数のデモ法人 (会社および組織) のデータが追加されます。 この演習では、右側にある会社の選択を使用して、*エンジニアリング組織* として設定されている1つの会社 (*DEMF*) *運営組織* として設定されている別の会社 (*USMF*) を切り替えます。

### <a name="set-up-an-engineering-organization"></a>エンジニアリング組織の設定

エンジニアリング組織はエンジニアリング データを所有し、製品デザインと製品の変更を担当します。 エンジニアリング組織を設定するには、以下の手順に従ってください。

1. **エンジニアリング変更管理 &gt; 設定 &gt; エンジニアリング組織** に移動します。
1. **新規** を選択して、グリッドに行を追加して、それに次の値を設定します。

    - **エンジニアリング組織:** *DEMF*
    - **組織名:** *Contoso Entertainment System Germany*

    ![エンジニアリング組織を追加します。](media/engineering-org.png "エンジニアリング組織の追加")

### <a name="set-up-the-version-product-dimension-group"></a>バージョンの製品分析コード グループの設定

1. **製品情報管理 &gt; 設定 &gt; 分析コードとバリアント グループ &gt; 製品分析コード グループ** に移動します。
1. **新規** を選択して、製品分析コードグループを作成します。
1. **名前** フィールドを *バージョン* に設定します。
1. **保存** を選択して、新しい分析コードを保存し、**製品分析コード** クイックタブに値を読み込みます。
1. **製品分析コード** クイックタブで、有効な製品分析コードとして **バージョン** を設定します。

    ![製品分析コード グループを追加します。](media/product-dimension-groups.png "製品分析コード グループの追加")

### <a name="set-up-product-lifecycle-states"></a>製品ライフサイクルの状態の設定

エンジニアリング製品はライフサイクルを通じて、ライフサイクル状態ごとに許可するトランザクションを制御できるようにすることが重要です。 製品ライフサイクル状態を設定するには、次の手順を実行します。

1. **エンジニアリング変更管理 &gt; 設定 &gt; 製造ライフサイクルの状態** に移動します。
1. **新規** を選択して、ライフサイクルの状態を追加して、それに次の値を設定します。

    - **状態:** *操作*
    - **説明:** *操作*

1. **保存** を選択して、新しいライフサイクルの状態を保存し、**有効化されたビジネス プロセス** クイックタブに値を読み込みます。
1. **有効化されたビジネス プロセス** クイックタブで、使用できるビジネス プロセスを選択します。 この例では、すべてのビジネス プロセスに対して **ポリシー** フィールドを *有効化* にしておきます。

    ![ライフサイクル状態のビジネス プロセスを有効化します。](media/product-lifecycle-states-1.png "ライフサイクルの状態のビジネス プロセスの有効化")

1. **新規** を選択して、他のライフサイクルの状態を追加して、それに次の値を設定します。

    - **状態:** *プロトタイプ*
    - **説明:** *プロトタイプ*

1. **保存** を選択して、新しいライフサイクルの状態を保存し、**有効化されたビジネス プロセス** クイックタブに値を読み込みます。
1. **有効化されたビジネス プロセス** クイックタブで、使用できるビジネス プロセスを選択します。 この例では、すべてのビジネス プロセスに対して **ポリシー** フィールドを *警告付きで有効化* にしておきます。

    ![ライフサイクル状態のビジネス プロセスを有効化 (警告付き) します。](media/product-lifecycle-states-2.png "ライフサイクルの状態のビジネス プロセスの有効化 (警告付き)")

### <a name="set-up-a-version-number-rule"></a>バージョン番号ルールの設定

1. **エンジニアリング変更管理 &gt; 設定 &gt; 製品バージョン番号ルール** に移動します。
1. **新規** を選択して、ルールを追加して、それに次の値を設定します。

    - **名前:** *自動*
    - **番号ルール:** *自動*
    - **フォーマット:** *V-\#\#*

    ![製品バージョン番号ルールを追加します。](media/version-number-rule.png "製品バージョン番号ルールの追加")

### <a name="set-up-a-product-release-policy"></a>製品リリース ポリシーの設定

1. **エンジニアリング変更管理 &gt; 設定 &gt; 製品リリースポリシー** に移動します。
1. **新規** を選択して、リリース ポリシーの状態を追加して、それに次の値を設定します。

    - **名前:** *コンポーネント*
    - **説明:** *コンポーネント*

1. **一般** クイック タブで、次の値を設定します。

    - **製品タイプ :** *品目*
    - **テンプレートの適用:** *常に*
    - **有効:** *はい*

1. **すべての製品** クイック タブで、**追加** を選択して明細行を追加し、次の値を設定します。

    - **企業:** *DEMF*
    - **テンプレートリリース製品:** *D0006*

1. **追加** を選択して別の明細行を追加し、それに対して次の値を設定します。

    - **会社アカウント ID:** *USMF*
    - **テンプレートリリース製品:** *D0006*
    - **BOM の受取:** このチェックボックスを選択します。
    - **BOM 承認のコピー:** このチェックボックスをオンにします。
    - **BOM 承認のコピー:** このチェックボックスをオンにします。
    - **ルートの受取:** このチェックボックスを選択します。
    - **ルート承認のコピー:** このチェック ボックスをオンにします。
    - **ルートのアクティブ化のコピー:** このチェック ボックスをオンにします。

    ![製品リリース ポリシーを追加します。](media/product-release-policy.png "製品リリース ポリシーの追加")

### <a name="set-up-an-engineering-product-category"></a>エンジニアリング製品カテゴリの設定 

エンジニアリング製品カテゴリは、エンジニアリング製品 (技術変更管理によってバージョン指定されて制御される製品) を作成するための基礎となります。 エンジニアリング製品カテゴリを設定するには、次の手順に従ってください。

1. **エンジニアリング変更管理 &gt;エンジニアリング製品カテゴリの詳細** に移動します。
1. **新規** を選択してカテゴリを作成します。
1. **詳細** クイック タブで、次の値を設定します。

    - **名前:** *コンポーネント*
    - **エンジニアリング組織:** *DEMF*
    - **製品タイプ :** *品目*
    - **トランザクションのトラック バージョン:** *はい*
    - **製品分析コード グループ:** *バージョン*
    - **作成時の製品ライフサイクルの状態:** *操作可能*
    - **バージョン番号ルール:** *自動*
    - **効力を発揮する:** *いいえ*
    - **番号ルール命名法を使用する:** *いいえ*
    - **名前ルール命名法を使用する:** *いいえ*
    - **番号ルール命名法を使用する:** *いいえ*

1. **リリース ポリシー** クイックタブで、**製品リリースポリシー** フィールドを *コンポーネント* に設定します。
1. **保存** を選択します。

    ![エンジニアリング製品カテゴリを追加します。](media/product-category-details.png "エンジニアリング製品カテゴリの追加")

### <a name="set-up-product-acceptance-conditions"></a>製品受け入れ条件の設定

1. ナビゲーションバーの右側にある会社のピッカーを使用して、*USMF* 法人 (会社) に切り替えます。
1. **エンジニアリング変更管理 &gt; 設定 &gt; エンジニアリング変更管理パラメータ** に移動します。
1. **リリース管理** タブの **製品の受け入れ** セクションで、**製品の承認** フィールドを *手動* に設定します。

    ![製品受け入れ条件を設定します。](media/engineering-change-management-parameters.png "製品受け入れ条件の設定")

## <a name="create-a-new-engineering-product"></a>新しいエンジニアリング製品を作成する

エンジニアリング製品は、エンジニアリング変更管理を通じてバージョン管理と管理される製品です。 つまり、変更はその期間中に制御でき、変更情報はエンジニアリング変更オーダーを使用して保存されます。 エンジニアリング製品を作成するには、次の手順に従います。

1. エンジニアリング組織の法人に所属していることを確認してください (この例の場合は *DEMF*)。 必要に応じて、ナビゲーションバーの右側にある会社ピッカーを使用します。
1. **リリース済製品** ページを、次の手順のいずれかを実行して開きます。

    - **製品管理情報 &gt; 製品 &gt; リリースされた製品** の順に移動します。
    - **エンジニアリング変更管理 &gt; 共通 &gt; リリース済み製品** に移動します。

1. アクション ペインで、**製品** タブの **新規** グループで、**エンジニアリング製品** を選択します。
1. **新しい製品** ダイアログ ボックスに次の値を設定します。

    - **エンジニアリング製品カテゴリ:** *コンポーネント*
    - **製品番号 :** *Z0001*
    - **製品名:** *スピーカー セット*

    ![エンジニアリング製品を追加します。](media/new-product-dialog.png "エンジニアリング製品カテゴリの追加")

    **バージョン** フィールドは、前に設定した製品バージョン番号のルールを使用して自動的に設定されます。

1. **OK** を選択して製品を作成し、ダイアログ ボックスを閉じます。
1. 新しい製品の詳細ページが開きます。 **保管分析コードグループ**、**追跡用分析コードグループ**、**品目モデルグループ** など、一部のフィールドでは、値が既に入力されていますので注意してください。 これらのフィールドは、製品が *DEMF*  法人でリリースされており、*コンポーネント* エンジニアリング製品カテゴリに関連付けられている *コンポーネント* 製品関連ポリシーを使用しています。 以前に、品目 *D0006* をテンプレートとして使用して *DEMF* 法人の行を設定しているため、入力された値が品目 *D0006* から取得されました。

    ![リリース済製品の詳細です。](media/product-details.png "リリース済製品の詳細")

1. アクション ペインの **エンジニア** タブの **エンジニアリング変更管理** グループで、製品のバージョンを表示する **エンジニアリング バージョン** を選択して、製品のバージョンを表示します。

    ![エンジニアリング バージョンです。](media/engineering-versions-list.png "エンジニアリング バージョン")

1. **エンジニアリング バージョン** ページで、製品のバージョンは 1 つだけであり、有効になっていることを確認します。
1. バージョンを選択して、その詳細を表示します。

    ![エンジニアリング バージョンの詳細です。](media/engineering-version-details.png "エンジニアリング バージョンの詳細")

1. **エンジニアリング バージョン** ページで、**部品表** クイックタブで、**BOM の作成** を選択します。
1. **BOM の作成** ダイアログ ボックスに次の値を設定します。

    - **BOM 番号:** Z0001
    - **名前:** スピーカー セット
    - **サイト:** 1

    ![BOM を作成します。](media/create-bom.png "BOM の作成")

1. **OK** を選択して、BOM を作成し、ダイアログ ボックスを閉じます。
1. **部品表** クイックタブで、**部品表** を選択します。
1. **部品表** ページの、**部品表明細行** クイックタブで、3 明細行、それぞれに対して *D0001*、*D0003*、*D0006* の品目番号を追加します。

    ![BOM 明細行を追加します。](media/bom.png "BOM 明細行の追加")

1. **保存** を選択します。
1. ページを閉じます。
1. **エンジニアリング バージョン** ページで、**部品表** クイックタブで、**承認** を選択します。
1. 表示されるダイアログ ボックスで、**OK** を選択します。

    ![BOM を承認します。](media/approve-dialog.png "BOM の承認")

1. **エンジニアリング バージョン** ページで、**部品表** クイックタブで、**アクティブにする** を選択します。
1. **アクティブにする** と **承認済** チェック ボックスが BOM に対して選択されていることを確認します。

    ![BOM をアクティブ化し、承認します。](media/approved-bom.png "BOM のアクティブ化と承認")

1. ページを閉じます。

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a>ローカル会社へのエンジニアリング製品のリリース

この製品は、現在エンジニアリング部門によって設計されています。 この例では、製品はエンジニアリングによって顧客向けに設計されたプロトタイプです。 顧客は *USFM* 法人の顧客であるため、製品をその法人にリリースする必要があります。

1. 法人は *DEMF* に設定したままにします。 (必要に応じて、ナビゲーション バーの右側にある会社ピッカーを使用します。)
1. **製品管理情報 &gt; 製品 &gt; リリースされた製品** の順に移動します。
1. 製品 *Z0001* を選択します。
1. アクション ペインで **製品** タブの **管理** グループで、**製品構造のリリース** を選択して **製品リリース** ウィザードを開きます。
1. **リリースするエンジニアリング製品の選択** ページで、製品 *Z0001* に対して **選択** チェックボックスを選択して。

    ![リリースするエンジニアリング製品を選択します。](media/select-eng-product-to-release.png "リリースするエンジニアリング製品の選択")

1. **リリースの詳細** を選択します。
1. **製品リリース詳細** ページが表示され、リリースされる製品の詳細と、その製品構造を確認できます。 **BOM を送る** オプションが *はい* に設定されていることを確認します。 したがって、BOM の製品 *Z0001* とすべての子品目がリリースされます。

    左ウィンドウで任意の子項目を選択して、その詳細を確認できます。 いずれかの子品目に BOM がある場合は、その子品目の BOM をリリースするように選択することもできます。

    ![製品リリースの詳細を確認します。](media/product-release-details.png "製品リリースの詳細の確認")

1. ページを閉じて、**リリース済み製品** ウィザードに戻ります。
1. **次へ** を選択して、**リリースする製品を選択する** ページを選択します。 標準 (エンジニアリング以外) 製品を選択した場合は、このページに表示されます。 **製品構造のリリース** を選択して標準製品をリリースすると 、BOM と工順もリリースされます。

    ![リリースする標準製品を選択します。](media/select-std-product-to-release.png "リリースする標準製品の選択")

1. **次へ** を選択して、**リリースする製品バリアントを選択する** ページを選択します。 この例では、バリアントは存在しません。
1. **次へ** を選択して、**会社を選択する** ページを選択します。
1. 製品をリリースすべき会社を選択します。 この例の場合、**USMF** のチェックボックスを選択します。

    ![リリース先の会社を選択します。](media/select-release-companies.png "リリース先の会社の選択")

1. **次へ** を選択して、**選択を確認する** ページを開きます。
1. **完了** を選択します。

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a>ローカル会社でリリースする前に製品をレビューして承認を行ってください

これで、現在エンジニアリング部門は、製品が使用されるローカル会社に情報をリリースしています。 この例では、ローカル会社は *USMF* です。

*USMF* 会社の **エンジニアリング変更管理パラメータ** ページで **製品承認** フィールドを *手動* に設定しているため、製品をその会社にリリースする前に手動で承認する必要があります。 つまり、リリース製品になる前に確認して承認する必要があります。

製品を確認して *USMF* 会社でリリースするには、次の手順に従います。

1. 法人は *USMF* に設定します。 (ナビゲーション バーの右側にある会社ピッカーを使用します。)
1. **エンジニアリング変更管理 &gt;共通 &gt; の製品リリース &gt; 未処理の製品リリース** に移動します。

    **未処理の製品リリース** ページには、*承認待ちのステータス* を持つ製品 *Z0001* が表示されます。

    ![製品リリースを開きます。](media/open-product-releases.png "製品リリースを開く")

1. **製品番号** 列の値を選択して、**製品リリースの詳細** ページを開きます。 次の詳細に留意してください。

    - **一般** クイックタブには、製品リリースに関する情報 (この例では *DEMF*)、リリースするサイト (*1*)、入荷サイト (*1*) が表示されます。 **製品のリリース** ウィザードでは、受信サイトを指定しなかったので、リリース後のサイトの値が受信サイトにコピーされます。
    - **リリースの詳細** クイックタブには、製品とリリースされたバージョンに関する情報が表示されます。 ここでは、有効期間の日付などの設定を変更できます。
    - **工順** クイックタブには、製品の工順が表示されます。 ただし、この例では、工順がリリースされていません。

    ![製品リリースの詳細です。](media/product-release-details-2.png "製品リリースの詳細")

1. 情報の確認が完了したら、製品を承認して、*USMF* 会社でリリースする準備ができていることになります。 アクション ペインで、**アクション &gt; 承認** を選択します。
1. *USMF* 会社で製品が今リリースされています。 **製品管理情報 &gt; 製品 &gt; リリースされた製品** の順に移動します。 品目 *Z0001* が表示されます。

## <a name="use-the-product-in-transactions-in-the-local-company"></a>ローカル会社のトランザクションでの製品の使用

*USMF* 会社のマスタ データ マネージャは、製品が *プロトタイプ* 状態にあることを確認して、ユーザーが作業中のプロセスに誤って追加した場合に警告が表示されるようにしたいと考えています。

1. **製品管理情報 &gt; 製品 &gt; リリースされた製品** の順に移動します。
1. 製品 *Z0001* を選択して詳細ページを開きます。 (このフィルターを使用して製品を検索できます。)
1. アクション ペインの **エンジニア** タブの **エンジニアリング変更管理** グループで、**エンジニアリング バージョン** を選択します。
1. **エンジニアリング バージョン** ページで、バージョン番号 *V-01* を選択して、詳細ページを開きます。
1. アクション ペインで、**ライフサイクルの状態** グループにある **製品** タブで、**ライフサイクルの状態** を選択します。
1. **ライフサイクル状態の変更** のダイアログ ボックスで、**状態** フィールドを *プロトタイプ* に設定し、**OK** を選択します。

    ![ライフサイクル状態を変更します。](media/change-lifecycle-state.png "ライフサイクルの状態の変更")

## <a name="add-the-engineering-product-to-a-sales-order"></a>販売注文にエンジニアリング製品を追加する

これで、製品を顧客に販売できるようになります。 販売注文ヘッダーに製品を追加するには、次の手順に従います。

1. **販売とマーケティング &gt; 販売注文 &gt; すべての販売注文** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **販売注文の作成** ダイアログボックスで、**顧客アカウント** フィールドを *US-0002* に設定して、**OK** を選択します。
1. 新しい販売注文が開かれます。 **販売注文明細行** クイックタブで、行を追加し、その行の **品目番号** フィールドを *Z000* を設定します。
1. アクション ウィンドウで、**保存** を選択します。

    品目に *プロトタイプ* のステータスがあることを通知する警告メッセージを受信します。 ただし、このメッセージは単なる警告であり、販売注文が作成されています。

    ![エンジニアリング製品の販売注文です。](media/sales-order-eng-product.png "エンジニアリング製品の販売注文")

## <a name="request-changes-in-the-engineering-product"></a>エンジニアリング製品の変更の要求

この製品は顧客に送付されましたが、顧客は完全に満足しておらず、改善のための提案を含むフィードバックを提供します。 顧客は電話で販売係と話していますが、販売係は顧客が説明している変更を要求できます。

1. **販売とマーケティング &gt; 販売注文 &gt; すべての販売注文** の順に移動します。
1. 前の演習で作成した販売注文を検索して開きます。
1. **販売注文明細行** クイックタブで、**エンジニアリング変更管理 &gt; 新規エンジニアリング変更要求** を選択します。

    ![販売注文からのエンジニアリング変更依頼を作成します。](media/sales-order-eng-change-request.png "販売注文からのエンジニアリング変更依頼の作成")

1. 顧客からのフィードバックに基づいて、エンジニアリング変更要求を入力します。 この例では、次の値を設定します。

    - **変更要求:** *555*
    - **タイトル:** *Z0001 顧客の変更*
    - **優先度:** *低*
    - **カテゴリ:** 変更の設定
    - **重要度:** *中*

1. **情報** クイック タブで、**新規 &gt; メモ** を選択してグリッドにメモを追加します。
1. 新しい注記の **説明** フィールドで、品目 *D0003* を BOM から削除するように指定します。 メモの詳細情報を追加する必要がある場合は、**メモ** フィールドにテキストを入力できます。

    ![エンジニアリング変更要求です。](media/eng-change-request.png "エンジニアリング変更要求")

1. アクション ウィンドウで、**保存** を選択します。
1. **製品** クイックタブに品目が自動的に追加され、エンジニアリング変更要求のソース (販売注文) が **製品** クイックタブに追加されていることを確認します。

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a>エンジニアリング変更指示を使用して製品に変更を加える

販売係は、製品が重要であり、それが顧客のために特別設計されたことを知っています。 したがって、販売係は、*DEMF* 会社のエンジニアに変更依頼についての通知を依頼します。 このようにして、エンジニアはプロセスを高速化することができます。

エンジニアは、顧客から要求を確認し、製品の変更オーダーを作成します。

1. エンジニアが *DEMF* 会社で作業を行うため、法人を *DEMF* に設定します。 (ナビゲーション バーの右側にある会社ピッカーを使用します。)
1. **エンジニアリング変更管理 &gt; 共通 &gt; エンジニアリング変更要求** に移動します。
1. 変更要求 *555* を開きます。
1. 情報を確認し、変更を承認します。 アクション ペインの **変更要求** タブで、**状態の変更** グループで、**承認** を選択します。
1. **エンジニアリング変更管理 &gt; 共通 &gt; エンジニアリング変更オーダー** に移動します。
1. アクション ペインで、変更オーダーを作成するために **新規** を選択して、次の値を設定します。

    - **変更オーダー:** *555*
    - **タイトル:** *Z0001 顧客の変更*
    - **カテゴリ:** *顧客変更*
    - **優先度:** *低*
    - **重要度:** *中*

1. **影響を受ける製品** クイックタブで、**新規 &gt; 既存の製品を追加** を選択して、グリッドに行を追加して次の値を設定します。

    - **製品:** *Z0001*
    - **影響:** *新規バージョン*

    ![エンジニアリング変更オーダーを作成します。](media/eng-change-order.png "エンジニアリング変更オーダーの作成")

1. **影響** フィールドを *新バージョン* に設定しているため、**製品の詳細** クイックタブの **詳細** タブにある **製品の詳細** フィールドには、新しいバージョン番号 (この例では *V-02* ) が何かが表示されます。

    ![エンジニアリング変更オーダーの製品詳細です。](media/eng-change-order-product-details.png "エンジニアリング変更オーダーの製品詳細")

1. アクション ウィンドウで、**保存** を選択します。
1. **製品の詳細** クイックタブの **部品表** タブで、**明細行** を選択して、製品 *Z0001* のバージョン *V-01* の BOM を開き ます。

    ![エンジニアリング製品 BOM 明細行です。](media/eng-product-bom-lines.png "エンジニアリング製品 BOM 明細行")

1. 品目番号 *D0003* の明細行を選択し、アクション ペインで **削除** を選択します。 この明細行の **種類の変更** フィールドの値が *削除済み* に変わります。
1. アクション ウィンドウで、**保存** を選択します。

    ![変更されたエンジニアリング製品 BOM 明細行です。](media/eng-product-bom-lines-modified.png "変更されたエンジニアリング製品 BOM 明細行")

1. **BOM 明細行** ページを閉じて、**エンジニアリング変更オーダー** ページに戻ります。
1. **製品の詳細** クイックタブの **部品表** タブで、BOM *Z0001* の **変更タイプ** フィールドの値が、*変更済み* になっていることを確認します。

    ![変更された BOM を含むエンジニアリング変更オーダーです。](media/eng-change-order-changed-bom.png "変更された BOM を含むエンジニアリング変更オーダー")

    このオーダーは変更を処理する前に承認される必要があります。 変更が処理されると、エンジニアリング変更オーダーに含まれる変更で製品が更新されます。 この例では、エンジニアリングの変更オーダーを作成した人物が承認者として指定されています。

1. アクション ペインの **変更―ダー** タブ、**状態の変更** グループで、**承認** を選択します。
1. **プロセス** を選択して、製品の情報を更新します。

## <a name="release-the-changed-product"></a>変更した製品のリリース

これで、製品は *USMF* 会社に再度リリースでき、顧客に送付できるようになります。 エンジニアリング変更指示書から製品を直接リリースするには、次の手順に従います。

1. 前の手順で作成したエンジニアリング変更順序を開きます (まだ開いていない場合)。
1. アクション ペインの **変更オーダー** タブ、**製品リリース** グループで、**検索** を選択します。
1. この検索結果には、影響を受ける製品がどの会社にリリースされたかが示されます。 検索結果を閉じます。
1. アクション ペインの **変更オーダー** タブ、**製品リリース** グループで、**表示** を選択して、**リリース** ダイアログボックスを開きます。ここでは前の検索の結果を表示できます。
1. 製品をリリースする各会社を選択します。
1. **OK** を選択し、**リリース**  ダイアログ ボックスを閉じて、偏光オーダーに戻ります。
1. アクション ペインの、**変更オーダー** タブ、**製品リリース** グループで、**プロセス** を選択して、影響を受ける製品を選択した会社にリリースします。 または、**製品構造のリリース** を選択してリリースプロセスを開始します。

## <a name="complete-the-change-order"></a>変更オーダーの完了

変更オーダーを完了としてマークして、それ以上のアクションが残っていないことを示す場合は、アクション ウィンドウで **完了** を選択します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

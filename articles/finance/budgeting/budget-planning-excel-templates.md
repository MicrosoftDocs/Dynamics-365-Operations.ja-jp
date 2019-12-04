---
title: Excel の予算計画テンプレート
description: このトピックでは、予算計画で使用できる Microsoft Excel テンプレートを作成する方法について説明します。
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 471c719a8e6de0ebe6fcdad0ae222453db841c87
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772102"
---
# <a name="budget-planning-templates-for-excel"></a>Excel の予算計画テンプレート

[!include [banner](../includes/banner.md)]

このトピックでは、予算計画で使用できる Microsoft Excel テンプレートを作成する方法について説明します。

このトピックでは、標準デモ データ セットと管理者ユーザー ログインを使用して予算計画に使用する Excel テンプレートを作成する方法を示します。 予算計画に関する詳細については、[予算計画の概要](budget-planning-overview-configuration.md)を参照してください。 [予算計画](budget-plan.md)チュートリアルに従って、基本モジュールのコンフィギュレーションと使用の原則について参照することもできます。

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>予算計画ドキュメント レイアウトを使用したワークシートの生成

予算計画ドキュメントは、1 つ以上のレイアウトを使用して表示、編集できます。 各レイアウトでは、Excel ワークシートで予算計画データを表示および編集する関連の予算計画ドキュメント テンプレートを使用できます。 このトピックでは、予算計画ドキュメント テンプレートは既存のレイアウト コンフィギュレーションを使用して生成されます。 

1. **予算計画の一覧** (**予算作成** &gt; **予算計画**) を開きます。 
2. **新規**をクリックして、新しい予算計画ドキュメントを作成します。 

   [![予算計画の一覧](./media/bpt11-1024x552.png)](./media/bpt11.png) 

3. **追加**の行オプションを使用して、行を追加します。 **レイアウト**をクリックして、予算計画ドキュメントのレイアウト コンフィギュレーションを表示します。 

   [![予算計画の追加](./media/bpt2-1024x274.png)](./media/bpt2.png) 

レイアウト コンフィギュレーションを確認し、必要に応じて調整できます。 
1. **テンプレート** &gt; **生成**の順に移動して、このレイアウトの Excel ファイルを作成します。 
2. テンプレートが生成された後、**テンプレート** &gt; **表示**の順に移動して予算計画ドキュメント テンプレートを開いて確認します。 ローカル ドライブに Excel ファイルを保存できます。 

[![名前を付けて保存](./media/bpt3-1024x545.png)](./media/bpt3.png)

> [!NOTE] 
> 予算計画ドキュメント レイアウトは、Excel テンプレートが関連付けられると編集できません。 レイアウトを変更するには、関連する Excel テンプレート ファイルを削除して再生成します。 これはレイアウトやワークシートのフィールドの同期を維持するために必要です。 

**ワークシートで利用可能**列が True になっている場合、Excel テンプレートには予算計画ドキュメント レイアウトのすべての要素が含まれます。 重複する要素は、Excel テンプレートで許可されません。 たとえば、レイアウトに要求 Q1、要求 Q2、要求 Q3、要求 Q4 の列、4 つすべての四半期の列の合計を表す合計要求列が含まれている場合、その四半期列または合計列は Excel テンプレートで使用できます。 Excel ファイルは、テーブルのデータが期限切れおよび不正確になることがあるため、更新時に重複する列を更新することはできません。

> [!NOTE] 
> Excel を使用した予算計画データの表示および編集で起こる可能性のある問題を回避するには、同じユーザーが、Microsoft Dynamics 365 Finance および Microsoft Dynamics Office アドインのデータ コネクタの両方にログインする必要があります。

## <a name="add-a-header-to-budget-plan-document-template"></a>予算計画ドキュメント テンプレートへのヘッダーの追加
ヘッダー情報を追加するには、Excel ファイルの一番上の行を選択し、空の行を挿入します。 **データ コネクタ**の**デザイン**をクリックして Excel ファイルにヘッダー フィールドを追加します。

**デザイン**タブで、**追加**フィールドをクリックしてから、**BudgetPlanHeader** をエンティティ データ ソースとして選択します。

Excel ファイルの挿入位置にカーソルを合わせます。 **ラベルの追加**をクリックして、フィールド ラベルを選択した場所に追加します。 **値の追加**を選択して、選択した場所に値フィールドを追加します。 **完了**をクリックしてデザイナーを閉じます。

## <a name="select-add-valuemediabpt7pngmediabpt7png"></a>[![値の追加を選択](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>予算計画ドキュメント テンプレート テーブルへの計算された列の追加
--------------------------------------------------------------

次に、計算された列が生成された予算計画ドキュメント テンプレートに追加されます。 **合計要求**列は、要求 Q1: 要求 Q4 の列を集計し、**調整**列は、事前定義された係数によって**合計要求**列を再計算します。

**データ コネクタ**の**デザイン**をクリックしてテーブルに列を追加します。 **BudgetPlanWorkshee** データ ソースの横にある**編集**をクリックして、列の追加を開始します。

[![列の追加を開始](./media/bpt8-1024x301.png)](./media/bpt8.png) 

選択したフィールド グループに、テンプレートで使用できる列が表示されます。 **式** をクリックして新しい列を追加します。 新しい列に名前を付けてから、式を **式** フィールドに貼り付けます。 **更新**をクリックして列を挿入します。

[![列の追加と挿入](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> 式を定義するには、式をスプレッドシートで作成し、**デザイン**ウィンドウにコピーします。 Finance and Operations のバインドされたテーブルは、通常「AXTable1」と呼ばれます。 たとえば、スプレッドシートの要求 Q1 : 要求 Q4 の列を集計するには、式 = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\] となります。

以上の手順を繰り返して、**調整**列を挿入します。 この列では式 = AxTable1\[Total request\]\*$I$1 を使用します。 これは、セル I1 の値を取得し、**合計要求**列の値をかけて、調整金額を計算します。

Excel ファイルを保存して閉じます。 **レイアウト**で、**テンプレート &gt; アップロード**をクリックし、予算計画に使用する保存した Excel テンプレートをアップロードします。 

[![Excel テンプレートのアップロード](./media/bpt10-1024x352.png)](./media/bpt10.png) 

**レイアウト**スライダーを閉じます。 **予算計画**ドキュメントで、**ワークシート**をクリックして Excel でドキュメントを表示して編集します。 調整された Excel テンプレートがこの予算計画ワークシートの作成に使用され、計算された列が前の手順で定義された式を使用して更新されることに注意してください。 

[![Excel でのドキュメントの表示と編集](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>予算計画テンプレートを作成するためのヒントとトリック
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>予算計画テンプレートに追加のデータ ソースを追加して使用することはできますか。

はい、**デザイン**メニューを使用して Excel テンプレートの同じシートまたは他のシートに追加のエンティティを追加できます。 たとえば、Excel で予算計画データを使用している場合、**BudgetPlanProposedProject** のデータ ソースを追加して、同時に提示されるプロジェクトの一覧を作成して管理できます。 大量のデータ ソースが含まれている場合、Excel ブックのパフォーマンスに影響が出る場合があることに注意してください。 

**データ コネクタ**の**フィルター**オプションを使用して、追加のデータ ソースに希望するフィルターを追加できます。

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>他のユーザーに対してデータ コネクタの [デザイン] オプションを非表示にできますか。

はい、**データ コネクタ**オプションを開いて、他のユーザーから**デザイン**オプションを非表示にできます。

[![データ コネクタ オプションを開く](./media/bpt13-1024x565.png)](./media/bpt13.png)

**データ コネクタ オプション**を展開して、**デザインの有効化**チェック ボックスをオフにします。 これで、**デザイン**オプションを**データ コネクタ**から非表示にできます。

[![データ コネクタからデザイン オプションを非表示にする](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>ユーザーがデータを使用する際に、誤ってデータ コネクタを閉じないようにできますか。

テンプレートをロックしてユーザーが閉じないようにすることをお勧めします。 ロックをオンにするには、**データ コネクタ**をクリックすると、右上に矢印が表示されます。 

[![ロックをオンにする](./media/bpt15-1024x285.png)](./media/bpt15.png) 

追加メニューの矢印をクリックします。 **ロック**を選択します。

### <a name="select-lockmediabpt16-1024x614pngmediabpt16png"></a>[![ロックを選択する](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>予算計画テンプレートでセルの書式、色、条件付き書式、グラフなど Excel の他の機能を使用できますか。

はい、Excel の標準機能のほとんどが、予算計画テンプレートで機能します。 ユーザーに色コードを使用して読み取り専用と編集可能列を区別することをお勧めします。 条件付き書式は、予算の問題のある領域を強調表示するために使用できます。 列合計は、テーブルの Excel の標準式を使用して簡単に表示できます。

また、予算データの追加のグループ化やビジュアル化のためにピボット テーブルおよびグラフを作成して使用することもできます。 **データ**タブの**接続**グループで、**すべて更新**をクリックしてから、**接続のプロパティ**をクリックします。 **使用**タブをクリックします。**更新**で、**ファイルを開いたときにデータを更新**チェック ボックスを選択します。 




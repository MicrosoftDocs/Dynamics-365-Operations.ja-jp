---
title: "Excelの予算の計画テンプレート"
description: "このトピックでは、予算の計画で使用できるMicrosoft Excelテンプレートを作成する方法について説明します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>Excelの予算の計画テンプレート

このトピックでは、予算の計画で使用できるMicrosoft Excelテンプレートを作成する方法について説明します。

このトピックでは、標準デモのデータセットとAdministratorsユーザーのログオンを使用して予算の計画に使用するExcelテンプレートを作成する方法を示します。 予算の計画に関する詳細については、" [予算の計画の概要。] (予算計画概要configuration.md)  [、101を計画する予算] (基本モジュールのコンフィギュレーションと使用の原則を入手予算plan.mdの追跡することができます) チュートリアル。

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>予算の計画のドキュメント レイアウトを使用してワークシートを生成します。
予算の計画のドキュメントが一つ以上のレイアウトを使用して見られ編集できます。 各レイアウトは、Excelワークシートの予算のデータを表示および編集する関連の予算の計画のドキュメント テンプレートを使用できます。 このトピックでは、予算の計画のドキュメント テンプレートは、既存のレイアウト コンフィギュレーションを使用して生成されます。 開き**計画を一覧表示すること。** **割り当てます (**&gt; ** **予算を計画します。 新しい予算の計画のドキュメントを作成します**新しい**。 [![] bpt1 (。/media/bpt11-1024x552.png) ] (。/media/bpt11.png)  

行を追加するのに**追加します。**行オプションを使用します。 予算の計画のドキュメント レイアウト コンフィギュレーションを表示するには、[**レイアウト**。 
[![] bpt2 (。/media/bpt2-1024x274.png) ] (。/media/bpt2.png)  

レイアウト コンフィギュレーションを確認し、必要に応じて変更できます。 ** ** **生成 &gt; されます**テンプレート実行します。このレイアウトのExcelファイルを作成します。 テンプレートが生成された後、テンプレート表示** ** &gt; ** **実行予算の計画のドキュメント テンプレートを確認する開きます。 ローカル ドライブにExcelファイルの保存できます。 [![] bpt3 (。/media/bpt3-1024x545.png) ] (。/media/bpt3.png)  

> [!NOTE] 
> 予算の計画のドキュメント レイアウトは、Excelテンプレートが関連付けられたと編集できません。 レイアウトを変更するには、関連するExcelテンプレート ファイルを削除して再生成します。 これは同期するレイアウトやワークシートのフィールドを維持するために必要です。 

Excelテンプレートは**ワークシートで使用できる**列を調整するために設定された予算の計画のドキュメント レイアウトからすべての要素が含まれます。 重複する要素は、Excelテンプレートに許可されません。 たとえば、レイアウトが要求Q1、要求Q2、要求Q3、要求Q4の列が含まれている場合、すべての4つの四半期の列の合計を表す合計要求の列四半期の列のみまたは合計列がExcelテンプレートを使用して使用できます。 Excelファイルは、更新時にテーブルのデータが無効と不正確になることができるので、重複する列を更新することはできません。

[![] bpt4 (。/media/bpt4-1024x615.png) ] (。/media/bpt4.png) 

> [!NOTE] 
> Excelを使用して、表示、および予算のデータを編集することのある潜在的な問題を回避するには、同じユーザーは、Dynamics 365 for OperationsおよびMicrosoft Dynamicsの会社データ展開Connectorの両方に記録されます。

## <a name="add-a-header-to-budget-plan-document-template"></a>予算の計画のドキュメント テンプレートにヘッダーを追加します。
ヘッダー情報を追加するには、Excelファイルの一番上の行を選択し、空の行を挿入します。 [デザイン** **は、Excelのヘッダー フィールドを追加するため、**データ コネクタ**ファイルします。

[![] bpt5 (。/media/bpt5-1024x615.png) ] (。/media/bpt5.png)  

**デザイン**タブで、[** ** **エンティティのデータ ソースとしては**追加します。**フィールド、** BudgetPlanHeader選択します。

[![] bpt6 (。/media/bpt6-1024x615.png) ] (。/media/bpt6.png) 

Excelファイルの挿入位置をカーソルをポイントします。 選択した場所ラベルにフィールドを追加します**ラベルを追加します。**。 [**値を追加する。**値]フィールドの特定の場所に追加します。 デザイナーを閉じる[**可能な**。

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![] bpt7 (。/media/bpt7.png) ] (。/media/bpt7.png) 

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>予算の計画のドキュメント テンプレートの表に、計算列を追加します。
--------------------------------------------------------------

次に、計算列が生成された予算の計画のドキュメント テンプレートに追加されます。 A **合計要求**要求Q1を集計する列、: Q4列および定義済の要因によって**合計要求**列を再**調整**列を要求します。

[デザイン** **テーブルの列を追加するため、**データ コネクタ**。 [**編集を行います** ** BudgetPlanWorksheet **列の追加を開始するデータ ソースの横に表示します。

[![] bpt8 (。/media/bpt8-1024x301.png) ] (。/media/bpt8.png)  

選択したフィールドのグループをテンプレートに使用できる列が表示されます。 新しい列を追加します**フォーミュラ**。 新しい列を付け、[フォーミュラ** **フィールドのフォーミュラを貼ってします。 列を挿入します**更新**。

[![] bpt12 (。/media/bpt12-1024x565.png) ] (。/media/bpt12.png) 

> [!NOTE] 
> フォーミュラを定義するには、フォーミュラをスプレッドシートで作成し、** **デザイン ウィンドウにコピーします。 工程で結合されたテーブル365 for Operationsは、「AXTable1」と呼ばれます。 たとえば、要求Q1を集計する場合: スプレッドシート、式= AxTable1\[要求Q1\]+AxTable1\[要求Q2\]+AxTable1\[要求Q3\]+AxTable1\[要求Q4\]のQ4列を要求します。

**調整**列を挿入するには、次の手順を繰り返してします。 この列のフォーミュラAxTable1 =\[合計要求の\]\*$I$1を使用します。 これは、セルI1の値をとり、調整金額の計算に**要求の合計。**列の値を大きくします。

Excelファイルを保存して終了します。 予算の計画に使用するExcelの保存されたテンプレートをアップロードするには、&gt; Dynamics 365 for Operationsは、**レイアウト**、[**テンプレートのアップロード**戻します。 

[![] bpt10 (。/media/bpt10-1024x352.png) ] (。/media/bpt10.png)  

**レイアウト**スライダーを閉じます。 **予算の計画**ドキュメントでは、Excelのドキュメントを表示および編集するに**ワークシート**クリックします。 この予算の計画ワークシートを作成する場合でも、Excelの調整されたテンプレートを使用して計算列が前の手順で定義された式を使用して更新されることに注意してください。 

[![] bpt11 (。/media/bpt111-1024x431.png) ] (。/media/bpt111.png) 

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>予算の計画テンプレートを作成するためのヒント トリックします。
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>[予算の計画テンプレートに追加データ ソースを追加して使用することもできますか。

[はい、同じに追加企業またはExcelテンプレートの他の返信シートを追加するのに**デザイン**メニューを使用できます。 たとえば、Excelの予算の計画データに提示されるプロジェクトの一覧の使用と** BudgetPlanProposedProject **データ ソースを追加する同時に作成および管理する。 大量のデータ ソースが、Excelのブックのパフォーマンスが低下するかもしあります。表示します。 

**でデータ コネクタ**追加データ ソースに必要なフィルタを追加するのに** **フィルタ オプションを使用できます。

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>[他のユーザーのデータConnectorに設計オプションを非表示にすることもできますか。

[はい、別のユーザーから**デザイン**オプションを非表示になります。**データ コネクタ**オプションを開きます。

[![] bpt13 (。/media/bpt13-1024x565.png) ] (。/media/bpt13.png) 

**データ コネクタ オプション**展開し、**有効デザイン**チェック ボックスをオフにします。 これは、**デザイン**オプションを非**データ コネクタ**。

[![] bpt14 (。/media/bpt14-1024x592.png) ] (。/media/bpt14.png) 

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>データを使用すると、[ユーザーが誤ってConnectorデータを行うことを回避するためですか。

ただし、ユーザーはそのを行うことを防ぐためのテンプレートをロックすることをお勧めします。 ロックを始動するには、矢印ボタンが表示される右上隅にある**データ コネクタ**、[]をクリックします。 

[![] bpt15 (。/media/bpt15-1024x285.png) ] (。/media/bpt15.png)  

追加メニューの矢印をクリックします。 **ロック**選択します。

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![] bpt16 (。/media/bpt16-1024x614.png) ] (。/media/bpt16.png) 

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>[期限切れの予算の計画テンプレートを含むセルの書式設定、色、条件付き書式とグラフにExcelなどの他の機能を使用することもできますか。

[はい、Excelの標準機能のほとんどは、予算の計画テンプレートにはたらきます。 ただし、ユーザーの色コードを使用して読み取り専用と編集可能列を区別することをお勧めします。 条件付き書式の予算の問題な領域を強調表示するのに使用できます。 列合計は、テーブルの上のExcelの標準式を使用して、簡単に表示できます。

また、別途グループにピボット テーブル、チャート、予算データのビジュアル化を作成および使用できます。 **でデータ**、**接続**グループに、[**をすべてを更新します。**記録し、[]をクリックします。**接続プロパティ**。 **使用**タブをクリックします。 で**更新**ファイルを開いたときに、**データを更新します。**チェック ボックスをオンにします。 

[![] bpt17 (。/media/bpt17-1024x614.png) ] (。/media/bpt17.png) 



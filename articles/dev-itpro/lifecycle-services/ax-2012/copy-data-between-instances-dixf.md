---
title: "Dynamics AX インスタンス間でのデータのコピー"
description: "このトピックでは、データ インポート/エクスポート フレームワーク (DIXF) を使用して Dynamics AX インスタンス間でデータをコピーする方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 20251
ms.assetid: f608a318-106e-4edb-8a6f-c7a753a27640
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 680ebdaec7e624ca5da9cef5f444b0fa1da52e5e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="copy-data-between-dynamics-ax-instances"></a>Dynamics AX インスタンス間でのデータのコピー

[!include [banner](../../includes/banner.md)]

このチュートリアルでは、次の作業について説明します。

-   ソース データのフォーマットを形式する
-   処理グループの定義
-   ソースからステージングにデータを処理
-   ステージングのデータの検証
-   データをファイルへエクスポート
-   データのインポート
-   ターゲットのデータの検証

## <a name="prerequisites"></a>前提条件
このチュートリアルを完了するには、次のものが必要です。

-   Microsoft Dynamics AX 2012、Microsoft Dynamics AX 2012 R2、または Microsoft Dynamics AX 2012 R3
-   データのインポート/エクスポート フレームワーク
-   Microsoft Dynamics AX 2012、Microsoft Dynamics AX 2012 R2、または Microsoft Dynamics AX 2012 R3 のデモ データ

次の図は、エクスポートおよびインポート処理中にデータが取るパスを示しています。 [![WalkthroughCopyDataBetweenAXInstances1](./media/walkthroughcopydatabetweenaxinstances1.jpg)](./media/walkthroughcopydatabetweenaxinstances1.jpg)

## <a name="define-the-format-of-your-source-data"></a>ソース データのフォーマットを形式する
1.  **データのインポート/エクスポート フレームワーク** &gt; **設定** &gt; **ソース データ形式**を開きます。
2.  **新規**をクリックし、名前と説明を入力します。次に、**タイプ** リストから **AX** を選択します。

## <a name="define-a-processing-group-to-export-data-from-microsoft-dynamics-ax"></a>Microsoft Dynamics AX からデータをエクスポートする処理グループを定義します。
1.  会社を **CEU** に変更します。
2.  **データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ**とクリックしてから、**新規**をクリックして新しい処理グループを作成します。
3.  グループ名を Export-Cust に設定し、説明を追加します。
4.  処理グループに含めるエンティティを選択するには、**エンティティ**をクリックします。
    1.  **処理グループのエンティティの選択**フォームで、**新規**をクリックしてから、エンティティに対して**顧客**を選択します。
    2.  **ソース データ形式**フィールドで、作成した Microsoft Dynamics AX のソース データ形式を選択します。
    3.  **選択**ボタンをクリックします。次に **DMFCustomerTargetEntity** フォームの**範囲**タブで、**フィールド**を**作成日時**と選択します。**基準**に &gt; 9/1/2007 と入力し、**OK** をクリックします。
    4.  **処理グループのエンティティの選択** フォームを閉じます。

## <a name="process-data-from-source-to-staging"></a>ソースからステージングにデータを処理
1.  **処理グループ** フォームで、作成したエクスポート顧客グループを選択して**ステージング データの取得**をクリックします。 **ステージング データ ジョブに対するジョブ ID の作成** フォームが開きます。
2.  既定では、ジョブの ID が生成されます。 必要に応じて、ID を変更して説明を追加することができます。 **OK** をクリックします。 **ステージング データ実行** フォームが開きます。
3.  **ステージング データ実行**フォームで、**実行**をクリックします。 **ソースからステージングにデータを取得** フォームが開きます。
4.  **ソースからステージングにデータを取得**フォームで、**OK** をクリックしてすぐに実行します。 ソース データはステージング テーブルにコピーされます。

## <a name="validate-the-data-in-staging"></a>ステージングのデータの検証
1.  **データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ** &gt; **実行履歴**とクリックしてから実行したジョブを選択します。
2.  **ステージング データの表示**をクリックします。
3.  ソースと一致することを検証するステージング データを確認します。
4.  **すべて検証**をクリックして、関連するすべての参照データが正しくシステムに存在することを確認します。

## <a name="export-the-data-to-a-file"></a>データをファイルへエクスポート
1.  **データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ**とクリックしてから、操作する処理グループを選択します。
2.  **AX にエクスポート**をクリックし、ファイル名を入力してから **OK** をクリックします。 処理グループによって識別される .dat ファイルが作成されます。

## <a name="import-the-data"></a>データのインポート
1.  データをインポートしたい Microsoft Dynamics AX のインスタンスに接続されているクライアントを開きます。
2.  現在の会社がデータのインポート先であることを確認します。
3.  **システム管理** &gt; **共通** &gt; **データのエクスポート/インポート** &gt; **インポート**の順にクリックします。
4.  **一般**タブで、インポートするデータ ファイルを選択します。
5.  **バッチ**タブで、インポート ファイルを処理するバッチ グループを選択します。 すべてのインポート ジョブはバッチ タスクとして実行します。

## <a name="validate-the-data-in-target"></a>ターゲットのデータの検証
元のインスタンスからの顧客データが **すべての顧客** フォームに表示されるようになったこと確認します。 **売掛金勘定** &gt; **共通** &gt; **顧客** &gt; **すべての顧客**フォームの順にクリックします。





---
title: "Dynamics AX 会社間でのデータのコピー"
description: "Microsoft Dynamics AX 2012 のデータのインポート/エクスポート フレームワークを使用すると、顧客などのエンティティを 1 つの Microsoft Dynamics AX の法人 (会社) から他にコピーすることができます。 この例では、Contoso データ セットの CEC 会社に CEU 会社の特定の顧客グループ内の顧客グループをエクスポートします。"
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 17821
ms.assetid: cd9b30d2-d4e0-4da7-9408-34bda5888070
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 58ff855888be0a7b06eae372bb31f2442ef09b03
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="copy-data-between-dynamics-ax-companies"></a>Dynamics AX 会社間でのデータのコピー

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics AX 2012 のデータのインポート/エクスポート フレームワークを使用すると、顧客などのエンティティを 1 つの Microsoft Dynamics AX の法人 (会社) から他にコピーすることができます。 この例では、Contoso データ セットの CEC 会社に CEU 会社の特定の顧客グループ内の顧客グループをエクスポートします。

**注:** このチュートリアルは、Microsoft Dynamics AX 2012 R2 または Microsoft Dynamics AX 2012 R3 の累積的な更新プログラム 7 に付属しているデータのインポート/エクスポート フレームワークのバージョンのユーザーを対象としていません。 これらのユーザーは、トピック [[企業間でのエンティティ データのコピーと比較 (DIXF、DMF)](copy-compare-entity-data-between-companies-dixf.md)] を参照してください。 このチュートリアルでは、次の作業について説明します。

-   ソース データのフォーマットを形式する
-   処理グループの定義
-   ソースからステージングにデータを処理
-   会社を切り替えて別の法人にデータをコピー
-   ステージングのデータの検証
-   ターゲットのデータの検証

次の図は、エクスポートおよびインポート処理中にデータが取るパスを示しています。 [![WalkthroughCopyDataBetweenAXCompanies1](./media/walkthroughcopydatabetweenaxcompanies1.jpg)](./media/walkthroughcopydatabetweenaxcompanies1.jpg)

## <a name="prerequisites"></a>前提条件
このチュートリアルを完了するには、次のものが必要です。

-   Microsoft Dynamics AX 2012 または Microsoft Dynamics AX 2012 R2
-   データのインポート/エクスポート フレームワーク
-   Microsoft Dynamics AX 2012 または Microsoft Dynamics AX 2012 R2 のデモ データ

## <a name="define-the-format-of-your-source-data"></a>ソース データのフォーマットを形式する
1.  **データのインポート/エクスポート フレームワーク** &gt; **設定** &gt; **ソース データ形式**を開きます。
2.  **新規**をクリックし、名前と説明を入力します。次に、**タイプ** リストから **AX** を選択します。

## <a name="define-a-processing-group-to-export-data-from-microsoft-dynamics-ax"></a>Microsoft Dynamics AX からデータをエクスポートする処理グループを定義します。
1.  会社を **CEU** に変更します。
2.  **データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ**とクリックしてから、**新規**をクリックして新しい処理グループを作成します。
3.  グループ名を **Export-Cust** に設定し、説明を追加します。
4.  処理グループに含めるエンティティを選択するには、**エンティティ**をクリックします。
    1.  **処理グループのエンティティの選択**フォームで、**新規**をクリックしてから、エンティティに対して**顧客**を選択します。
    2.  **ソース データ形式**フィールドで、作成した Microsoft Dynamics AX のソース データ形式を選択します。
    3.  **選択**をクリックし、**DMFCustomerTargetEntity** フォーム内の**範囲**タブで、**フィールド**の**顧客グループ**、および**基準**の **20** を選択し、**OK** をクリックします。
    4.  **処理グループのエンティティの選択** フォームを閉じます。

## <a name="process-data-from-source-to-staging"></a>ソースからステージングにデータを処理
1.  **処理グループ** フォームで、作成したエクスポート顧客グループを選択して**ステージング データの取得**をクリックします。 **ステージング データ ジョブに対するジョブ ID の作成** フォームが開きます。
2.  既定では、ジョブの ID が生成されます。 必要に応じて、ID を変更して説明を追加することができます。 **OK** をクリックします。 **ステージング データ実行フォーム**が開きます。
3.  **ソースからステージングにデータを取得**フォームで、**OK** をクリックしてすぐに実行します。 ソース データはステージング テーブルにコピーされます。

## <a name="validate-the-data-in-staging"></a>ステージングのデータの検証
1.  **データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ** &gt; **実行履歴**とクリックしてから実行したジョブを選択します。
2.  **ステージング データの表示**をクリックします。
3.  ソースと一致することを検証するステージング データを確認します。
4.  **すべて検証**をクリックして、関連するすべての参照データが正しくシステムに存在することを確認します。

## <a name="switch-companies-to-copy-data-to-another-company"></a>会社を切り替えて別の会社にデータをコピー
1.  **CEC** 会社に切り替えます。
2.  **データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ**とクリックしてから、操作する処理グループを選択します。
3.  **データをターゲットにコピー**をクリックします。 **実行するジョブ ID を選択** フォームが開きます。
4.  ジョブを選択し、**OK** をクリックします。 **ターゲット データ実行** フォームが開きます。
5.  **実行**をクリックし、**OK** をクリックします。 データはターゲット エンティティにコピーされます。

## <a name="validate-the-data-in-target"></a>ターゲットのデータの検証
元の会社からの顧客データが次のいずれかの方法で表示されていることを確認します。

-   ステージング データの表示:
    1.  **データのインポート/エクスポート フレームワーク**で、**共通** &gt; **処理グループ** &gt; **実行履歴** &gt; **ステージング データの表示**とクリックしてから実行したジョブを選択します。
    2.  ソースと一致することを検証するステージング データを確認します。
    3.  **すべて検証**をクリックして、関連するすべての参照データが正しくシステムに存在することを確認します。
-   CEU 会社からの顧客データが **すべての顧客フォーム** に表示されるようになったこと確認します。 **売掛金勘定** &gt; **共通** &gt; **顧客** &gt; **すべての顧客**フォームの順にクリックします。






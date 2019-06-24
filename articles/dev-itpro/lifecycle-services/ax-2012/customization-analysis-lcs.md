---
title: Lifecycle Services (LCS) 内のカスタマイズ分析
description: Microsoft Dynamics Lifecycle Services では、カスタマイズ分析がテーブル、クラス、フォーム、および列挙の Microsoft Dynamics AX のベスト プラクティス ルールに対して顧客のモデル ファイルを検証する自動ツールを Microsoft Dynamics AX 2012 の顧客に提供します。 その後、サイトでの概要レポートの表示、すべての問題を一覧表示する詳細な Microsoft Excel レポート、開発者が Microsoft Dynamics AX の開発環境で読み込むことができる開発者レポートを含んだレポートを生成します。
author: RobinARH
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 19021
ms.assetid: 409386b2-98c8-44a7-be6f-252f8a21f819
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 9bd15953d0f024a8df5959837ff3b39534eba1a9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544088"
---
# <a name="customization-analysis-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) 内のカスタマイズ分析

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics Lifecycle Services では、カスタマイズ分析がテーブル、クラス、フォーム、および列挙の Microsoft Dynamics AX のベスト プラクティス ルールに対して顧客のモデル ファイルを検証する自動ツールを Microsoft Dynamics AX 2012 の顧客に提供します。 その後、サイトでの概要レポートの表示、すべての問題を一覧表示する詳細な Microsoft Excel レポート、開発者が Microsoft Dynamics AX の開発環境で読み込むことができる開発者レポートを含んだレポートを生成します。 

<a name="prerequisites"></a>必要条件
-------------

Microsoft Dynamics AX 2012 モデル ファイルの分析を行う必要があります。 モデル ファイルの詳細については、「[方法: モデルのエクスポートおよびインポート](http://msdn.microsoft.com/library/c2449a03-7574-4b9d-8518-9005b560209f(AX.60).aspx)」を参照してください。

## <a name="getting-started"></a>はじめに
カスタマイズ分析を使用するには、モデル ファイルをアップロードし、レポートを評価して、どのように変更するかを判断する必要があります。

### <a name="upload-model-files"></a>モデル ファイルのアップロード

1.  [Lifecycle Services に移動](https://lcs.dynamics.com).
2.  プロジェクトを開いて、**カスタマイズ分析**タイルをクリックします。
3.  **追加**をクリックし、**カスタマイズ分析: ジョブを作成**ページで、名前、適切なバージョンの Microsoft Dynamics AX、および適切なビルドを入力します。
4.  **作成** をクリックします。
5.  **ファイルの追加**をクリックして分析するモデルを参照し、**アップロード**をクリックします。 分析のために複数のモデル ファイルをアップロードすることができます。
6.  **コードの分析**をクリックします。 サイトがファイルを処理し、レポートを生成します。 処理中に、ステータス インジケーターは更新します。 **注記:** 処理が続行されている間、ページを離れることができます。 処理には 10 分以上かかることがあります。

### <a name="evaluate-reports"></a>レポートの評価

カスタマイズ分析は、テーブル、クラス、フォーム、および列挙の Microsoft Dynamics AX のベスト プラクティス ルールに照らして、モデル ファイルを検証します。 その後、コードがこれらのルールから逸脱するインスタンスの詳細なレポートを生成します。 処理が完了したら、レビューするレポートを選択できます。 カスタマイズの分析には、次のレポート タイプが用意されています。

1.  ブラウザー内で表示できる HTML カスタマイズ分析のレポートです。
2.  Excel ファイルを使用して生成されたエラーを確認できます。 このレポートを表示するには、**表示** をクリックし、ファイルを開きます。
3.  HTML 開発者レポート。Microsoft Dynamics AX の開発者環境で開くことができます。 Microsoft Dynamics AX 開発環境でこのレポートを表示するには、次の手順を実行します。
    1.  **表示**をクリックします。 ファイルはブラウザー ウィンドウで開きます。
    2.  開発環境のコンピューターにレポートを保存します。
    3.  **コンパイラ出力**ウィンドウで、**インポート**をクリックし、ファイルを選択して開きます。
    4.  レポート内で任意の行をダブルクリックして、報告された問題を含むオブジェクトおよび行を開くことができます。

### <a name="remove-a-customization-job"></a>カスタマイズ ジョブの削除

プロジェクトのカスタマイズ一覧からジョブを削除するには、ジョブ名の上にカーソルを置き、左側のボックスをクリックして **削除** ボタンをクリックします。

<a name="additional-resources"></a>追加リソース
--------

[Microsoft Dynamics AX 開発のベスト プラクティス](http://msdn.microsoft.com/library/833e44ff-d89a-459a-84be-0cc5da57ee90(AX.60).aspx)




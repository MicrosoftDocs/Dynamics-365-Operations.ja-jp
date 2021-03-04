---
title: Power BI Desktop を使用した分析レポートの作成
description: このトピックでは、ローカルの Entity Store データベースを使用して Power BI レポートを作成するプロセスについて説明します。
author: MilindaV2
manager: AnnBe
ms.date: 01/29/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: BIMeasurementDeployManagementEntityStore
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: 265864
ms.assetid: e253a57a-979b-4ca5-8e09-2bfce97395a5
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 5809cf5ad0422939fe68ab97f0e8782b4d6769e4
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093096"
---
# <a name="create-analytical-reports-by-using-power-bi-desktop"></a>Power BI Desktop を使用した分析レポートの作成

[!include [banner](../includes/banner.md)]

ユーザーが power user またはビジネス アナリストである場合は、自分の組織のために多くのレポートを作成している可能性があります。 他のユーザーと共有する前に、データの書式設定と関連付けによって、Microsoft Excel でこれらのレポートを作成する場合があります。 レポートへの変更が必要な場合、組織内のユーザーから連絡が来る可能性があります。 このソリューションを使用すると、リッチでインタラクティブなレポートを簡単に作成できます。 レポート ライターは、Microsoft Power BI Desktop をレポート ツールとして使用することができます。 作成したレポートは、PowerBI.com に公開することができます。 Power BI Desktop の詳細については、[Power BI Desktop で魅力的なレポートとビジュアライゼーションを作成する](https://powerbi.microsoft.com/desktop)を参照してください。

## <a name="accessing-the-local-entity-store-by-using-directquery"></a>DirectQuery を使用してローカル エンティティ ストアへのアクセス
データ エンティティを介して公開されるオープン データ プロトコル (OData) エンドポイントを使用して、Microsoft Power BI レポートを作成することができます。 このアプローチの限界にもかかわらず、エンティティ格納はレガシ ソリューションでもエンティティ格納をサポートしています。 ただし、DirectQuery は、解析ソリューションのソース データに推奨されるメソッドになりました。 DirectQuery の利点および制限の詳細については、[Power BI Desktop で DirectQuery の使用](https://powerbi.microsoft.com/documentation/powerbi-desktop-use-directquery/)を参照してください。

Power BI Desktop を使用すると、ローカルのエンティティ格納データベースに直接接続することによって、開発またはテスト環境でレポートを作成することができます。 レポートに問題がなければ、管理者は、ユーザーがそれを実稼働環境に移行する支援をすることができます。 このセクションの残りの部分では、このプロセスについて説明します。

> [!NOTE]
> 分析ワークスペースとレポートをアプリケーション スイートで開発または拡張するには、顧客が独自の定期売買またはローカル コンピューターで実行している開発環境を使用する必要があります。 Microsoft が提供するレベル 1 環境では、埋め込まれた分析レポートを開発または拡張することはできません。 Power BI Desktop をインストールするには管理者権限が必要です。

> レベル 1環境には、Power BI Desktop のサービス互換性があるバージョンが含まれます。 分析ワークスペースとレポートをアプリケーション スイートで開発または拡張するには、顧客が開発環境にプレインストールした Power BI Desktop を使用することができます。 または、Power BI Desktop の最新の互換性があるリリースを使用し、プレビュー機能をオフにして、Finance and Operations アプリの分析レポートを作成できます。 [Power BI Desktop の前の月次更新](https://docs.microsoft.com/power-bi/fundamentals/desktop-latest-update-archive#power-bi-desktop-monthly-update-video-3) で Power BI Desktop の 2020 年 8 月の更新プログラムをダウンロードします。

### <a name="step-1-populate-the-local-entity-store-database"></a>手順 1: ローカル エンティティ格納データベースに入力する
この例では、ローカルのエンティティ ストアでコマース 分析ソリューションが消費する集計モデルをステージングします。 アプリケーションが使用するモデルは、RetailCube 集計測定で定義されています。 

1. クライアントで **エンティティ格納** ページを開きます。 (**システム管理** \> **設定** \> **エンティティ格納** の順に選択します。) 
2. **RetailCube** 集計測定を選択し、**更新** を選択します。 
3. バック グラウンドで実行されるジョブ名を入力し、**OK** を選択します。

次の図は、集計モデルの更新頻度を設定するために使用する管理者ダイアログ ボックスを示しています。

![更新ダイアログ ボックスのコンフィギュレーション](media/Configure-refresh.png)

データをステージングするジョブの進行状況を監視するには、バッチ ジョブ監視ページを使用します。 (**システム管理** \> **データベース** \> **バッチ ジョブ** の順に選択します。) デモ データを使用している場合、ジョブは 1 分ほどかかります。 データがエンティティ格納に格納された後、レポートを作成できます。 

### <a name="step-2-connect-to-the-local-entity-store-database"></a>手順 2: ローカル エンティティ格納データベースに接続する
1. Power BI Desktop を起動します。 Power BI Desktop のアップデートが使用可能な場合は、それらをダウンロードし、適用する必要があります。 
2. Power BI **ようこそ** ページで、**データの取得** を選択します。 

    または、Power BI Desktop が開始するとき、**データの取得** \> **SQL Server** を選択することができます。 

    ![Power BI Desktop でデータ メニューを取得する](media/Power-BI-Desktop-Get-Data.png)

3. **SQL Server データベース** ダイアログ ボックスに **.** と入力します。 サーバー名として、および **AxDW** をデータベースとして。 その後、**DirectQuery** オプションを選択します。 

    次の図は、Power BI Desktop がローカルのエンティティ格納データベースにアクセスするための設定を示しています。

    ![ローカル エンティティ格納データベースにアクセスするための設定](media/Connect-to-SQL-Database.png)

    > [!NOTE]
    > **インポート** オプションは現在サポートされていません。

4. **OK** を選択します。 

    **ナビゲーター** ダイアログ ボックスが表示されます。 このダイアログ ボックスを使用して、レポートの対象となるテーブルとビューをエンティティ格納から選択します。 

5. 検索ボックスで、**Retail** と入力して RetailCube 集計測定に関連するエンティティについてフィルター処理します。
6. ナビゲーターに表示された **RetailCube\_RetailTransDetailsView** テーブルを選択し、**読み込み** を選択します。 

レポートを作成できるようになりました。 測定およびフィールドはキャンバスにドラッグして、データおよび傾向を対話的に参照することができます。

次の図は、ローカルの Entity Store データベースをソースとして使用する基本レポートを示しています。

![Power BI Desktop レポート](media/Power-BI-Desktop-Report.png)

Power BI Desktop でも計算の作成がサポートされ、複数の集計測定のデータを組み合わせることができます。 数分で、ローカルの開発環境でデータを使用することにより分析レポートを作成することができます。 レポートに問題がなければ、それを実稼働環境に移行できます。これにより、ユーザーは、そのレポートを使用して、実稼働データにかかわることができます。

## <a name="validating-reports-in-a-demo-environment"></a>デモ環境でのレポートの検証

レポートにはデベロッパー環境のデモまたはテスト データが表示されます。 デモ環境にレポートを統合する場合は、引き続きこのレポートを PowerBI.com アカウントに公開し、クライアントに固定することができます。 

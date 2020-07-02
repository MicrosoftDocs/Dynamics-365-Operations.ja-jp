---
title: Azure Data Lake の Finance and Operations アプリ データ
description: このトピックでは、Data Lakeを実装した Finance and Operations アプリ環境の設定方法を説明します。
author: MilindaV2
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 96283
ms.assetid: ''
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Platform Update 34
ms.openlocfilehash: 6184a50d14c1bc81b86249e6b95f6fdbe1ed3517
ms.sourcegitcommit: a5009c8958037afbaa1dd4f1469255b187ced93a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454998"
---
# <a name="finance-and-operations-apps-data-in-azure-data-lake"></a>Azure Data Lake の Finance and Operations アプリ データ

[!include [banner](../includes/banner.md)]

> [!NOTE]
> **Azure Data Lake へのエクスポート**機能は、Microsoft Dynamics 365 Finance and Operations アプリで対応しているすべての地域および環境では使用できない場合があります。 Life cycle services (LCS)、または Finance and Operations アプリで **Azure Data Lake へのエクスポート**の機能が見つからない場合は、ご利用の環境でこの機能を使用できません。 この機能へのアクセスを許可する場合は、機能担当チームにメールでお問い合わせください (**FnODataLakePreview@service.microsoft.com**)。 この機能をご利用頂けるよう、迅速に対応します。 現時点では、 **Azure Data Lake へのエクスポート**機能は、Tier 1 (開発者) 環境では使用できません。 この機能を有効化するには、クラウドベースの Tier 2 またはそれ以上の環境が必要です。
> Data Lakeで集計測定を使用できるようにするには、[エンティティ ストアを Data Lake として使用可能にする](entity-store-data-lake.md) に記載されている方法に従ってこの機能を引き続き使用してください。
 
 
**Azure Data lake にエクスポート**機能を使用すると、アプリケーションのデータをご利用の Azure Data lake (Gen 2) の Finance and Operations アプリにコピーできます。 このシステムでは、含めるテーブルやエンティティを選択できます。 必要なデータを選択した後、システムが初期コピーを行います。 システムは、変更、削除、追加を適用することで、選択したデータを最新の状態に保ちます。 Finance and Operations アプリのインスタンスのデータを変更後、data lake でデータが使用可能になるまでには数分を要する場合があります。 

この機能を使用するには、**Data Lake へのエクスポート**を構成する必要があります。 詳細については、[Azure Data Lake へのエクスポートの構成](configure-export-data-lake.md)を参照してください。


## <a name="turn-on-the-export-data-to-azure-data-lake-feature"></a>Azure Data Lake へのデータのエクスポート機能を有効にします

管理者は事前に、**Azure Data Lake へのエクスポート**  機能を有効化しておく必要があります。 これを行うには、**機能の管理** ワークスペースにアクセスし、**Azure Data Lake にデータをエクスポート** 機能を選択し、**有効化** を選択してください。

この機能を有効化すると、**システムの管理** の配下に **Azure Data Lake にエクスポートする** オプションが表示されます。

## <a name="select-data"></a>データの選択

Data Lake にステージングする必要のあるテーブルとエンティティを選択することができます 。

1. ご利用の環境で、**システム管理** \> **Azure Data Lake にエクスポートする** へと移動します。
2. **Data Lake にエクスポートするデータフィードの構成** を選択します。
3. **テーブルの選択** タブの、**Data Lake に対するデータフィードの構成** ページで、 Data Lake にステージングするデータ テーブルを選択します。 テーブルは、表示名またはシステム名で検索できます。 テーブルが既に同期されているかどうかを確認することもできます。 
4. 完了後に、**テーブルの追加** を選択し、選択したテーブルを Data Lake に追加します。

    ![テーブルの選択](./media/Export-Tables-toData-lake-unselectedv2.png)

5. **データフィードの有効化** を選択し 、**OK** を選択します。 テーブルを追加する際に、このテーブルの状態が **初期化中** と表示される場合があります。 これは、データの初期コピーを作成していることを意味します。 初期コピーが完了すると、状態が **実行中** に変更されます

エラーが発生した場合は、状態が **無効** と表示されます。 **実行中**の状態を確認する際に、データ レイクのデータを使用でき ます。 **初期化**または**無効化**状態の間にデータ レイクデータを使用している場合は、一部のデータが表示されないことがあります。 

必要な特定のテーブルについて詳しくない場合は、エンティティを使用してテーブルを選択することができます。 エンティティはデータの抽象度が高く、複数のテーブルを含む場合があります。 エンティティを選択することで、それを構成するテーブルも選択することになります。
    
7. **使用するエンティティの選択** タブでエンティティを選択し、**エンティティを使用してテーブルを追加する** を選択します。

    ![エンティティを使用したテーブルの選択](./media/Export-Entities-toData-lake-unselectedv2.png)
    
    テーブルを選択する方法を問わず、Data Lake ではテーブルがステージングされます。

## <a name="monitor-the-tables-in-data-lake"></a>Data Lake のテーブルを監視する

システムが Data Lake でデータの更新を維持するため、データのエクスポートの監視や、スケジュールを設定する必要はありません。 **Data Lake に対するデータフィードの構成** ページの **アクティブ** タブで、進行中のデータ エクスポートの状態を確認することができます。

![テーブルの監視の進行状況](./media/Export-Tables-toData-lake-monitorv2.png)

## <a name="troubleshooting-common-issues-and-errors"></a>一般的な問題とエラーに対するトラブルシューティング

### <a name="export-to-data-lake-feature-is-not-available-in-your-region-andor-your-environment-at-this-time"></a>Data Lake へのエクスポート機能が表示されない場合は、この機能がご利用の環境や地域で対応していないことを意味します
この機能は、Tier 1 (開発者) 環境では使用できません。 バージョン 10.0.12、またはそれ以上のプラットフォーム更新プログラムを含むサンドボックス環境 (Tier 2 またはそれ以降) が必要です。

この機能は、 Finance and Operations アプリが利用可能となっている Azure の地域で利用できない場合や、ご利用の環境によっては利用できない場合があります。 この機能へのアクセスを許可する場合は、機能担当チームにメールでお問い合わせください (**FnODataLakePreview@service.microsoft.com**)。 この機能をご利用頂けるよう対応いたします。

### <a name="export-to-data-lake-feature-is-currently-being-installed-for-your-environment-please-check-back-later"></a>Data Lake へのエクスポート機能は、ご利用の環境にインストールされています。 後でもう一度ご確認ください。
この機能を使用するには、Data Lake へのエクスポートを構成する必要があります。 詳細については、[Azure Data Lake へのエクスポートの構成](configure-export-data-lake.md)を参照してください。

### <a name="export-to-data-lake-add-in-is-not-installed"></a>Data Lake アドインへのエクスポート機能がインストールされていません。 
Dynamics Lifecycle Services (LCS) を使用してこのアドインをインストールする場合は、管理者に問い合わせてください。 この機能を使用するには、Data Lake へのエクスポートを構成する必要があります。 詳細については、[Azure Data Lake へのエクスポートの構成](configure-export-data-lake.md)を参照してください。

### <a name="export-to-data-lake-feature-failed-to-install-in-dynamics-life-cycle-services-lcs"></a>Data Lake へのエクスポート機能は、Dynamics Life Cycle Services (LCS) へのインストールに失敗しました。 
Data Lake アドインへのエクスポート機能を再インストールするには、管理者に問い合わせてください。 問題が解消しない場合は、サポートにお問い合わせください。 Data Lake へのエクスポート機能を構成した際に、エラーが表示される場合があります。 または、ご利用の環境の変更がされている場合は、構成後に Data Lake にアクセスした際にエラーが発生する場合があります。 詳細については、[Azure Data Lake へのエクスポートの構成](configure-export-data-lake.md)を参照してください。

### <a name="export-to-data-lake-feature-is-temporarily-unavailable-please-check-back-later"></a>Data Lake へのエクスポート機能は、一時的に使用できなくなります。 後でもう一度ご確認ください。
このエラーが長時間継続するする場合は、サポートに連絡してください。  


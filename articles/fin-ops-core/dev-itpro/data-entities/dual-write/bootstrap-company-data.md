---
title: 会社データの初期化
description: このトピックでは、デュアル書き込み接続を有効にする前に、会社情報を使用してデータを初期化する方法について説明します。
author: RamaKrishnamoorthy
ms.date: 12/01/2020
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e9680f16eec4ce663e66ffb4044c8f7c6f4224a
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060957"
---
# <a name="initialize-company-data"></a>会社データの初期化

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



ビジネス データを持つ既存の Microsoft Dataverse インスタンスまたは財務と運用アプリ インスタンスを所有している場合、それに対して二重書き込み接続を有効にすることをお勧めします。 この場合は、二重書き込みを有効にする前に、会社情報を使用して Dataverse データまたは財務と運用アプリ データを初期化する必要があります。 この初期化プロセスは、*bootstrapping* と呼ばれる場合があります。

このトピックには、デュアル書き込み用 Dataverse のデータを初期化するために、[Azure Data Factory](/azure/data-factory/introduction) の使い方をを説明するサンプル シナリオが含まれます。 すべてのテーブル、エラー処理のシナリオ、またはルックアップについては説明しません。 照会としてこのトピックとテンプレートを使用し、独自の Azure Data Factory パイプラインを設定して、データを Dataverse にインポートまたは  Dataverse に更新します。

## <a name="high-level-scenario"></a>高レベルのシナリオ

財務と運用アプリの **顧客** テーブル、および Dataverse の **アカウント** テーブルについて考えます。

- 最初の書き込みを使用して、財務と運用アプリから Dataverse へ、**会社**、**顧客グループ** および **支払条件** などの照会と依存テーブルをコピーします。
- データ管理フレームワークを使用して、コンマ区切り値 (CSV) 形式で財務と運用アプリからデータをエクスポートします。 たとえば、財務と運用アプリの **DataAreaId** フィールドを使用して、各会社から顧客をエクスポートするように、データ管理でエクスポート プロジェクトを設定します。 このプロセスは、1 回の手動プロセスです。
- Azure Blob Storage を使用し、ルックアップと変換用の CSV ファイルを格納します。 Finance and Operations 顧客の CSV ファイルを Azure Blob Storage にアップロードします。
- Azure Data Factory を使用し、Dataverse のデータを初期化します。

次の図はワークフローを示します。

:::image type="content" source="media/boot-process-flow.png" alt-text="高レベル フロー。":::

このシナリオは、次の前提に基づいています。

- ソース データは財務と運用アプリにあります。
- アカウントが Dataverse に存在し、財務と運用アプリに存在しない場合は、このフローの一部として初期化されません。 Dataverse に保存されているデータの量に基づいて、DIXF または [初期同期](initial-sync-guidance.md) 機能を使用します。
- Customer Engagement アプリのすべてのアカウント レコードには、Finance and Operations ナチュラル キーと一致するナチュラル キー (アカウント番号) が設定されています (**CustomerAccount**)。 
- 行には、アプリ全体での 1 対 1 (1:1) マッピングがあります。

> [!NOTE]
> 財務と運用アプリと Dataverse の両方で、顧客レコードが作成されると、関係者レコードが暗黙的に作成されます。 

## <a name="prerequisites"></a>必要条件

- **Azure サブスクリプション** – 既存の Azure サブスクリプションに対する **貢献者のアクセス** があります。 Azure サブスクリプションをお持ちでない場合は、開始前に[フリー Azure アカウント](https://azure.microsoft.com/free/) を作成してください。
- **Azure Storage アカウント** – Azure Srage アカウントがあります。 ストレージ アカウントを持っていない場合は、[Azure Storage アカウントを作成](/azure/storage/common/storage-account-create?tabs=azure-portal#create-a-storage-account) の手順に従ってください。
- **Azure データ ファクトリ** – [データ ファクトリを作成](/azure/data-factory/tutorial-copy-data-portal#create-a-data-factory) の手順に従い Azure Data Factory のリソースを作成します。
- **財務と運用アプリ** – データ管理フレームワークを使用して、CSV 形式でデータをエクスポートします。 詳細については、 [データ管理の概要](../data-entities-data-packages.md) を参照してください。 このテンプレートでは、顧客が **CustCustomerV3Entity** テーブルを使用してエクスポートされます。
- **Dynamics 365 Dataverse** – Dataverse 管理者ユーザーの認証情報を使い、データを初期化します。
- **デュアル書き込み** – デュアル書き込みソリューションがインストールされ、初期書き込みを使用して参照データがコピーされます。

## <a name="deployment-steps"></a>配置の手順

### <a name="set-up-an-azure-storage-account"></a>Azure ストレージ アカウントの設定

Azure ストレージ アカウントを持っていない場合は、[Azure ストレージ アカウントを作成](/azure/storage/common/storage-account-create?tabs=azure-portal#create-a-storage-account) の手順に従ってください。 ストレージ アカウントで、**ce-data** という名前のコンテナーを 1 つ作成します。 このコンテナには、すべてのデータ ファイルが格納されます。 データセットおよびパイプライン内のコンテナは、必要に応じ変更できます。 次の図に示すように、**アクセス キー** に移動し、**接続文字列** 値をコピーします。 この値は、Azure Data Factory テンプレートをインポートする際に必須です。

:::image type="content" source="media/boot-storage-account.png" alt-text="アクセス キーの設定。":::

### <a name="deploy-an-azure-data-factory-template"></a>Azure Data Factory テンプレートの配置

1. 作成した Azure データ ファクトリーの名前をメモします。
2. Azure ストレージ アカウントの接続文字列をメモします。
3. Dataverse インスタンスのサービス URI と管理者ユーザーの名前、パスワードをメモします。

    次の表に、必要なパラメーターを示します。

    | パラメーター名 | 説明 | サンプル値 |
    |---|---|---|
    | ファクトリー名 | データ ファクトリー名 | *BootstrapDataverseDataADF* |
    | Bootstrap blob storage account Linked Service\_connection String | Blob ストレージの接続文字列 | ストレージ アカウントの作成時にコピーした値 |
    | Bootstrap Dynamics 365 Linked Service\_service URI | Dataverse インスタンスの URI | `https://contosod365.crm4.dynamics.com` |
    | Bootstrap Dynamics 365 Linked Service\_properties\_type Properties\_username | Dynamics 365 管理者ユーザーのユーザー ID | `<adminservice@contoso.onmicrosoft.com>` |
    | Bootstrap Dynamics 365 Linked Service\_password | Dynamics 365 管理者ユーザーのパスワード | _\*\*\*\*\*\*\*\*_ | 

4. [Azure Resource Manager (ARM) テンプレート ファイル](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Bootstrapping/arm_template.json) をローカル ディレクトリにダウンロートします。
5. Azure ポータルで、[カスタム デプロイ](https://ms.portal.azure.com/#create/Microsoft.Template) に移動します。
6. **独自のテンプレートをエディターに作成** を選択します。
7. **ファイルの読み込み** を選択し、先にダウンロードした ARM テンプレート ファイルを検索して選択します。 その後、**保存** を選択します。
8. 必要なパラメータを指定し、**確認** を選び、**作成** を選択します。

    :::image type="content" source="media/boot-custom-deployment.png" alt-text="テンプレートのカスタマイズ。":::

9. デプロイ後、リスト ウィンドウに **パイプライン**、**データセット** および **データ フロー** セクションが表示されます。

    :::image type="content" source="media/boot-pipeline.png" alt-text="パイプライン、データセット、およびデータ フロー":::

## <a name="run-the-process"></a>プロセスを実行する

1. 財務と運用アプリで、データ管理フレームワークを使用して CSV 形式でデータをエクスポートします。 詳細については、 [データ管理の概要](../data-entities-data-packages.md) を参照してください。 このテンプレートでは、顧客データが **CustCustomerV3Entity** テーブルからエクスポートされます。 **CustCustomerV3Entity** を設定し、**FullPripriyAdtomer** フィールド マップをマッピングから削除します。 **DataAreaId** フィールドを CSV ファイルに追加します。 エクスポートしたファイル名を **01-CustomersV3Export-Customers V3.csv** にして、**ce-data** と名前をつけた Azure ストレージ アカウントにアップロードします。

    :::image type="content" source="media/boot-customer-file.png" alt-text="Finance and Operations 顧客ファイル。":::

2. [サンプル顧客ファイル](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Bootstrapping/01-CustomersV3Export-Customers%20V3.csv) をダウンロードします。

3. Azure Data Factory から **CountAccountsPipeline** を実行します。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

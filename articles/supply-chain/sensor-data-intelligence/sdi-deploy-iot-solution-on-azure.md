---
title: " IoT ソリューションを Azure に配置する"
description: Sensor Data Intelligence は、Microsoft Azure に接続されたセンサーからのデータを使用しています。 この記事では、Azure サブスクリプションで、Internet of Things (IoT) ソリューションを配置する方法について説明します。
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5026f234f1b2f38e7041098421d0261fd468db96
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643721"
---
# <a name="deploy-an-iot-solution-on-azure"></a> IoT ソリューションを Azure に配置する

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Sensor Data Intelligence は、Microsoft Azure に接続されたセンサーからのデータを使用しています。 Azure を有効にして、スポンサーから データを取得して Dynamics 365 Supply Chain Management で共有するには、Azure サブスクリプションで Internet of Things (IoT) ソリューションを配置する必要があります。 次のアーキテクチャ図は、ソリューションとそのコンポーネントの概要を示しています。

![Sensor Data Intelligence のアーキテクチャ図。](media/sdi-architecture.png "Sensor Data Intelligence のアーキテクチャ図")

## <a name="video-instructions"></a>ビデオの指示

次のビデオでは、[センサー データ インテリジェンス機能を有効](sdi-enable-feature.md)にし、必要な Azure リソースを配置する方法を説明します。 この記事の他のセクションでは、テキスト ベースの形式で同じ手順を示します。

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58g3I]

## <a name="procedure"></a>手順

Azure で必要なリソースを配置するには、次の手順を実行します。

1. 管理者として Supply Chain Management にサインインします。
1. **システム管理 \> 設定 \> Sensor Data Intelligence \> Azure リソースを配置して接続** に移動して、配置ウィザードを開きます。
1. **ようこそ** ページ で、情報を読み、**次へ** を選択 します。
1. **サンプルの IoTソリューションをAzureに配置する** ページで、この情報を読み、**手順** セクションで **配置** を選択します。
1. 新しいブラウザのタブが開き、Azure ポータルに移動して、Azure リソースを配置できます。 プロンプトされたら、Azure の サブスクリプションの資格情報を使用してサイン インします。
1. **カスタム配置** ページの **サブスクリプション** フィールドで、サブスクリプションを選択します。
1. **リソース グループ** フィールドで **新規作成** を選択し、配置するAzure コンポーネントのリソース グループを作成します。
1. 表示されるドロップダウン ダイアログ ボックスの **名前** フィールドに、新しいリソース グループの名前を入力します (*IoTデモ* など)。 その後、**OK** を選択します。
1. 次のフィールドを設定します。

    - **リソース グループ** - 作成したリソース グループを選択します。
    - **地域** - Supply Chain Management 環境が配置されている地域が理想的な地域を選択します。 Azure 地域の価格は異なるので、次に示します。 自分の地域の見積もり原価は、[Sensor Data Intelligence 価格計算機](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68) を使用して見ることができます。
    - **Supply Chain Management 環境 URL** - Supply Chain Management 環境の URL を入力します。
    - **既存の Azure IoT ハブを再利用 –** このチェック ボックスはオフのままにします。

1. **次: レビュー + 作成** を選択します。
1. **カスタム配置** ページで、検証に通ったことを確認した後、**作成** を選択します。
1. **配置は進行中です** ページでは、配置の進捗状況が追跡されます。 この配置プロセスには最大で 30 分かかります。 **配置は進行中です** ページで、配置が完了したと示されている場合は、リソース グループ名のリンクを選択して、グループに配置されているリソースの一覧を示すページが開きます。
1. リソース の一覧で、**タイプ** フィールドが *管理 されたID* に設定されているレコードを検索します。 **名前** 列で、名前を選択して、リリースの詳細ページを開きます。
1. **クライアント ID** フィールドに値をコピーします (**クリップボードにコピー** ボタンを選択する場合など)。
1. Supply Chain Management が実行されているブラウザのタブに戻るが、*Azureポータルのタブは閉じません*。 **サンプル のIoTソリューションを Azure に配置** ウィザード ページは、まだ開いている必要があります。 
1. **次へ** を選択します。
1. **Azureリソースへの接続** ページの **Azure AD アプリケーション クライアント ID** フィールドに、コピーした **クライアント ID**  値を貼り付けます。
1. Azure ポータルが開いているブラウザ タブに戻るが、*Supply Chain Management のタブは閉じません*。 リソースの詳細ページはまだ開いています。
1. 新しいリソース グループのリソースの一覧に戻る場合は、ブラウザの **戻る** ボタンをクリックします。
1. リソース の一覧で、**タイプ** フィールドが *Azure Cache for Redis* に設定されているレコードを検索します。 **名前** 列で、名前を選択して、リリースの詳細ページを開きます。
1. 左側のナビゲーション ウィンドウで、**アクセス キー** を選択します。
1. **アクセス キー** ページで、**プライマリ接続文字列 (StackExchange.Redis)** に表示される値をコピーします (**クリップボードにコピー** ボタンを選択する場合など)。
1. Supply Chain Management が実行されているブラウザ タブに戻ります。 **Azure リソースに接続** ページ は開いている必要があります。
1. **Redis メトリック店舗の接続文字列** フィールドに、コピーした **プライマリ接続文字列 (StackExchange.Redis)** 値を貼り付けます。
1. **完了** を選択します。

これで、Sensor Data Intelligence が Azure サブスクリプションで配置されます。

> [!NOTE]
> **Sensor Data Intelligence パラメータ** ページを開いて、Supply Chain Management に保存される接続情報をいつでも表示または編集できます。 詳細については、[Sensor Data Intelligence パラメータ](sdi-parameters.md) を参照してください。

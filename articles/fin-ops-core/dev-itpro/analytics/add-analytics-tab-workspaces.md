---
title: Power BI Embedded を使用したワークスペースへの分析の追加
description: このトピックでは、ワークスペースの分析タブで Power BI レポートを組み込む方法を説明します。
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: dd88537506521fd37aa170c7e8f43bcf5a106836
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174354"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Power BI Embedded を使用したワークスペースへの分析の追加

[!include [banner](../includes/banner.md)]

> [!NOTE]
> この機能は、Finance and Operations (バージョン 7.2 以降) でサポートされています。

## <a name="introduction"></a>はじめに
このトピックでは、ワークスペースの**分析**タブで Microsoft Power BI レポートを組み込む方法を説明します。 ここで示した例では、フリート管理アプリケーションの **予約管理** ワークスペースを拡張して、分析ワークスペースを**分析**タブに埋め込みます。

## <a name="prerequisites"></a>前提条件
+ プラットフォーム更新プログラム 8 以降を実行する開発環境へのアクセス。
+ Microsoft Power BI Desktop を使用して作成され、エンティティ格納 データベースから取得されたデータ モデルを持つ分析レポート (.pbix ファイル) です。

## <a name="overview"></a>概要
既存のアプリケーション ワークスペースを拡張する場合でも、自分の新しいワークスペースを導入する場合でも、埋め込み分析ビューを使用して、ビジネス データの洞察的でインタラクティブなビューを提供できます。 分析ワークスペース タブを追加するプロセスには、4 つのステップがあります。

1. Dynamics 365 リソースとして .pbix ファイルを追加します。
2. 分析ワークスペース タブを定義します。
3. ワークスペース タブに .pbix リソースを埋め込みます。
4. オプション: 表示をカスタマイズする拡張機能を追加します。

> [!NOTE]
> 分析レポートを作成する方法の詳細については、[Power BI Desktop の使い方](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/)を参照してください。 このページは、魅力的な分析レポート作成ソリューションの作成に役立つ素晴らしいソースです。

## <a name="add-a-pbix-file-as-a-resource"></a>リソースとして .pbix ファイルを追加します。
開始する前に、ワークスペースに埋め込む Power BI レポートを作成または取得する必要があります。 分析レポートを作成する方法の詳細については、[Power BI Desktop の使い方](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/)を参照してください。

.pbix ファイルを Visual Studio プロジェクト コンポーネントとして追加するには、次の手順を実行します。

1. 該当するモデルで新しいプロジェクトを作成します。
2. ソリューション エクスプローラーで、プロジェクトを選択し、右クリックした後に、**追加** \> **新しい品目**の順に選択します。
3. **新しい項目の追加**ダイアログ ボックスの**工程コンポーネント**で**リソース**テンプレートを選択します。
4. X++ メタデータのレポートを参照するために使用する名前を入力し、**追加**をクリックします。

    ![[新しい項目の追加] ダイアログ ボックスの追加](media/analytical-workspace-add.png)

5. 分析のレポートの定義を含む .pbix ファイルを見つけて、**未処理**をクリックします。

    ![[リソース ファイル] ダイアログ ボックスをオンにします。](media/analytical-workspace-select-resource.png)

Dynamics 365 リソースとして .pbix ファイルを追加したため、ワークスペースにレポートを埋め込み、メニュー項目を使用して直接リンクを追加できるようになりました。

## <a name="add-a-tab-control-to-an-application-workspace"></a>アプリケーション ワークスペースへのタブ コントロールの追加
この例では、**FMClerkWorkspace** フォームの定義に**分析**タブを追加することで、フリート管理モデルの **引当管理** ワークスペースを拡張します。

次の図は、**FMClerkWorkspace** フォームが Microsoft Visual Studio のデザイナーにどのように表示されるかを示しています。

![変更する前の FMClerkWorkspace フォーム](media/analytical-workspace-definition-before.png)

次の手順に従って、**引当管理**ワークスペースの定義を拡張します。

1. デザイン定義を拡張するフォーム デザイナーを開きます。
2. 設計の定義では、**デザイン | パターン: 操作ワークスペース**というラベルが付いた最上位の要素を選択します。
3. 右クリックし、**新規** \> **タブ**の順に選択して、**FormTabControl1** という名前の新しいコントロールを追加します。
4. フォーム デザイナーで **FormTabControl1** を選択します。
5. 、**新しいタブ ページ**を右クリックし、選択し、新しいタブ ページを追加します。
6. **ワークスペース**など、タブ ページをわかりやすい名前に変更します。
7. フォーム デザイナーで **FormTabControl1** を選択します。
8. **新しいタブ ページ**を右クリックし、選択します。
9. **分析**など、タブ ページをわかりやすい名前に変更します。
10. フォーム デザイナーで、**分析 (タブ ページ)** を選択します。
11. **キャプション**プロパティを**分析**に設定します。
12. コントロールを右クリックし、**新規** \> **グループ**の順に選択して、新しいフォーム グループ コントロールを追加します。
13. **powerBIReportGroup** など、フォーム グループをわかりやすい名前に変更します。
14. フォーム デザイナーで、**PanoramaBody (タブ)** を選択し、コントロールを**ワークスペース**タブの上にドラッグします。
15. 設計の定義では、**デザイン | パターン: 操作ワークスペース**というラベルが付いた最上位の要素を選択します。
16. **パターンの削除**を右クリックし、選択します。
17. もう一度右クリックし、**パターンの追加** \> **ワークスペース タブ**の順に選択します。
18. 変更を確認するビルドを実行します。

次の図は、これらの変更が適用された後に設計がどのように表示されるかを示します。

![変更後の FMClerkWorkspace](media/analytical-workspace-definition-after.png)

ワークスペース レポートの埋め込みに使用するフォーム コントロールを追加したため、親コントロールのサイズがレイアウトに対応できるように、それを定義する必要があります。 既定では、**フィルタ ウィンドウ**ページと**タブ**ページの両方がレポートに表示されます。 ただし、これらのコントロールの表示/非表示を、レポートの対象となる消費者の必要に応じて変更することができます。

> [!NOTE]
> 埋め込みのワークスペースについては、ページの一貫性を保つため、拡張機能を使用して、**フィルタ ウィンドウ**および**タブ**ページを非表示にすることをお勧めします。

これでアプリケーション フォームの定義を拡張するためのタスクが完了しました。 カスタマイズを行うために拡張機能を使用する方法に関する詳細については、[カスタマイズ: オーバーレイおよび拡張機能](../extensibility/customization-overlayering-extensions.md) を参照してください。

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a>ビューアー コントロールを埋め込むための X++ ビジネス ロジックの追加
これらの手順に従い、**引当管理** ワークスペースに埋め込まれているレポート ビューアー コントロールを初期化するビジネス ロジックを追加します。

1. **FMClerkWorkspace** フォーム デザイナーを開き、デザイン定義を拡張します。
2. F7 キーを押し、コードの定義の背後にあるコードにアクセスします。
3. 次の X++ コードを追加します。

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. 変更を確認するビルドを実行します。

これで、埋め込みレポート ビューアー コントロールを初期化するビジネス ロジックを追加するタスクを完了しました。 次の図は、これらの変更が適用された後にワークスペースがどのように表示されるかを示します。

![ワークスペースに埋め込まれているレポート](media/analytical-workspace-final.png)

> [!NOTE]
> 既存の操作ビューは、ページのタイトルの下のワークスペース タブを使用してアクセスできます。

## <a name="reference"></a>参照

### <a name="pbireporthelperinitializereportcontrol-method"></a>PBIReportHelper.initializeReportControl 方法
このセクションでは、フォーム グループ コントロールで Power BI レポート (.pbix リソース) の埋め込みに使用されるヘルパー クラスに関する情報を提供します。

#### <a name="syntax"></a>構文
```
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a>パラメーター

| 氏名             | 説明                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| resourceName     | .pbix リソースの名前。                                                                              |
| formGroupControl | Power BI レポートのコントロール適用先のフォーム グループ コントロール。                                              |
| defaultPageName  | 既定のページの名前                                                                                       |
| showFilterPane   | フィルタ ウィンドウを表示 (**true**) または非表示 (**false**) するかを示すブール値。     |
| showNavPane      | ナビゲーション ウィンドウを表示 (**true**) または非表示 (**false**) するかを示すブール値。 |
| defaultFilters   | Power BI レポートの既定のフィルター。                                                                 |

---
title: Power BI Embedded を使用して分析ワークスペースおよびレポートをセキュリティで保護
description: このトピックでは、Power BI Embedded を使用して提供されるレポートとデータ セットの両方へのアクセスを保護するための推奨方法について説明します。
author: RichdiMSFT
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.custom: 21551
ms.assetid: ''
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fea9957810d306e3c76d20cab0ede630334d1f102d11fea9121bd55530b4e156
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721916"
---
# <a name="help-secure-analytical-workspaces-and-reports-by-using-power-bi-embedded"></a>Power BI Embedded を使用して分析ワークスペースおよびレポートをセキュリティで保護

[!include [banner](../includes/banner.md)]

> [!NOTE]
> この機能は、Microsoft Dynamics 365 for Finance and Operations、Enterprise edition (2017 年 7 月) (バージョン7.2) 以降のリリースでサポートされています。

## <a name="introduction"></a>はじめに
このトピックでは、Microsoft Power BI Embedded を使用して提供される、分析ワークスペースとレポートのセキュリティ保護を支援するアプリケーション開発者向けにウォークスルーを提供します。 ビューアーのアクセス権に基づいてレポートおよびデータ セット両方へのアクセスを保護するための推奨方法について説明します。 このトピックに記載されている手法を使用することにより、ユーザーからレポートを非表示にし、有効な会社のコンテキストに基づいて、特定のユーザーに適したデータ セットを表示するためにレポートをフィルター処理することができます。

## <a name="prerequisites"></a>必要条件
+ プラットフォーム更新プログラム 8 以降を実行する開発環境へのアクセス
+ Microsoft Power BI Desktop を使用して作成され、エンティティ格納データベースから取得されたデータ モデルを持つ分析レポート (.pbix ファイル)

## <a name="overview"></a>概要
既存のアプリケーション ワークスペースを拡張する場合でも、自身のワークスペースを追加する場合でも、埋め込み分析ビューを使用して、ビジネス データの洞察的でインタラクティブなビューを提供できます。 新しい分析ワークスペースおよびレポートを追加する前に、コンテンツを保護するための戦略を確立することは重要です。

Power BI Embedded を使用して分析ソリューションを開発する際には、いくつか注意すべき点があります。 分析レポートはメニュー項目を使用して保護されます。 レポートにアクセスすると、すべての閲覧者はレポートに定義されている基礎データ モデルにアクセスできます。 サービス オプションはレポート データ セットを戻しフィールドを自動的に非表示にすることが可能ですが、レポートのすべての閲覧者はデータ モデル内のフィールドに有効的にアクセスできます。 また、レポートがクライアントに表示される方法に影響を与える X++ 拡張機能が使用できます。 **フィルター** ウィンドウと **レポート** タブの両方を非表示にすることができます。 ただし、Microsoft Power BI フィルターは、クライアント側のスクリプト インジェクションを使用して変更できます。

### <a name="recommendation"></a>推奨事項
シナリオ固有の .pbix ファイルを作成して分析ビューを作成する:

+ ワークスペースを使用して提供される領域の概要
+ 題材固有の分析レポート

    > [!NOTE]
    > これらの分析レポートは、中堅企業や大規模企業に影響を与えるデータを含むレポートを配信するために使用されることがよくあります。

分析レポートを作成する方法の詳細については、[Power BI Desktop の使い方](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/)を参照してください。 このページは、魅力的な分析レポート作成ソリューションの作成に役立つ素晴らしいソースです。

## <a name="help-secure-analytical-views-that-are-provided-through-embedded-power-bi-reports"></a>埋め込み Power BI レポートを通して提供される分析ビューのセキュリティを強化する
Power BI レポート フィルターと **フィルター** ウィンドウは、**分析** タブに埋め込まれたレポートにセッション コンテキストを渡すためのメカニズムとして機能します。**フィルター** ウィンドウの表示のオンとオフを切り替える機能は、セキュリティ機能ではありません。 Power BI レポート フィルターと、**フィルター** ウィンドウを非表示および表示する機能は、アプリケーション デザイナーが行うユーザー エクスペリエンス (UX) の決定です。

定義されている行レベルのセキュリティは Power BI レポートによって継承されていません。 代わりに、アプリケーション開発者は、ワークスペースまたはレポートのセキュリティを高めることができます。

### <a name="help-secure-analytical-workspaces-on-the-analytics-tab"></a>分析タブの分析ワークスペースのセキュリティを強化する
分析ワークスペースはフォーム コントロールに表示される埋め込まれた Power BI レポートです。 次の手順を完了しない限り、ワークスペースにアクセスできるすべてのユーザーには **分析** タブが表示され、Power BI レポートにアクセスできます。

1. 分析ワークスペースのメニュー項目を追加します。
2. ユーザーがメニュー項目にアクセスできることを確認するために、フォームの初期化に **hasMenuItemAccess** アプリケーション プログラミング インターフェイス (API) が使用されていることを確認します。

    ```xpp
    // Note: secure entry point into the Workspace's Analytics report
    if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
    {
        FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
        PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
    }
    ```

上記のロジックは、Power BI ビューアー コントロールの初期化を阻止します。 したがって、空のタブがページに表示されます。 既定では、フレームワークは自動的に空のタブを非表示にします。 したがって、**分析** タブは非表示になっており、ユーザーが分析ワークスペースに関連付けられているメニュー項目へのアクセス権を持たない場合はアクセスできません。

### <a name="help-secure-analytical-reports"></a>分析レポートのセキュリティを強化する
アプリケーションの埋め込み Power BI レポートは、メニュー項目を使用してセキュリティで保護されます。 アプリケーションのメニュー項目を使用して Power BI レポートに直接アクセスを試みるユーザーに、エラーが表示されます。 分析レポートのセキュリティを確保するには、これらの手順に従います。

1. レポートまたは適切なタブのメニュー項目を追加します。既定では、その他のタブが選択されていない場合、レポートの最初のタブが表示されます。
2. メニュー項目を **PowerBIEmbedded\_App** コンフィギュレーション キーにリンクします。

    ![メニュー項目を PowerBIEmbedded_App コンフィギュレーション キーにリンクします。](media/secure-workspace-key.png)

このメニュー項目は、Power BI Embedded サービスの可用性に関連付けられています。 サービスを使用できない場合は、アプリケーションからメニュー項目のリンクが削除されます。

## <a name="help-secure-analytical-workspaces-and-reports-by-company"></a>会社ごとの分析ワークスペースおよびレポートのセキュリティを強化する
Power BI ワークスペースとレポートは会社が保護できます (たとえば、**DataAreaID** 値など)。 アプリケーション ソリューションは、分析ワークスペースとレポートで会社レベルのセキュリティのために、次の手順を適用する必要があります。

このシナリオでは、Contoso USA の販売マネージャーが確認するワークスペースとレポートは、Contoso USA に関連するデータに限定されます。 レポート ビューアーは、会社のコンテキストが変更されない限り、他の会社に関連付けられたデータにアクセスできないようにする必要があります。

1. Microsoft Visual Studio プロジェクト内のリソースをダブルクリックして、Power BI Desktop で分析レポートを開きます。
2. **モデリング** タブで、**ロールの管理** をクリックします。
3. **会社** フィールドを含むデータ モデル内の列に対して新しいロールを作成します。 新しいロールに **CompanyFilter** と名前を付けます。 会社によるアクセスを制限するために、データ モデルに **会社** フィールドが必要です。

    ![新しいロールを作成します。](media/secure-workspace-filter.png)

4. **テーブル フィルターの DAX 式** フィールドに、**\[COMPANY\]=username()** と入力します。
5. ルールが機能することを確認するには、**モデリング** タブで **ロールとして表示** をクリックします。 ダイアログ ボックスで、次のフィールドを設定します。

    1. **なし** チェック ボックスをオフにします。
    2. **その他のユーザー** チェック ボックスをオンにし、テキスト ボックスに **USMF** と入力します。
    3. **CompanyFilter** チェック ボックスをオンにします。

これでレポートに、USMF 企業を経営しているかのようなデータが表示されます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

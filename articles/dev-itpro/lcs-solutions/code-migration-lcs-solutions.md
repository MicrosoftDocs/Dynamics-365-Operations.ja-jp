---
title: Finance and Operations ソリューションのコードの移行
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) で、コードをアップグレードおよび分析する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 06/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Lifecycle Services
ms.custom: 196993
ms.assetid: aa01254e-4c18-43e4-81a1-0ef42a27871d
ms.search.region: Global
ms.author: omarc
ms.openlocfilehash: e0caa16eba5ba3c3ef248e88a61797c28c1d9f6f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369483"
---
# <a name="migrate-code-for-finance-and-operations-solutions"></a>Finance and Operations ソリューションのコードの移行

[!include[banner](../includes/banner.md)]

ソリューション パッケージを完成させるための第一歩は、Microsoft Dynamics Lifecycle Services (LCS) の **Finance and Operations ソリューションの移行と作成**のベスト プラクティスを使用してコードをアップグレードすることです。 ステップが完了したら、カスタマイズ分析のレポート (CAR) を実行する必要があります。 このレポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行します。 

CAR を生成するには、Microsoft Dynamics 365 for Finance and Operations 開発環境で次のコマンドを実行します。

    xppbp.exe -metadata=<local packages folder> -all -model=<ModelName> -xmlLog=C:\BPCheckLogcd.xml -module=<PackageName> -car=<reportlocation>

このコマンドの例を次に示します。

    xppbp.exe -metadata=C:\Packages -all -model=MyAppSuiteCustomizations -xmlLog=C:\temp\BPCheckLogcd.xml -module=ApplicationSuite -car=c:\temp\CAReport.xlsx

xppbp.exe ファイルは、c:\\packages\\bin または I:\\AosService\\Packages\\LocalDirectory\\bin に配置されています。 レポートの**問題**タブ上に表示される警告またはエラーを解決する必要があります。 CAR のコピーを、検証ミーティングよりも前に、Microsoft に送信する必要があります。 詳細については、[カスタマイズ分析のレポート](../dev-tools/customization-analysis-report.md)を参照してください。 問題と例外の詳細については、Dynamics 365 Community ブログの投稿[カスタマイズ分析のレポート: 例外と既知の問題](http://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues)を参照してください。

## <a name="extensibility"></a>拡張性
Microsoft Dynamics 365 for Finance and Operationsバージョン 8.0 (2018年4月) では、すべての製品モデルがシールされます。 したがって、拡張機能ベースのカスタマイズのみが現在サポートされています。 拡張機能の詳細については、[拡張機能](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/extensibility/extensibility-home-page)を参照してください。

ソリューション パッケージを完成させるための第一歩は、LCS の <strong>Migrate and Create Finance and Operations Solutions</strong> のベストプラクティスを使用してコードをアップグレードすることです。 このステップが完了したら、カスタマイズ分析レポートを実行する必要があります。 このレポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行します。 

カスタマイズ分析レポート (CAR) を生成するには、Microsoft Dynamics 365 for Finance and Operations 開発環境で次のコマンドを実行します。

    xppbp.exe -metadata=<local packages folder> -all -model=<ModelName> -xmlLog=C:\BPCheckLogcd.xml -module=<PackageName> -car=<reportlocation>

このコマンドの見方の例を次に示します。

    xppbp.exe -metadata=C:\Packages -all -model=MyAppSuiteCustomizations -xmlLog=C:\temp\BPCheckLogcd.xml -module=ApplicationSuite -car=c:\temp\CAReport.xlsx

xppbp.exe ファイルは、*c:\packages\bin* または *I:\AosService\Packages\LocalDirectory\bin)* にあります。 レポートの**問題**タブ上に表示される警告またはエラーを解決する必要があります。 CAR レポートのコピーは、検証ミーティングよりも前に、Microsoft に送信する必要があります。 詳細については、Finance and Operations ヘルプ トピック、[カスタマイズ分析のレポート](../dev-tools/customization-analysis-report.md) および、問題と例外に関する [Dynamics コミュニティのブログ](http://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues) を参照してください。

<a name="additional-resources"></a>追加リソース
--------
[AppSource の Dynamics 365 for Finance and Operations アプリを公開](lcs-solutions-app-source.md)

[コードの移行の技術概念ガイド](../dev-tools/developer-home-page.md#code-migration)

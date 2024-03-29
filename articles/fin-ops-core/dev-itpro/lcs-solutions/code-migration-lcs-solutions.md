---
title: 財務と運用アプリ ソリューションのコードの移行
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) で、コードをアップグレードおよび分析する方法について説明します。
author: sericks007
ms.date: 06/13/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.custom: 196993
ms.assetid: aa01254e-4c18-43e4-81a1-0ef42a27871d
ms.openlocfilehash: f1c0a970cbd8dbedd8e8f7cff7859ed4a632adf8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270739"
---
# <a name="migrate-code-for-finance-and-operations-apps-solutions"></a>財務と運用アプリ ソリューションのコードの移行

[!include[banner](../includes/banner.md)]

ソリューション パッケージを完成させるための第一歩は、Microsoft Dynamics Lifecycle Services (LCS) の **財務と運用アプリ ソリューションの移行と作成** のベスト プラクティスを使用してコードをアップグレードすることです。 ステップが完了したら、カスタマイズ分析のレポート (CAR) を実行する必要があります。 このレポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行します。 

CAR を生成するには、開発環境で次のコマンドを実行します。

```Console
xppbp.exe -metadata=<local packages folder> -all -model=<ModelName> -xmlLog=C:\BPCheckLogcd.xml -module=<PackageName> -car=<reportlocation>
```

このコマンドの例を次に示します。

```Console
xppbp.exe -metadata=C:\Packages -all -model=MyAppSuiteCustomizations -xmlLog=C:\temp\BPCheckLogcd.xml -module=ApplicationSuite -car=c:\temp\CAReport.xlsx
```

xppbp.exe ファイルは、c:\\packages\\bin または I:\\AosService\\Packages\\LocalDirectory\\bin に配置されています。 レポートの **問題** タブ上に表示される警告またはエラーを解決する必要があります。 CAR のコピーを、検証ミーティングよりも前に、Microsoft に送信する必要があります。 詳細については、 [カスタマイズ分析のレポートt (CAR)](../dev-tools/customization-analysis-report.md)を参照してください。 問題と例外の詳細については、Dynamics 365 Community ブログの投稿[カスタマイズ分析のレポート: 例外と既知の問題](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues)を参照してください。

## <a name="extensibility"></a>拡張性
Microsoft Dynamics 365 Finance バージョン 8.0 (2018年4月) では、すべての製品モデルがシールされます。 したがって、拡張機能ベースのカスタマイズのみが現在サポートされています。 拡張機能の詳細については、[拡張機能](../extensibility/extensibility-home-page.md)を参照してください。

ソリューション パッケージを完成させるための第一歩は、LCS の<strong>財務と運用アプリ ソリューションの移行と作成</strong>のベスト プラクティスを使用してコードをアップグレードすることです。 このステップが完了したら、カスタマイズ分析レポートを実行する必要があります。 このレポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行します。 

カスタマイズ分析レポート (CAR) を生成するには、開発環境で次のコマンドを実行します。

```Console
xppbp.exe -metadata=<local packages folder> -all -model=<ModelName> -xmlLog=C:\BPCheckLogcd.xml -module=<PackageName> -car=<reportlocation>
```

このコマンドの見方の例を次に示します。

```Console
xppbp.exe -metadata=C:\Packages -all -model=MyAppSuiteCustomizations -xmlLog=C:\temp\BPCheckLogcd.xml -module=ApplicationSuite -car=c:\temp\CAReport.xlsx
```

xppbp.exe ファイルは、*c:\packages\bin* または *I:\AosService\Packages\LocalDirectory\bin)* にあります。 レポートの **問題** タブ上に表示される警告またはエラーを解決する必要があります。 CAR レポートのコピーは、検証ミーティングよりも前に、Microsoft に送信する必要があります。 詳細については、 [カスタマイズ分析のレポート (CAR)](../dev-tools/customization-analysis-report.md) および、問題と例外に関する [Dynamics コミュニティのブログ](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues) を参照してください。

## <a name="additional-resources"></a>追加リソース
[AppSource でアプリを公開するための要件](lcs-solutions-app-source.md)

[開発およびカスタマイズのホーム ページ](../dev-tools/developer-home-page.md#code-migration)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]


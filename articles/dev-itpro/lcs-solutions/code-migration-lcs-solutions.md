---
title: "LCS ソリューションのコードの移行"
description: "このトピックでは、LCS ソリューションのコードをアップグレードおよび分析する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Lifecycle Services
ms.custom: 196993
ms.assetid: aa01254e-4c18-43e4-81a1-0ef42a27871d
ms.search.region: Global
ms.author: omarc
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 4e5970447a3120bed30280d5de8ea4a331020aaf
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="migrate-code-for-an-lcs-solution"></a>LCS ソリューションのコードの移行

[!include [banner](../includes/banner.md)]

ソリューション パッケージを完成させるための第一歩は、LCS の <strong>Migrate and Create Finance and Operations Solutions</strong> のベストプラクティスを使用してコードをアップグレードすることです。 このステップが完了したら、カスタマイズ分析レポートを実行する必要があります。 このレポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行します。 

カスタマイズ分析レポート (CAR) を生成するには、Microsoft Dynamics 365 for Finance and Operations 開発環境で次のコマンドを実行します。

    xppbp.exe -metadata=<local packages folder> -all -model=<ModelName> -xmlLog=C:\BPCheckLogcd.xml -module=<PackageName> -car=<reportlocation>

このコマンドの見方の例を次に示します。

    xppbp.exe -metadata=C:\Packages -all -model=MyAppSuiteCustomizations -xmlLog=C:\temp\BPCheckLogcd.xml -module=ApplicationSuite -car=c:\temp\CAReport.xlsx

xppbp.exe ファイルは、*c:\packages\bin* または *I:\AosService\Packages\LocalDirectory\bin)* にあります。 レポートの**問題**タブ上に表示される警告またはエラーを解決する必要があります。 CAR レポートのコピーは、検証ミーティングよりも前に、Microsoft に送信する必要があります。 詳細については、Finance and Operations ヘルプ トピック、[カスタマイズ分析のレポート](../dev-tools/customization-analysis-report.md) および、問題と例外に関する [Dynamics コミュニティのブログ](http://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues) を参照してください。

<a name="additional-resources"></a>その他のリソース
--------

[AppSource 向け LCS ソリューション ホームページ](lcs-solutions-app-source.md)

[コードの移行の技術概念ガイド](../dev-tools/developer-home-page.md#code-migration)





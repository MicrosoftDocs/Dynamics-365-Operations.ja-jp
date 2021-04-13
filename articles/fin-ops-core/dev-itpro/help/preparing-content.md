---
title: ヘルプ ウィンドウで使用するコンテンツの準備
description: このトピックでは、[ヘルプ] ウィンドウで使用できるようにコンテンツを準備する方法について説明します。
author: edupont04
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: fba424452ea4d4b9c2eaac7c0d079efd53495774
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748775"
---
# <a name="prepare-content-for-use-with-the-help-pane"></a>ヘルプ ウィンドウで使用するコンテンツの準備

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce の **ヘルプ** ウィンドウで使用できるコンテンツは、既存の Microsoft コンテンツから取得することも、既存の Dynamics AX 2012 のヘルプ コンテンツから移行することも、新しいファイルとして作成することもできます。

Microsoft では、Finance、Supply Chain Management、Commerce でサポートされているロケールについて複数言語のヘルプを作成しています。 ただし、ロケールのサポートは、これらのロケールに限定されません。

## <a name="creating-custom-help-content-that-is-derived-from-existing-microsoft-content"></a>既存の Microsoft コンテンツから派生するカスタム ヘルプ コンテンツの作成

Microsoft ヘルプ コンテンツは、ソリューションを説明するコンテンツのベースラインとして使用できます。 [HtmlFromRepoGenerator](custom-help-toolkit-HtmlFromRepoGenerator.md) ツールは、Microsoft リポジトリ内のマークダウン ファイルからコンテンツを取得してHTML ファイルに変換します。

ソリューションを説明するコンテンツのベースラインとして既存の Microsoft コンテンツを使用する方法の詳細については、[ヘルプでの拡張、カスタマイズ、および共同作業](contributor-guide.md) を参照してください。

## <a name="migrating-content-from-existing-ax-2012-help-content"></a>既存の AX 2012 ヘルプ コンテンツからのコンテンツの移行

AX 2012 の既存のコンテンツがある場合は、Finance、Supply Chain Management、および Commerce に再利用できます。 ただし、カスタム ヘルプ環境で使用できるように HTML ファイルを変換する必要があります。 [カスタム ヘルプ ツールキット](custom-help-toolkit.md) には、AX 2012 の HTML ファイルを変換してカスタム ヘルプ環境で使用できるようにする Windows PowerShell スクリプト **run_ax2012.ps1** が含まれています。

## <a name="creating-new-help-content"></a>新しいヘルプ コンテンツの作成

[カスタム ヘルプ ツールキット](custom-help-toolkit.md) の一部として提供されている [AzureSearchCustomHelp](walkthrough-help-azure.md) ソリューションを使用して、コンテンツを **ヘルプ** ウィンドウに接続します。 **ヘルプ** ウィンドウは、検索サービスのインデックスに対して実行されるクエリを生成します。 **AzureSearchCustomHelp** ソリューションの状況依存ヘルプと全文検索では、各トピックに特定のメタデータが含まれる必要があります。

### <a name="metadata-requirements-for-custom-help-topics"></a><a name="metadata"></a>カスタム ヘルプ トピックのメタデータ要件

[AzureSearchCustomHelp](walkthrough-help-azure.md) ソリューションで結果を返すには、状況依存ヘルプと全文検索用のトピックに次のメタデータが存在する必要があります。

| プロパティ | 説明 |
|----------|-------------|
| タイトル | この値は、**ヘルプ** ウィンドウからの全文検索に使用されます。 |
| 説明 | この値は、**ヘルプ** ウィンドウからの全文検索に使用されます。 |
| ms.search.form | この値には、ページのアプリケーション オブジェクト ツリー (AOT) の名が含まれ、**ヘルプ** ウィンドウからの状況依存検索に使用されます。 |
| ms.locale | 値は、トピックの言語を示します。 **ヘルプ** ウィンドウがコンテンツを検索するときに、現在のブラウザー ロケールに対してマップされます。 ターゲットのカスタム ヘルプ Web サイトに対して、言語のフォールバックを設定できます。 詳細については、[製品およびヘルプの言語およびロケール記述子](language-locale.md) を参照してください。 |
| ms.search.scope | 値は、ヘルプ トピックが表示されるクライアントを決定します。 1 つ以上の値を指定できます。 値には 、**Core**、**Operations**、**Retail**、および **Human Resources** が含まれます。 |

次の表では、**ms.search.scope** プロパティに指定できる値について説明しています。 1 つ以上の値を指定できます。 値は、ヘルプ トピックが表示されるクライアントを決定します。

| 先頭値 | 説明 |
|-------|-------------|
| 基本 | この値が存在する場合、トピックは **ヘルプ** ウィンドウに表示されます。 それ以外の場合、トピックは **ヘルプ** ウィンドウに表示されません。 この値は、サポートされているすべての Dynamics 365 ソリューションのすべてのユーザーに対して、常に **ヘルプ** ウィンドウで使用可能でなければならない Microsoft コンテンツの一部に設定されます。 |
| 運用 | この値は、Finance または Supply Chain Management に基づくソリューションに適用されます。 |
| Retail | この値は、Commerce に基づくソリューションに適用されます。 |
| Human Resources | この値は、Dynamics 365 Human Resources に基づくソリューションに適用されます。 |
| 人材 | この値は、Dynamics 365 Talent に基づくソリューションに適用されます。 (Dynamics 365 Talent: Attract と Dynamics 365 Talent: Onboard アプリは廃止されます。 詳細については、[Dynamics 365 Talent: Attract およびオンボード アプリの廃止](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-nboard-apps) を参照してください。) |

### <a name="non-required-metadata"></a>不要なメタデータ

次のプロパティは、将来の使用のために予約されています。

- **ms.search.region** – 最終的には、このプロパティを使用して、グローバルまたは実装の地域のいずれかのタグが付けられたコンテンツに表示されるコンテンツを制限できます。
- **ms.search.validFrom** – 最終的には、このプロパティを使用して、特定の日付以前にリリースされた製品のコンテンツに対して表示されるコンテンツを制限できます。
- **ms.dyn365.ops.version** – 最終的には、このプロパティを使用して、特定のバージョン以前の製品のコンテンツに対して表示されるコンテンツを制限できます。
- **ms.search.industry** – 最終的には、このプロパティを使用して、特定の業種のコンテンツに表示されるコンテンツを制限できます。

> [!TIP]
> GitHub の公開リポジトリの Microsoft コンテンツには、ヘルプ システムのしくみに関連しない内部プロセスで Microsoft が使用する追加のメタデータが含まれています。 Microsoft コンテンツを拡張またはカスタマイズする場合、これらのメタデータ プロパティを無視できます。

## <a name="changing-the-locale-of-topics-to-match-the-locale-of-solutions"></a>ソリューションのロケールに合わせてトピックのロケールを変更する

ソリューションが複数の市場をサポートすることを目的としている場合は、各市場のヘルプ コンテンツを用意する必要があります。 たとえば、ソリューションがドイツ語 (ドイツ) とドイツ語 (オーストリア) をサポートしているが、ドイツ語 (ドイツ) 専用の HTML ファイルがあるとします。 同じコンテンツをドイツ語 (オーストリア) で使用できるようにするには、HTML ファイルのコピーを作成した後、[HtmlLocaleChanger](custom-help-toolkit-HtmlLocaleChanger.md) ツールを使用して、**ms.locale** メタデータを更新します。 必要に応じて、これらの新しい HTML ファイルにオーストリア固有のコンテンツを追加することもできます。

## <a name="converting-html-files-to-json-files-for-use-with-an-azure-search-service"></a>Azure 検索サービスで使用するために HTML ファイルを JSON ファイルに変換する

[カスタム ヘルプ ツールキット](custom-help-toolkit.md) の一部として提供されている [AzureSearchCustomHelp](walkthrough-help-azure.md) ソリューションを使用する場合、検索サービスでは、すべてのコンテンツを JavaScript Object Notation (JSON) 形式にする必要があります。 [ConvertHtmlToJson](custom-help-toolkit-ConvertHtmlToJson.md) ツールは、HTML ファイルを JSON ファイルに変換します。

## <a name="see-also"></a>参照

[カスタム ヘルプの概要](custom-help-overview.md)  
[カスタム ヘルプ ツールキット](custom-help-toolkit.md)  
[製品およびヘルプの言語およびロケール記述子](language-locale.md)  
[Finance and Operations アプリのヘルプ エクスペリエンスのコンフィギュレーション](../../fin-ops/get-started/help-connect.md)  
[ヘルプ システム](../../fin-ops/get-started/help-overview.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
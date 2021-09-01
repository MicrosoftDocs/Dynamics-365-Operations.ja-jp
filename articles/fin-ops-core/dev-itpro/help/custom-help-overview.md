---
title: カスタム ヘルプの概要
description: このトピックでは、ソリューションを反映するために Microsoft ヘルプ システムを拡張し、コンテンツを [ヘルプ] ウィンドウに接続する方法について説明します。
author: edupont04
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: 75ed04a18ee444e1174eb5c3e034dc130ede208cf51c248f590a8adcca0df644
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763464"
---
# <a name="custom-help-overview"></a>カスタム ヘルプの概要

[!include [banner](../includes/banner.md)]

Finance and Operationsアプリは、多くの場合、組織のニーズに合わせてカスタマイズおよび拡張されます。 ソリューションが Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、または Dynamics 365 Commerce に基づいている場合、ソリューション固有および顧客固有のヘルプ コンテンツを Finance and Operations クライアントの [ヘルプ ウィンドウ](../../fin-ops/get-started/help-overview.md#in-product-help) に接続できます。 このトピックでは、主要な手順と決定ポイントについて説明します。

> [!NOTE]
> Finance and Operations アプリのユーザーは、カスタム タスク ガイドを作成して、ソリューションの機能を説明する概念コンテンツを補うことができます。 これらの概念的な説明は、ヘルプとも呼ばれ、Microsoft、パートナー、および組織自体が提供できます。 詳細については、[ヘルプ システム](../../fin-ops/get-started/help-overview.md) を参照してください。

次の図およびこのトピック一般では、*ヘルプ* という用語を使用して、ハウツー ガイドを含めるか除外するかを概念的に説明します。 *タスク ガイド* という用語は、製品内のタスク ガイドを指します。

![カスタマイズされたヘルプ ソリューションと [ヘルプ] ウィンドウです。](../../fin-ops/get-started/media/help-architecture.png)

## <a name="custom-help-content"></a>カスタム ヘルプ コンテンツ

通常、カスタム ヘルプ コンテンツは、次の 3 つのソースのいずれかから生成されます。

- Microsoft ドキュメント リポジトリ

    カスタム ヘルプ ツールキットの [HTMLFromRepoGenerator](custom-help-toolkit-HtmlFromRepoGenerator.md) ツールを使用して、任意の Finance and Operations リポジトリからコンテンツを複製し、対応する HTML ファイルを生成できます。 これらのファイルは、ソリューションに固有のコンテンツで更新できます。

- 既存のカスタマイズされた Dynamics AX コンテンツ

    [Dynamics AX カスタム ヘルプ コンテンツを変換して、Dynamics 365 で使用できるようにする](migrate-dynamicsax2012.md) ことができます。

- ソリューションに対して特別に作成された HTML ファイル

    [メタデータの詳細](preparing-content.md#metadata) は、状況依存ヘルプと検索が正しく機能するために HTML ファイルに追加する必要があります。

## <a name="process"></a>処理

エンドツーエンド プロセスは、実際の顧客ソリューションとユーザーの期待によって異なります。 標準的なプロセスには、次の手順が含まれます:

1. カスタム ヘルプ コンテンツを作成します。
2. コンテンツを Web サイト に公開します。
3. 検索サービスを使用してコンテンツにインデックスを付けます。
4. カスタム **ヘルプ** ウィンドウを Web サイト と検索サービスに接続します。

Microsoft は、Microsoft Help リポジトリから HTML ファイルを生成し、検索サービス用の JavaScript Object Notation (JSON) ファイルを生成して、HTML ファイルのロケールを変更し、ソリューションのロケールに一致するようにする [ツールキット](custom-help-toolkit.md) を提供します。

ページ下部のリンクからこのドキュメントに寄稿するか、[Dynamics 365 コミュニティ](https://community.dynamics.com/) に参加して、知識を共有してください。

次の表は、ヘルプ エクスペリエンスを構成するために管理者が通常持つ主な目的の概要を示します。

| 目標 | 詳細情報 |
|-----------|------------|
| 実際のソリューションを反映した、カスタマイズされた製品内ヘルプ エクスペリエンスをユーザーに提供したい。 | このトピックの [カスタム ヘルプ Web サイト](#custom-help-sites) セクションと、[タスク レコーダーを使用したドキュメントやトレーニングの作成](../user-interface/task-recorder-training-docs.md) を参照してください。 |
| Microsoft Help コンテンツをソリューションに固有の Help コンテンツのベースラインとして使用したい。 | [カスタム ヘルプ ツールキット: HtmlFromRepoGenerator ツール](custom-help-toolkit-HtmlFromRepoGenerator.md) を参照してください。 |
| Microsoft Help コンテンツに寄稿したい。 | [ヘルプの拡張、カスタマイズ、および共同作業](contributor-guide.md) を参照してください。 |
| 既存の Dynamics AX コンテンツを再利用したい。 | [Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換](migrate-dynamicsax2012.md) を参照してください。 |
| ヘルプ コンテンツの Web サイト を設定したい。 | このトピックの [カスタム ヘルプ Web サイト](#custom-help-sites) セクションを参照してください。 |
| コンテンツを **ヘルプ** ウィンドウに追加したい。 | [カスタム ヘルプ Web サイトを ヘルプ ウィンドウに接続する](connect-help-pane.md) を参照してください。 |
| テクニカル ライターは、以前のコンテンツを Markdown に変換して、Microsoft コンテンツをカスタマイズしやすくするためのガイダンスを必要としています。 | [Markdown への移行](migrate-dynamicsax2012.md#moving-to-markdown) を参照してください。 |

## <a name="custom-help-websites"></a><a name="custom-help-sites"></a>カスタム ヘルプ Web サイト

製品がヘルプ コンテンツに接続する前に、製品内の **ヘルプ** ウィンドウをカスタマイズして、コンテンツが表示されるようにする必要があります。 次の条件を満たす必要があります:

- コンテンツは Web サイト で入手可能である必要があります。

    コンテンツを既存の Web サイト に展開するか、コンテンツをホストする専用の Web サイト を設定できます。 Web サイトは非公開でも公開でもかまいませんが、ユーザーがコンテンツにアクセスするためサインインする必要は **ない** ことをお勧めします。

- コンテンツには、検索サービスでインデックス付けされる必要があります。

    状況依存ヘルプの [カスタム ヘルプ ツールキット](custom-help-toolkit.md) の一部である [AzureSearchCustomHelp](walkthrough-help-azure.md) ソリューションを使用する場合、**ヘルプ** ウィンドウは、検索サービスのインデックスに対して実行する必要があるクエリを生成します。 クエリは、ヘルプ トピックの特定のメタデータに依存します。 詳細については、[カスタム ヘルプ トピックのメタデータ要件](preparing-content.md#metadata) を参照してください。

[Azure にカスタム ヘルプを展開](walkthrough-help-azure.md) トピックでは、Azure でコンテンツをホストするためのアプローチについて説明します。 製品内の **ヘルプ** ウィンドウで検索できるように、コンテンツにインデックス付けする検索サービスの設定方法に関する情報が含まれています。 [Azure サブスクリプション](/azure/guides/developer/azure-developer-guide#understanding-accounts-subscriptions-and-billing) をお持ちでない場合は、始める前にアカウントを作成してください。 12 か月間は無料のアカウントで開始できます。 詳細については、[今すぐ Azure 無料アカウントを作成する](https://azure.microsoft.com/free/) を参照してください。

## <a name="see-also"></a>参照

[カスタム ヘルプ Web サイトを [ヘルプ] ウィンドウに接続する](connect-help-pane.md)  
[Azure にカスタム ヘルプを展開](walkthrough-help-azure.md)  
[カスタム ヘルプ ツールキット](custom-help-toolkit.md)  
[製品およびヘルプの言語およびロケール記述子](language-locale.md)  
[Finance and Operations アプリのヘルプ エクスペリエンスのコンフィギュレーション](../../fin-ops/get-started/help-connect.md)  
[ヘルプ システム](../../fin-ops/get-started/help-overview.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
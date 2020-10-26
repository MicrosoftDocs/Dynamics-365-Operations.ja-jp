---
title: Dynamics 365 Translation Service 概要
description: このトピックでは、Microsoft Dynamics 365 Translation Service (DTS) について説明します。 DTS はパートナーおよび ISV がソリューションの翻訳またはサポートされている Microsoft Dynamics 製品に新しい言語を追加するときにエクスペリエンスを向上するために設計されています。
author: ejcho
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 6154
ms.assetid: ejchoGIT
ms.search.region: Global
ms.author: ejcho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2bf8ea3e4f8f9a2045d53383345065ddc0dc3a9
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979076"
---
# <a name="dynamics-365-translation-service-overview"></a>Dynamics 365 Translation Service 概要

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Translation Service (DTS) は、Microsoft Dynamics Lifecycle Services (LCS) にホストされています。 パートナーおよび独立系ソフトウェア ベンダー (ISV) がソリューションの翻訳または[サポートされている Dynamics 製品](./translation-service-overview.md#supported-products)に新しい言語を追加するときにエクスペリエンスを向上するために設計されています。

DTS は、翻訳出力の品質を最大限に高めるために [Microsoft 一般提供 (GA) 言語](./translation-service-overview.md#glossary) のカスタム トレーニングを受けた機械翻訳 (MT) システムを使用します。 DTS は、Microsoft Dynamics およびパートナー/ISV の言語資産からの翻訳リサイクルもサポートしています。 したがって、同一の文字列は一度変換され、一貫して再利用されます。

次の図は、サービスが、高レベルで、どのように機能するかを示しています。

![DTS のしくみ](./media/dts-overview.png "DTS のしくみ")

## <a name="recycling-existing-translations"></a>既存の翻訳をリサイクル
既存の言語資産は、ローカライズ交換ファイル形式 (XLIFF) を使用する翻訳メモリ (TM) ファイルを含む zip ファイルに資産がアップロードされた場合にのみ再利用できます。 詳細については、[翻訳メモリ ファイル](./use-translation-service-tm.md) を参照してください。

## <a name="custom-trained-mt-system"></a>カスタム トレーニングされた MT システム
DTSは Microsoft Translator サービスとカスタム トランスレーターを使用して、Microsoft Dynamics 製品向けに Microsoft Translator の高度なニューラル機械翻訳をカスタマイズします。 カスタム トレーニングを受けた MT システムは、パートナーが 10,000 を超える翻訳単位 (TU) を含む XLIFF TM ファイルをアップロードしない限り、GA 言語でのみ使用できます。 (TU には、通常、ソース文字列、翻訳、状態、状態識別子、およびメモが含まれています。) そのような場合、DTS は、XLIFF TM ファイルが提出される翻訳要求に固有のカスタムトレーニング MT システムを作成します。

> [!NOTE]
> Microsoft Translator は Microsoft Translator テキスト API を介したテキスト翻訳をサポートしています。 [Microsoft Translator Hub](https://www.microsoft.com/translator/business/hub/) の廃止により、V2 も 2019 年 4 月 30 日に廃止されます。そのため DTS は V3 Translator API を使用します。 V3 のサポート言語についての詳細は [Translator テキスト API の言語と地域のサポート](https://docs.microsoft.com/azure/cognitive-services/translator/language-support#customization) を参照してください。 

## <a name="supported-products"></a>サポートされている製品
DTS では、現在次の製品バージョンがサポートされています。

| 製品名 | バージョン | ユーザー インターフェイス ファイルのサポートされている形式 | ドキュメント ファイルのサポートされている形式 | 摘要 |
|--------------|----------|-------------------------------------------|------------------------------------------|-------|
| Microsoft Dynamics AX 2012 | すべてのバージョン | .ktd、.ald | .docx | |
| Dynamics 365 Finance and Operations アプリ | すべてのバージョン | .label.txt | .docx、.html | .txt は固有のラベル形式で、.html はカスタム ヘルプ ソリューションの形式です。 |
| Microsoft Dynamics 365 Commerce | すべてのバージョン | .label.txt | .docx | |
| Microsoft Dynamics CRM | すべてのバージョン | .resx | .docx | |
| Microsoft Dynamics NAV | すべてのバージョン | .etx、.stx、.resx、.txt、.xml、.xlf | .docx | .txt と .xml は NAV 固有の形式で、.xlf は Business Central の拡張リソース形式です。 |

## <a name="accessing-dts"></a>DTS へのアクセス
LCS の次の 2 つの場所で DTS にアクセスすることができます。

- LCS のホーム ページから
- LCS プロジェクト内から

### <a name="accessing-dts-from-the-lcs-home-page"></a>LCS のホーム ページから DTS へのアクセス
LCS にログインし、ページの右側にスクロールします。 タイル ワッフルを展開し、**翻訳サービス**タイルを選択して DTS のダッシュボード ビューを開きます。

### <a name="accessing-dts-from-within-an-lcs-project"></a>LCS プロジェクト内から DTS へのアクセス
新しいプロジェクトを作成するか、既存のプロジェクトを開きます。 プロジェクト ダッシュ ボードの、**追加ツール**セクションで、**翻訳サービス**タイルを選択します。 または、プロジェクト ダッシュ ボードで、**メニュー**ボタンを選択し、その後**翻訳サービス**を選択します。

### <a name="accessing-dts-from-the-lcs-home-page-vs-accessing-it-from-within-an-lcs-project"></a>LCS プロジェクト内からアクセス対 LCS ホーム ページから DTS へのアクセス
LCS のホーム ページから DTS にアクセスして、翻訳要求を作成するとき、その要求に使用される製品を選択できます。 異なる製品を使用するリクエストを追加するには、製品を選択するだけで変更できます。 サービスを閉じて、さまざまな翻訳プロジェクトを開く必要はありません。

このオプションは、複数の製品翻訳プロジェクトで作業する場合に便利です。 ただし、LCS プロジェクトの範囲外のサービスにアクセスするため、他のユーザーは DTS ダッシュ ボードで要求を表示できません。 代わりに、このオプションには、すべてのプロジェクト内および LCS ホーム ページから行った翻訳の要求をすべて表示する独自の DTS ダッシュボードがあります。

次の図は、LCS のホームページから開いた DTS ダッシュボードの例を示しています。

![LCS のホーム ページから開いた DTS ダッシュ ボード](./media/dts-home-dashboard.png "LCS のホーム ページから開いた DTS ダッシュ ボード")

LCS プロジェクトは常に製品に関連付けられているため、プロジェクトから送信する翻訳要求にはプロジェクトの製品タイプとバージョン情報が自動的に含まれます。 要求では異なる製品を選択することはできません。

LCS プロジェクトでは、プロジェクト所有者とユーザーに、DTS ダッシュボードおよびプロジェクト内の送信された翻訳要求にアクセスするアクセス許可があります。 したがって、このオプションは、LCS の 1 つの製品翻訳プロジェクトで複数の人と作業する場合に便利です。

次の図は、LCS プロジェクト内から開いた DTS ダッシュボードの例を示しています。

![プロジェクト内から開いた DTS ダッシュ ボード](./media/dts-project-dashboard.png "プロジェクト内から開いた DTS ダッシュ ボード")

## <a name="accessing-lcs-preview-features"></a>LCS プレビュー機能へのアクセス
LCS はさまざまな理由から一部のサービスや機能をプレビュー機能としてのみ提供します。 利用可能なプレビュー機能の一覧を表示するには、LCS ホームページで **プレビュー機能の管理** タイルを選択します。 機能を有効にするには、機能を選択して、**プレビュー機能を有効にする** オプションを **はい** に設定します。

DTS には 2 つのプレビュー機能があります。

+ **Dynamics 365 Translation Service - ドキュメント翻訳サポート** - 製品またはソリューションのドキュメント (たとえば、Microsoft Word 文書など) を翻訳する場合は、この機能を有効にする必要があります。
+ **NAV 製品使用可能性** – NAV 製品の LCS プロジェクトを作成し、プロジェクト内から DTS にアクセスするには、この機能を有効にする必要があります。

## <a name="glossary"></a>用語集

| 相談 | 説明 |
|------|-------------|
| XLIFF | XML ローカライズ交換ファイル形式。 XLIFF は XML ベース形式です。 これは、ローカライズ プロセス中にツール間でローカライズ可能なデータが渡される方法を標準化し、コンピューター支援翻訳 (CAT) ツールで使用されるファイルの一般的な形式として機能するために作成されました。 |
| Microsoft GA 言語 | Microsoft が生成した言語の一般的な可用性。 一覧は、製品によって異なります。 |
| TU | 単位の変換です。 TU には通常、ソース文字列、翻訳、状態、状態識別子、およびメモが含まれています。 |


DTSの使用方法の詳細については、[ユーザー インタ フェース ファイルの翻訳](use-translation-service.md)と[ドキュメント ファイルの翻訳](use-translation-service-ua.md)を参照してください。


---
title: 拡張機能を使用してアプリ スイート レポートをカスタマイズする
description: このトピックでは、App スイート レポートをカスタマイズするための一連のシナリオについて説明します。
author: RichdiMSFT
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: 266614
ms.assetid: acf73781-08bb-4f59-9956-8f9f295ddd02
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: a025cee65dd34e7ee3be9b48898df17d9a861c89
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755460"
---
# <a name="customize-app-suite-reports-by-using-extensions"></a><span data-ttu-id="228bc-103">拡張機能を使用してアプリ スイート レポートをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="228bc-103">Customize App Suite reports by using extensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="228bc-104">このトピックでは、App スイート レポートをカスタマイズするための一連のシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="228bc-104">This topic discusses a series of scenarios for customizing App Suite reports.</span></span>

<span data-ttu-id="228bc-105">Finance and Operations は、カスタム ソリューションをサポートするためのツールの拡張セットを提供します。</span><span class="sxs-lookup"><span data-stu-id="228bc-105">Finance and Operations offers an expanded set of tools to support custom solutions.</span></span> <span data-ttu-id="228bc-106">標準アプリケーションのレポート ソリューションのカスタマイズは、純粋な拡張モデルを使用して完全にサポートをされています。</span><span class="sxs-lookup"><span data-stu-id="228bc-106">Customizations to reporting solutions in the standard application are fully supported using a pure extension model.</span></span> <span data-ttu-id="228bc-107">このトピックには、アプリケーション スイート コンポーネントをオーバーレイすることなく、標準のアプリケーション レポートに最も一般的なカスタマイズを追加する方法についてのガイダンスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="228bc-107">This topic contains guidance about how to add the most common customizations to standard application reports without overlayering Application Suite artifacts.</span></span> <span data-ttu-id="228bc-108">アプリケーションをカスタマイズするときの、拡張ベースのアプローチを使用する主な利点を次に示します。</span><span class="sxs-lookup"><span data-stu-id="228bc-108">Here are some of the key benefits of using an extension-based approach when customizing the application:</span></span>

- <span data-ttu-id="228bc-109">コードの重複を最小化して、アプリケーション ソリューションのフットプリントを低減します。</span><span class="sxs-lookup"><span data-stu-id="228bc-109">It reduces the footprint of your application solutions by minimizing code duplication.</span></span>
- <span data-ttu-id="228bc-110">カスタムレポートには、レポート データ プロバイダー (RDP)、データ コントラクト、および UI ビルダー クラスのビジネス ロジックの更新などの標準ソリューションの拡張機能があります。</span><span class="sxs-lookup"><span data-stu-id="228bc-110">Custom reports benefit from enhancements made to standard solutions including updates to business logic in Report Data Provider (RDP), data contracts, and UI Builder classes.</span></span>
- <span data-ttu-id="228bc-111">標準アプリケーション ソリューションは影響を受けず、カスタム レポートと同時に引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="228bc-111">Standard application solutions are unaffected and continue to be available in concert with custom reports.</span></span>

<span data-ttu-id="228bc-112">レポート拡張機能は、標準アプリケーション レポートを中断またはアクセス禁止しません。</span><span class="sxs-lookup"><span data-stu-id="228bc-112">Report extensions do not break or prevent access to standard application reports.</span></span> <span data-ttu-id="228bc-113">代わりに、プラットフォームは、ユーザー セッションのコンテキストに基づいて適切なレポート デザインを選択できるターゲット レポートの実行時の選択をサポートします。</span><span class="sxs-lookup"><span data-stu-id="228bc-113">Instead, the platform supports run-time selection of the target report allowing you to choose the appropriate report design based on the context of the user session.</span></span> <span data-ttu-id="228bc-114">拡張機能を使用したカスタマイズに関する詳細については、 [拡張機能およびオーバーレイによるカスタマイズ](../extensibility/customization-overlayering-extensions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="228bc-114">For more information about customizations using extensions, see [Customize through extension and overlayering](../extensibility/customization-overlayering-extensions.md)</span></span>

## <a name="scenarios"></a><span data-ttu-id="228bc-115">シナリオ</span><span class="sxs-lookup"><span data-stu-id="228bc-115">Scenarios</span></span>
<span data-ttu-id="228bc-116">使用可能な柔軟性を実証する 4 つの重要なシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="228bc-116">There are four key scenarios which demonstrate the flexibility available.</span></span> <span data-ttu-id="228bc-117">最初の 2 つのシナリオには、カスタム レポート ソリューションのために既存の RDP クラスの拡張が含まれます。</span><span class="sxs-lookup"><span data-stu-id="228bc-117">The first two scenarios involve extending existing RDP classes for custom reporting solutions.</span></span>

- <span data-ttu-id="228bc-118">[アプリケーション スイート レポート の データセットを拡張する](expand-app-suite-report-data-sets.md) – テーブル拡張機能を使用し、カスタム ビジネス ロジックを統合して既存のデータセットにユーザー定義の列を追加します。</span><span class="sxs-lookup"><span data-stu-id="228bc-118">[Expand Application Suite report data sets](expand-app-suite-report-data-sets.md) – Use table extensions and integrate custom business logic to add custom columns to an existing dataset.</span></span>
- <span data-ttu-id="228bc-119">カスタム データセットの作成 – 既存の RDP クラスを拡張してカスタム データセットを返すことによって、アプリケーション レポートにデータを追加します。</span><span class="sxs-lookup"><span data-stu-id="228bc-119">Composing custom datasets – Add more data to application reports by extending an existing RDP class to return a custom dataset.</span></span>

<span data-ttu-id="228bc-120">その他の 2 つのシナリオでは拡張機能を使用して、カスタム ソリューションにアプリケーション ナビゲーションをリダイレクトする方法に関する情報を提供できます。</span><span class="sxs-lookup"><span data-stu-id="228bc-120">The other two scenarios offer insights on how to use extensions to redirect application navigations to your custom solutions.</span></span>

- <span data-ttu-id="228bc-121">[レポート メニュー項目を拡張してユーザー ナビゲーション に リダイレクトする](extend-report-menu-items.md)– アプリケーションのメニュー項目をカスタマイズして、カスタム レポート デザインへの参照をリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="228bc-121">[Extend report menu items to redirect user navigation](extend-report-menu-items.md) – Customize application menu items to redirect references to a custom report design.</span></span>
- <span data-ttu-id="228bc-122">[ビジネス ドキュメントのユーザー定義のデザインを作成する](custom-designs-business-docs.md) – 委任ハンドラーを使用すると、既存の印刷の管理ドキュメント インスタンスに ユーザー定義 レポート デザインを追加できます。</span><span class="sxs-lookup"><span data-stu-id="228bc-122">[Create custom designs for business documents](custom-designs-business-docs.md) – Delegate handlers allow you to add custom report designs to an existing Print Management document instance.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
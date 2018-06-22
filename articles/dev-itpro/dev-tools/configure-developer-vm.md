---
title: "1 ボックス開発環境のコンフィギュレーション"
description: "この記事では、ワンボックス開発環境の推奨構成について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 23361
ms.assetid: 09dbb06c-dbc7-468d-a78e-e89a97a59fe6
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 72504bbb5b33b7edf1a8e1260eacc60f2c76b9f4
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="configure-a-one-box-development-environment"></a><span data-ttu-id="dc997-103">1 ボックス開発環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="dc997-103">Configure a one-box development environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc997-104">この記事では、ワンボックス開発環境の推奨構成について説明します。</span><span class="sxs-lookup"><span data-stu-id="dc997-104">This article describes recommended configurations of your one-box developer environment.</span></span>

<a name="setup"></a><span data-ttu-id="dc997-105">段取り</span><span class="sxs-lookup"><span data-stu-id="dc997-105">Setup</span></span>
-----

1. <span data-ttu-id="dc997-106">Visual Studio を起動し、ツール バーで <strong>Dynamics 365 **&gt; **オプション</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc997-106">Start Visual Studio, and on the toolbar, click <strong>Dynamics 365 **&gt; **Options</strong>.</span></span>
2. <span data-ttu-id="dc997-107">**Microsoft Dynamics** ノードを展開し、**プロジェクト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc997-107">Expand the **Microsoft Dynamics** node, and then click **Projects**.</span></span>
3. <span data-ttu-id="dc997-108"><strong>要素タイプ別のプロジェクトを整理する</strong> チェック ボックスが選択されていることを確認し、[*<strong><em>OK</em></strong>*] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc997-108">Verify that the <strong>Organize projects by element type</strong> check box is selected, and click *<strong><em>OK.</em></strong>*</span></span>
4. <span data-ttu-id="dc997-109">コード エディターで行番号を表示するには、**ツール**&gt;**オプション**&gt;**テキスト** **エディター**&gt;**すべての言語** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc997-109">To view the line numbers in your code editor, select **Tools** &gt; **Options** &gt; **Text** **Editor** &gt; **All Languages**.</span></span>
5. <span data-ttu-id="dc997-110">**行番号** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="dc997-110">Select the **Line numbers** check box.</span></span>



## <a name="debugging"></a><span data-ttu-id="dc997-111">デバッグ</span><span class="sxs-lookup"><span data-stu-id="dc997-111">Debugging</span></span>
<span data-ttu-id="dc997-112">より良い X++ デバッガーのパフォーマンスについては、IntelliTrace をオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="dc997-112">For better performance of the X++ debugger, you might want to turn off IntelliTrace.</span></span> <span data-ttu-id="dc997-113">IntelliTrace はアプリケーションの完全な実行履歴を収集します。</span><span class="sxs-lookup"><span data-stu-id="dc997-113">IntelliTrace collects the complete execution history of an application.</span></span> <span data-ttu-id="dc997-114">アプリケーション スイートのような大規模なパッケージをデバッグする場合、X++ デバッグをサポートしておらず、IDE でパフォーマンスの問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="dc997-114">It is not supported for X++ debugging and causes performance issues in the IDE when debugging large packages like Application Suite.</span></span> <span data-ttu-id="dc997-115">Intellitrace をオフにするには、**オプション**&gt;**IntelliTrace**&gt;**IntelliTrace を有効にする** をクリックしてチェック ボックスをオフにし、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dc997-115">To turn off Intellitrace, click **Options** &gt; **IntelliTrace** &gt; **Enable IntelliTrace**, clear the check box, and then click **OK**.</span></span> <span data-ttu-id="dc997-116">Intellitrace は Visual Studio 2015 の Enterprise 版でのみ使用できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="dc997-116">Note that Intellitrace is only available in the Enterprise version of Visual Studio 2015.</span></span>    





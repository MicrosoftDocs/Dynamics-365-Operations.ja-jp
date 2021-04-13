---
title: 1 ボックス開発環境の構成
description: この記事では、ワンボックス開発環境の推奨構成について説明します。
author: RobinARH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 23361
ms.assetid: 09dbb06c-dbc7-468d-a78e-e89a97a59fe6
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7fa40f8f48196815ca4cbce379a21041a4677ee
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750360"
---
# <a name="configure-one-box-development-environments"></a><span data-ttu-id="450d8-103">1 ボックス開発環境の構成</span><span class="sxs-lookup"><span data-stu-id="450d8-103">Configure one-box development environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="450d8-104">この記事では、ワンボックス開発環境の推奨構成について説明します。</span><span class="sxs-lookup"><span data-stu-id="450d8-104">This article describes recommended configurations of your one-box developer environment.</span></span>

<a name="setup"></a><span data-ttu-id="450d8-105">セットアップ</span><span class="sxs-lookup"><span data-stu-id="450d8-105">Setup</span></span>
-----

1. <span data-ttu-id="450d8-106">Visual Studio を起動し、ツール バーで <strong>Dynamics 365 **&gt;**オプション</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="450d8-106">Start Visual Studio, and on the toolbar, click <strong>Dynamics 365 \*\*&gt; \*\*Options</strong>.</span></span>
2. <span data-ttu-id="450d8-107">**Microsoft Dynamics** ノードを展開し、**プロジェクト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="450d8-107">Expand the **Microsoft Dynamics** node, and then click **Projects**.</span></span>
3. <span data-ttu-id="450d8-108"><strong>要素タイプ別のプロジェクトを整理する</strong> チェック ボックスが選択されていることを確認し、*<strong><em>OK</em></strong>* をクリックします。</span><span class="sxs-lookup"><span data-stu-id="450d8-108">Verify that the <strong>Organize projects by element type</strong> check box is selected, and click *<strong><em>OK.</em></strong>*</span></span>
4. <span data-ttu-id="450d8-109">コード エディターで行番号を表示するには、**ツール**&gt;**オプション**&gt;**テキスト** **エディター**&gt;**すべての言語** を選択します。</span><span class="sxs-lookup"><span data-stu-id="450d8-109">To view the line numbers in your code editor, select **Tools** &gt; **Options** &gt; **Text** **Editor** &gt; **All Languages**.</span></span>
5. <span data-ttu-id="450d8-110">**行番号** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="450d8-110">Select the **Line numbers** check box.</span></span>



## <a name="debugging"></a><span data-ttu-id="450d8-111">デバッグ</span><span class="sxs-lookup"><span data-stu-id="450d8-111">Debugging</span></span>
<span data-ttu-id="450d8-112">より良い X++ デバッガーのパフォーマンスについては、IntelliTrace をオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="450d8-112">For better performance of the X++ debugger, you might want to turn off IntelliTrace.</span></span> <span data-ttu-id="450d8-113">IntelliTrace はアプリケーションの完全な実行履歴を収集します。</span><span class="sxs-lookup"><span data-stu-id="450d8-113">IntelliTrace collects the complete execution history of an application.</span></span> <span data-ttu-id="450d8-114">アプリケーション スイートのような大規模なパッケージをデバッグする場合、X++ デバッグをサポートしておらず、IDE でパフォーマンスの問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="450d8-114">It is not supported for X++ debugging and causes performance issues in the IDE when debugging large packages like Application Suite.</span></span> <span data-ttu-id="450d8-115">Intellitrace をオフにするには、**オプション**&gt;**IntelliTrace**&gt;**IntelliTrace を有効にする** をクリックしてチェック ボックスをオフにし、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="450d8-115">To turn off Intellitrace, click **Options** &gt; **IntelliTrace** &gt; **Enable IntelliTrace**, clear the check box, and then click **OK**.</span></span> <span data-ttu-id="450d8-116">Intellitrace は Visual Studio の Enterprise 版でのみ使用できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="450d8-116">Note that Intellitrace is only available in the Enterprise version of Visual Studio.</span></span>    





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
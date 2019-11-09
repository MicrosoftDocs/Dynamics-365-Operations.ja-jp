---
title: 1 ボックス開発環境の構成
description: この記事では、ワンボックス開発環境の推奨構成について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 23361
ms.assetid: 09dbb06c-dbc7-468d-a78e-e89a97a59fe6
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f584e0444b60cdf7dbd01a4b2f0ca16bb00b210
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191701"
---
# <a name="configure-one-box-development-environments"></a><span data-ttu-id="3963d-103">1 ボックス開発環境の構成</span><span class="sxs-lookup"><span data-stu-id="3963d-103">Configure one-box development environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3963d-104">この記事では、ワンボックス開発環境の推奨構成について説明します。</span><span class="sxs-lookup"><span data-stu-id="3963d-104">This article describes recommended configurations of your one-box developer environment.</span></span>

<a name="setup"></a><span data-ttu-id="3963d-105">セットアップ</span><span class="sxs-lookup"><span data-stu-id="3963d-105">Setup</span></span>
-----

1. <span data-ttu-id="3963d-106">Visual Studio を起動し、ツール バーで <strong>Dynamics 365 **&gt;**オプション</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3963d-106">Start Visual Studio, and on the toolbar, click <strong>Dynamics 365 \*\*&gt; \*\*Options</strong>.</span></span>
2. <span data-ttu-id="3963d-107">**Microsoft Dynamics** ノードを展開し、**プロジェクト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3963d-107">Expand the **Microsoft Dynamics** node, and then click **Projects**.</span></span>
3. <span data-ttu-id="3963d-108"><strong>要素タイプ別のプロジェクトを整理する</strong> チェック ボックスが選択されていることを確認し、*<strong><em>OK</em></strong>* をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3963d-108">Verify that the <strong>Organize projects by element type</strong> check box is selected, and click *<strong><em>OK.</em></strong>*</span></span>
4. <span data-ttu-id="3963d-109">コード エディターで行番号を表示するには、**ツール**&gt;**オプション**&gt;**テキスト** **エディター**&gt;**すべての言語** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3963d-109">To view the line numbers in your code editor, select **Tools** &gt; **Options** &gt; **Text** **Editor** &gt; **All Languages**.</span></span>
5. <span data-ttu-id="3963d-110">**行番号** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="3963d-110">Select the **Line numbers** check box.</span></span>



## <a name="debugging"></a><span data-ttu-id="3963d-111">デバッグ</span><span class="sxs-lookup"><span data-stu-id="3963d-111">Debugging</span></span>
<span data-ttu-id="3963d-112">より良い X++ デバッガーのパフォーマンスについては、IntelliTrace をオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="3963d-112">For better performance of the X++ debugger, you might want to turn off IntelliTrace.</span></span> <span data-ttu-id="3963d-113">IntelliTrace はアプリケーションの完全な実行履歴を収集します。</span><span class="sxs-lookup"><span data-stu-id="3963d-113">IntelliTrace collects the complete execution history of an application.</span></span> <span data-ttu-id="3963d-114">アプリケーション スイートのような大規模なパッケージをデバッグする場合、X++ デバッグをサポートしておらず、IDE でパフォーマンスの問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="3963d-114">It is not supported for X++ debugging and causes performance issues in the IDE when debugging large packages like Application Suite.</span></span> <span data-ttu-id="3963d-115">Intellitrace をオフにするには、**オプション**&gt;**IntelliTrace**&gt;**IntelliTrace を有効にする** をクリックしてチェック ボックスをオフにし、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3963d-115">To turn off Intellitrace, click **Options** &gt; **IntelliTrace** &gt; **Enable IntelliTrace**, clear the check box, and then click **OK**.</span></span> <span data-ttu-id="3963d-116">Intellitrace は Visual Studio 2015 の Enterprise 版でのみ使用できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3963d-116">Note that Intellitrace is only available in the Enterprise version of Visual Studio 2015.</span></span>    



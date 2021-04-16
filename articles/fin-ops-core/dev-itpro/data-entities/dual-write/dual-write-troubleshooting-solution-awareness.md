---
title: ソリューションの認識に関する問題のトラブルシューティング
description: このトピックでは、 ソリューションの認識に関する問題の修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 86dd8803f7560ea337f2452e9722fe0151466daf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748876"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="90c35-103">ソリューションの認識に関する問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="90c35-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="90c35-104">このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="90c35-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="90c35-105">このトピックでは、 ソリューションの認識に関する問題の修正に役立つトラブルシューティングに特化した情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="90c35-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90c35-106">このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="90c35-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="90c35-107">各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。</span><span class="sxs-lookup"><span data-stu-id="90c35-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="90c35-108">デュアル書き込みのページでエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="90c35-108">Error on the Dual-write page</span></span>

<span data-ttu-id="90c35-109">**デュアル書き込み** ページでは、次のようなエラーメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="90c35-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="90c35-110">*MetadataCache で 'msdyn\_dualwriteentitymap' with namemapping='Logical という名称のエンティティが見つかりませんでした。*</span><span class="sxs-lookup"><span data-stu-id="90c35-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="90c35-111">この問題を修正するには、Dataverse にデュアル書き込みのコアソ リューションがインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="90c35-111">To fix the issue, make sure that the dual-write core solution is installed in Dataverse.</span></span> <span data-ttu-id="90c35-112">デュアル書き込みのコア ソリューションは、ソリューションを認識するにあたって必須となります。</span><span class="sxs-lookup"><span data-stu-id="90c35-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
---
title: "セキュリティ開発ツールのユーザー ガイド"
description: "このトピックでは、セキュリティ開発ツールを使用して、ロール、職務、権限などのセキュリティ アーティファクトを作成および管理する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18451
ms.assetid: fc61e23f-f20d-4149-800a-3614d13828a6
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b86108616f3c7705dfdf637abcafc60517421bb7
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="security-development-tool-user-guide"></a><span data-ttu-id="3e9a7-103">セキュリティ開発ツールのユーザー ガイド</span><span class="sxs-lookup"><span data-stu-id="3e9a7-103">Security Development Tool user guide</span></span>

[!include [banner](../../includes/banner.md)]

| <span data-ttu-id="3e9a7-104">**メモ**</span><span class="sxs-lookup"><span data-stu-id="3e9a7-104">**Note**</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9a7-105">これは、予備的なプレリリース ドキュメントで、予告なしに変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="3e9a7-105">This is pre-release documentation of a preliminary nature and is subject to change at any time without notice.</span></span> <span data-ttu-id="3e9a7-106">ここで提供されている情報の正確さは保障されていません。</span><span class="sxs-lookup"><span data-stu-id="3e9a7-106">Microsoft cannot guarantee the accuracy of any information provided herein.</span></span> |

<span data-ttu-id="3e9a7-107">Microsoft Dynamics AX 2012 のセキュリティ開発ツールは、ロール、職務、および特権などのセキュリティ コンポーネントを簡単に管理および維持できるようにすることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="3e9a7-107">The Security Development Tool for Microsoft Dynamics AX 2012 is intended to help you more easily create and maintain security artifacts such as roles, duties, and privileges.</span></span> <span data-ttu-id="3e9a7-108">このツールは、特定の役割、義務、権限に対するエントリポイントのアクセス許可を表示します。</span><span class="sxs-lookup"><span data-stu-id="3e9a7-108">The tool displays entry point permissions for a given role, duty, or privilege.</span></span> <span data-ttu-id="3e9a7-109">追加のツールは、エントリ ポイント用のアクセス レベルの更新を使用して説明します。</span><span class="sxs-lookup"><span data-stu-id="3e9a7-109">Additional tools guide you through updates of the access levels for entry points.</span></span> <span data-ttu-id="3e9a7-110">また、異なるテスト ユーザー アカウントを使用せずに、新規作成または修正したセキュリティ ロール、職務権限、または権限を同じインターフェイスからテストするために、ツールを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="3e9a7-110">You can also use the tool to test a newly created or modified security role, duty, or privilege from the same interface, without using a different test user account.</span></span> <span data-ttu-id="3e9a7-111">また、このツールを使用して業務プロセス フローを記録し、使用されるエントリ ポイントを識別することができます。</span><span class="sxs-lookup"><span data-stu-id="3e9a7-111">Additionally, you can use the tool to record business process flows and identify the entry points that are used.</span></span> <span data-ttu-id="3e9a7-112">セキュリティ開発ツールが移動されました。</span><span class="sxs-lookup"><span data-stu-id="3e9a7-112">The Security Development Tool has moved.</span></span> <span data-ttu-id="3e9a7-113">Microsoft Dynamics Lifecycle Services のダウンロード可能なツール セクションから利用できます。</span><span class="sxs-lookup"><span data-stu-id="3e9a7-113">It is now available from the Downloadable tools section of Microsoft Dynamics Lifecycle Services.</span></span> <span data-ttu-id="3e9a7-114">[Lifecycle Services に移動](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="3e9a7-114">[Go to Lifecycle Services](https://lcs.dynamics.com).</span></span>



<a name="additional-resources"></a><span data-ttu-id="3e9a7-115">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="3e9a7-115">Additional resources</span></span>
--------

[<span data-ttu-id="3e9a7-116">セキュリティ開発ツール ユーザー インターフェイス (AX 2012) の概要</span><span class="sxs-lookup"><span data-stu-id="3e9a7-116">Overview of the Security Development Tool user interface (AX 2012)</span></span>](overview-security-development-tool-user-interface.md)

[<span data-ttu-id="3e9a7-117">セキュリティ開発ツール (AX 2012) をインストールする</span><span class="sxs-lookup"><span data-stu-id="3e9a7-117">Install the Security Development Tool (AX 2012)</span></span>](install-security-development-tool.md)

[<span data-ttu-id="3e9a7-118">エントリ ポイントのアクセス許可を定義または編集する (AX 2012)</span><span class="sxs-lookup"><span data-stu-id="3e9a7-118">Define or edit entry point permissions (AX 2012)</span></span>](define-edit-entry-point-permissions.md)

[<span data-ttu-id="3e9a7-119">Microsoft Dynamics AX エンタープライズ ポータルでのエントリ ポイントの記録</span><span class="sxs-lookup"><span data-stu-id="3e9a7-119">Record entry points in Microsoft Dynamics AX Enterprise Portal</span></span>](record-entry-points-enterprise-portal.md)





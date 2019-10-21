---
title: モバイル ワークスペースのセキュリティを強化する
description: このトピックでは、ワークスペースへのユーザー アクセスを制限する方法について説明します。
author: makhabaz
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: a388b6aa954f1588c63bf7be83a249270bcf2407
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191821"
---
# <a name="help-secure-mobile-workspaces"></a><span data-ttu-id="d4a52-103">モバイル ワークスペースのセキュリティを強化する</span><span class="sxs-lookup"><span data-stu-id="d4a52-103">Help secure mobile workspaces</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="d4a52-104">このトピックでは、ワークスペースへのユーザー アクセスを制限する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d4a52-104">This topic describes how to limit a user's access to a workspace.</span></span>

## <a name="assign-a-menu-item-to-workspace"></a><span data-ttu-id="d4a52-105">メニュー項目をワークスペースに割り当てる</span><span class="sxs-lookup"><span data-stu-id="d4a52-105">Assign a menu item to workspace</span></span>
<span data-ttu-id="d4a52-106">ワークスペースはメニュー項目に関係させることができます。</span><span class="sxs-lookup"><span data-stu-id="d4a52-106">Workspaces can be tied to a menu item.</span></span> <span data-ttu-id="d4a52-107">ワークスペースはメニュー項目への権限を持つユーザーにのみ表示されるため、メニュー項目へのアクセス権がないユーザーは、ワークスペースを使用できません。</span><span class="sxs-lookup"><span data-stu-id="d4a52-107">Users who don't have access to the menu item can't use the workspace, because the workspace is shown only to users who have rights to the menu item.</span></span>

<span data-ttu-id="d4a52-108">メニュー項目がワークスペースに割り当てられていない場合、ワークスペースは常にユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d4a52-108">If a menu item isn't assigned to a workspace, the workspace is always shown to the user.</span></span>

<span data-ttu-id="d4a52-109">メニュー項目を割り当てることによってワークスペースのセキュリティを確保するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d4a52-109">Follow these steps to help secure your workspaces by assigning a menu item.</span></span>

1. <span data-ttu-id="d4a52-110">**SysAppWorkspaceSecurityAttribute** 属性をワークスペース クラスに追加して、ワークスペースに割り当てるメニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4a52-110">Add a **SysAppWorkspaceSecurityAttribute** attribute to the workspace class, and specify the menu item to assign to the workspace.</span></span>

    ![メニュー項目をワークスペースに割り当てます](media/workspace-api/SecureWorkspaceOption1.png)

2. <span data-ttu-id="d4a52-112">メニュー項目とワークスペースを構築します。</span><span class="sxs-lookup"><span data-stu-id="d4a52-112">Build the menu item and workspace.</span></span> <span data-ttu-id="d4a52-113">変更をテストするには、メニュー項目にアクセスできないユーザー アカウントを使用してモバイル アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="d4a52-113">To test your changes, sign in to mobile app by using a user account that does’nt have access to the menu item.</span></span>

## <a name="override-the-workspacehidden-method"></a><span data-ttu-id="d4a52-114">WorkspaceHidden メソッドのオーバーライド</span><span class="sxs-lookup"><span data-stu-id="d4a52-114">Override the workspaceHidden method</span></span>
<span data-ttu-id="d4a52-115">パラメーターに基づき、ワークスペースを非表示または表示するか指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="d4a52-115">You can also specify whether the workspace is hidden or shown, based on parameters.</span></span> <span data-ttu-id="d4a52-116">**workspaceHidden** メソッドを上書きすることにより、次のコード例に示すように、コードでワークスペースの可視性を制御できます。</span><span class="sxs-lookup"><span data-stu-id="d4a52-116">By overriding the **workspaceHidden** method, you enable your code to control the visibility of the workspace, as shown in the following code example.</span></span>

![WorkspaceHidden メソッドのオーバーライド](media/workspace-api/SecureWorkspaceOption2.png)

## <a name="add-a-menu-item-and-override-the-workspacehidden-method"></a><span data-ttu-id="d4a52-118">メニュー項目を追加して、workspaceHidden メソッドを上書きする</span><span class="sxs-lookup"><span data-stu-id="d4a52-118">Add a menu item and override the workspaceHidden method</span></span>
<span data-ttu-id="d4a52-119">アプリで両方の先行メソッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d4a52-119">You can use both the preceding methods in your app.</span></span> <span data-ttu-id="d4a52-120">メニュー項目はセキュリティ チェックを提供し、**workspaceHidden** メソッドには、ワークスペースの可視性に関連する追加ロジックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d4a52-120">The menu item provides a security check, and the **workspaceHidden** method contains additional logic that is related to the visibility of the workspace.</span></span>

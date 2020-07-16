---
title: AssemblyDeployManager クラス
description: このトピックでは、AssemblyDeployManager クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d14751886e3ec17c02eec898927743bdcac281a7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502724"
---
# <a name="class-assemblydeploymanager"></a><span data-ttu-id="84cf9-103">クラス AssemblyDeployManager</span><span class="sxs-lookup"><span data-stu-id="84cf9-103">Class AssemblyDeployManager</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class AssemblyDeployManager extends Object
```

<span data-ttu-id="84cf9-104">AssemblyDeployManager クラスを使用すると、.NET 呼び出し時に X++ ランタイムによって使用できる AOS VSAssemblies フォルダーに、AOT Visual Studio プロジェクトに格納されているアセンブリを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="84cf9-104">The AssemblyDeployManager class lets you deploy the assemblies that are stored in the AOT Visual Studio Projects to the AOS VSAssemblies folder that can be used by the X++ runtime during .NET calls.</span></span>

## <a name="remarks"></a><span data-ttu-id="84cf9-105">備考</span><span class="sxs-lookup"><span data-stu-id="84cf9-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="84cf9-106">例</span><span class="sxs-lookup"><span data-stu-id="84cf9-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="84cf9-107">方法</span><span class="sxs-lookup"><span data-stu-id="84cf9-107">Methods</span></span>

| <span data-ttu-id="84cf9-108">方法</span><span class="sxs-lookup"><span data-stu-id="84cf9-108">Method</span></span>                                                        | <span data-ttu-id="84cf9-109">説明</span><span class="sxs-lookup"><span data-stu-id="84cf9-109">Description</span></span>                                                                                             |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84cf9-110">::public static boolean isHotswappingEnabled()</span><span class="sxs-lookup"><span data-stu-id="84cf9-110">::public static boolean isHotswappingEnabled()</span></span>                | <span data-ttu-id="84cf9-111">ホット スワップが有効かどうかを示すブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="84cf9-111">Returns a Boolean value that indicates whether hot swapping is enabled.</span></span>                                 |
| <span data-ttu-id="84cf9-112">::public static void deployAssemblyFromPath(str assemblyPath)</span><span class="sxs-lookup"><span data-stu-id="84cf9-112">::public static void deployAssemblyFromPath(str assemblyPath)</span></span> |                                                                                                         |
| <span data-ttu-id="84cf9-113">::public static void removeAssemblyFromPath(str assemblyPath)</span><span class="sxs-lookup"><span data-stu-id="84cf9-113">::public static void removeAssemblyFromPath(str assemblyPath)</span></span> | <span data-ttu-id="84cf9-114">サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーから削除します。</span><span class="sxs-lookup"><span data-stu-id="84cf9-114">Removes one specific assembly that is marked for deployment to the server from the VSAssemblies folder.</span></span> |
| <span data-ttu-id="84cf9-115">::public static void deployAssemblies()</span><span class="sxs-lookup"><span data-stu-id="84cf9-115">::public static void deployAssemblies()</span></span>                       | <span data-ttu-id="84cf9-116">サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーに展開します。</span><span class="sxs-lookup"><span data-stu-id="84cf9-116">Deploys one specific assembly that is marked for deployment to server to the VSAssemblies folder.</span></span>       |

## <a name="method-ishotswappingenabled"></a><span data-ttu-id="84cf9-117">メソッド isHotswappingEnabled</span><span class="sxs-lookup"><span data-stu-id="84cf9-117">Method isHotswappingEnabled</span></span>

<span data-ttu-id="84cf9-118">ホット スワップが有効かどうかを示すブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="84cf9-118">Returns a Boolean value that indicates whether hot swapping is enabled.</span></span>

```xpp
public static boolean isHotswappingEnabled()
```

### <a name="return-value---ishotswappingenabled"></a><span data-ttu-id="84cf9-119">戻り値 - isHotswappingEnabled</span><span class="sxs-lookup"><span data-stu-id="84cf9-119">Return Value - isHotswappingEnabled</span></span>

<span data-ttu-id="84cf9-120">ホット スワップが有効かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="84cf9-120">A Boolean value that indicates whether hot swapping is enabled.</span></span>

## <a name="method-deployassemblyfrompath"></a><span data-ttu-id="84cf9-121">メソッド deployAssemblyFromPath</span><span class="sxs-lookup"><span data-stu-id="84cf9-121">Method deployAssemblyFromPath</span></span>

```xpp
public static void deployAssemblyFromPath(str assemblyPath)
```

### <a name="parameters---deployassemblyfrompath"></a><span data-ttu-id="84cf9-122">パラメーター - deployAssemblyFromPath</span><span class="sxs-lookup"><span data-stu-id="84cf9-122">Parameters - deployAssemblyFromPath</span></span>

<span data-ttu-id="84cf9-123">assemblyPath</span><span class="sxs-lookup"><span data-stu-id="84cf9-123">assemblyPath</span></span>  

## <a name="method-removeassemblyfrompath"></a><span data-ttu-id="84cf9-124">メソッド removeAssemblyFromPath</span><span class="sxs-lookup"><span data-stu-id="84cf9-124">Method removeAssemblyFromPath</span></span>

<span data-ttu-id="84cf9-125">サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーから削除します。</span><span class="sxs-lookup"><span data-stu-id="84cf9-125">Removes one specific assembly that is marked for deployment to the server from the VSAssemblies folder.</span></span>

```xpp
public static void removeAssemblyFromPath(str assemblyPath)
```

### <a name="parameters---removeassemblyfrompath"></a><span data-ttu-id="84cf9-126">パラメーター - removeAssemblyFromPath</span><span class="sxs-lookup"><span data-stu-id="84cf9-126">Parameters - removeAssemblyFromPath</span></span>

<span data-ttu-id="84cf9-127">assemblyPath</span><span class="sxs-lookup"><span data-stu-id="84cf9-127">assemblyPath</span></span>  
<span data-ttu-id="84cf9-128">アセンブリが格納されている Visual Studio プロジェクト パス。</span><span class="sxs-lookup"><span data-stu-id="84cf9-128">The Visual Studio Project path where the assembly is stored.</span></span>

## <a name="method-deployassemblies"></a><span data-ttu-id="84cf9-129">メソッド deployAssemblies</span><span class="sxs-lookup"><span data-stu-id="84cf9-129">Method deployAssemblies</span></span>

<span data-ttu-id="84cf9-130">サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーに展開します。</span><span class="sxs-lookup"><span data-stu-id="84cf9-130">Deploys one specific assembly that is marked for deployment to server to the VSAssemblies folder.</span></span>

```xpp
public static void deployAssemblies()
```


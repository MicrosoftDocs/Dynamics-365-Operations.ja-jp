---
title: SecureNode クラス
description: このトピックでは、SecureNode クラスについて説明します。
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
ms.openlocfilehash: 8b0f2f5afc8b1e892b7814460d19781191304006
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502815"
---
# <a name="class-securenode"></a><span data-ttu-id="69732-103">クラス SecureNode</span><span class="sxs-lookup"><span data-stu-id="69732-103">Class SecureNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SecureNode extends TreeNode
```

<span data-ttu-id="69732-104">SecureNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="69732-104">The SecureNode class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="69732-105">備考</span><span class="sxs-lookup"><span data-stu-id="69732-105">Remarks</span></span>

<span data-ttu-id="69732-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="69732-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="69732-107">例</span><span class="sxs-lookup"><span data-stu-id="69732-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="69732-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="69732-108">Methods</span></span>

| <span data-ttu-id="69732-109">方法</span><span class="sxs-lookup"><span data-stu-id="69732-109">Method</span></span>                                                                          | <span data-ttu-id="69732-110">説明</span><span class="sxs-lookup"><span data-stu-id="69732-110">Description</span></span>                                                             |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="69732-111">public boolean checkAccessRights()</span><span class="sxs-lookup"><span data-stu-id="69732-111">public boolean checkAccessRights()</span></span>                                              |                                                                         |
| <span data-ttu-id="69732-112">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="69732-112">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>        | <span data-ttu-id="69732-113">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="69732-113">Gets or sets the configuration key that is assigned to the control.</span></span>     |
| <span data-ttu-id="69732-114">public ConfigurationKeyId countryConfigurationkey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="69732-114">public ConfigurationKeyId countryConfigurationkey(\[ConfigurationKeyId value\])</span></span> |                                                                         |
| <span data-ttu-id="69732-115">public boolean extendedDataSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="69732-115">public boolean extendedDataSecurity(\[boolean value\])</span></span>                          |                                                                         |
| <span data-ttu-id="69732-116">public boolean isWeb()</span><span class="sxs-lookup"><span data-stu-id="69732-116">public boolean isWeb()</span></span>                                                          |                                                                         |
| <span data-ttu-id="69732-117">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="69732-117">public int neededAccessLevel(\[int value\])</span></span>                                     | <span data-ttu-id="69732-118">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="69732-118">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span> |
| <span data-ttu-id="69732-119">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="69732-119">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                       |                                                                         |
| <span data-ttu-id="69732-120">public ConfigurationKeyId webConfigurationkey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="69732-120">public ConfigurationKeyId webConfigurationkey(\[ConfigurationKeyId value\])</span></span>     |                                                                         |

## <a name="method-checkaccessrights"></a><span data-ttu-id="69732-121">メソッド checkAccessRights</span><span class="sxs-lookup"><span data-stu-id="69732-121">Method checkAccessRights</span></span>

```xpp
public boolean checkAccessRights()
```

### <a name="return-value---checkaccessrights"></a><span data-ttu-id="69732-122">戻り値 - checkAccessRights</span><span class="sxs-lookup"><span data-stu-id="69732-122">Return Value - checkAccessRights</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="69732-123">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="69732-123">Method configurationKey</span></span>

<span data-ttu-id="69732-124">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="69732-124">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="69732-125">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="69732-125">Parameters - configurationKey</span></span>

<span data-ttu-id="69732-126">値</span><span class="sxs-lookup"><span data-stu-id="69732-126">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="69732-127">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="69732-127">Return Value - configurationKey</span></span>

<span data-ttu-id="69732-128">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="69732-128">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="69732-129">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="69732-129">Remarks - configurationKey</span></span>

<span data-ttu-id="69732-130">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="69732-130">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="69732-131">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="69732-131">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-countryconfigurationkey"></a><span data-ttu-id="69732-132">メソッド countryConfigurationkey</span><span class="sxs-lookup"><span data-stu-id="69732-132">Method countryConfigurationkey</span></span>

```xpp
public ConfigurationKeyId countryConfigurationkey([ConfigurationKeyId value])
```

### <a name="parameters---countryconfigurationkey"></a><span data-ttu-id="69732-133">パラメーター - countryConfigurationkey</span><span class="sxs-lookup"><span data-stu-id="69732-133">Parameters - countryConfigurationkey</span></span>

<span data-ttu-id="69732-134">値</span><span class="sxs-lookup"><span data-stu-id="69732-134">value</span></span>  

### <a name="return-value---countryconfigurationkey"></a><span data-ttu-id="69732-135">戻り値 - countryConfigurationkey</span><span class="sxs-lookup"><span data-stu-id="69732-135">Return Value - countryConfigurationkey</span></span>

## <a name="method-extendeddatasecurity"></a><span data-ttu-id="69732-136">メソッド extendedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="69732-136">Method extendedDataSecurity</span></span>

```xpp
public boolean extendedDataSecurity([boolean value])
```

### <a name="parameters---extendeddatasecurity"></a><span data-ttu-id="69732-137">パラメーター - extendedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="69732-137">Parameters - extendedDataSecurity</span></span>

<span data-ttu-id="69732-138">値</span><span class="sxs-lookup"><span data-stu-id="69732-138">value</span></span>  

### <a name="return-value---extendeddatasecurity"></a><span data-ttu-id="69732-139">戻り値 - extendedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="69732-139">Return Value - extendedDataSecurity</span></span>

## <a name="method-isweb"></a><span data-ttu-id="69732-140">メソッド isWeb</span><span class="sxs-lookup"><span data-stu-id="69732-140">Method isWeb</span></span>

```xpp
public boolean isWeb()
```

### <a name="return-value---isweb"></a><span data-ttu-id="69732-141">戻り値 - isWeb</span><span class="sxs-lookup"><span data-stu-id="69732-141">Return Value - isWeb</span></span>

## <a name="method-neededaccesslevel"></a><span data-ttu-id="69732-142">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="69732-142">Method neededAccessLevel</span></span>

<span data-ttu-id="69732-143">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="69732-143">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

```xpp
public int neededAccessLevel([int value])
```

### <a name="parameters---neededaccesslevel"></a><span data-ttu-id="69732-144">パラメーター - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="69732-144">Parameters - neededAccessLevel</span></span>

<span data-ttu-id="69732-145">値</span><span class="sxs-lookup"><span data-stu-id="69732-145">value</span></span>  

### <a name="return-value---neededaccesslevel"></a><span data-ttu-id="69732-146">戻り値 - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="69732-146">Return Value - neededAccessLevel</span></span>

<span data-ttu-id="69732-147">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="69732-147">The current value of the neededAccessLevel property.</span></span>

### <a name="remarks---neededaccesslevel"></a><span data-ttu-id="69732-148">備考 - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="69732-148">Remarks - neededAccessLevel</span></span>

<span data-ttu-id="69732-149">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="69732-149">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="69732-150">AccessType::NoAccess。</span><span class="sxs-lookup"><span data-stu-id="69732-150">AccessType::NoAccess.</span></span>
-   <span data-ttu-id="69732-151">AccessType::View。</span><span class="sxs-lookup"><span data-stu-id="69732-151">AccessType::View.</span></span>
-   <span data-ttu-id="69732-152">AccessType::Edit。</span><span class="sxs-lookup"><span data-stu-id="69732-152">AccessType::Edit.</span></span>
-   <span data-ttu-id="69732-153">AccessType::Add。</span><span class="sxs-lookup"><span data-stu-id="69732-153">AccessType::Add.</span></span>
-   <span data-ttu-id="69732-154">AccessType::Delete。</span><span class="sxs-lookup"><span data-stu-id="69732-154">AccessType::Delete.</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="69732-155">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="69732-155">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="69732-156">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="69732-156">Parameters - securityKey</span></span>

<span data-ttu-id="69732-157">値</span><span class="sxs-lookup"><span data-stu-id="69732-157">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="69732-158">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="69732-158">Return Value - securityKey</span></span>

## <a name="method-webconfigurationkey"></a><span data-ttu-id="69732-159">メソッド webConfigurationkey</span><span class="sxs-lookup"><span data-stu-id="69732-159">Method webConfigurationkey</span></span>

```xpp
public ConfigurationKeyId webConfigurationkey([ConfigurationKeyId value])
```

### <a name="parameters---webconfigurationkey"></a><span data-ttu-id="69732-160">パラメーター - webConfigurationkey</span><span class="sxs-lookup"><span data-stu-id="69732-160">Parameters - webConfigurationkey</span></span>

<span data-ttu-id="69732-161">値</span><span class="sxs-lookup"><span data-stu-id="69732-161">value</span></span>  

### <a name="return-value---webconfigurationkey"></a><span data-ttu-id="69732-162">戻り値 - webConfigurationkey</span><span class="sxs-lookup"><span data-stu-id="69732-162">Return Value - webConfigurationkey</span></span>


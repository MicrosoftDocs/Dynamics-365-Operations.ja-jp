---
title: ConfigurationKeySet クラス
description: このトピックでは、ConfigurationKeySet クラスについて説明します。
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
ms.openlocfilehash: 79c7c5942d3d2990bac8bd726981ea30884ab5b8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502707"
---
# <a name="class-configurationkeyset"></a><span data-ttu-id="f5fcb-103">クラス ConfigurationKeySet</span><span class="sxs-lookup"><span data-stu-id="f5fcb-103">Class ConfigurationKeySet</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ConfigurationKeySet extends Object
```

<span data-ttu-id="f5fcb-104">ConfigurationKeySet クラスでは、コンフィギュレーション キーのツリーを操作できます。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-104">The ConfigurationKeySet class enables working with a tree of configuration keys.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5fcb-105">備考</span><span class="sxs-lookup"><span data-stu-id="f5fcb-105">Remarks</span></span>

<span data-ttu-id="f5fcb-106">新しい ConfigurationKeySet が作成されるとき、コンフィギュレーション キーのツリーが作成されます。この場合、すべてのキーは既定では「有効」に設定されます。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-106">When a new ConfigurationKeySet is created, a tree of configuration keys is created, where all keys are set by default to "enabled".</span></span> <span data-ttu-id="f5fcb-107">cnt メソッドは、すべての設定キーをループしてカウントするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-107">The cnt method is used to loop through all configuration keys and count them.</span></span> <span data-ttu-id="f5fcb-108">cntID メソッドは、設定キーの ID を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-108">The cntID method is used to retrieve the IDs of the configuration keys.</span></span> <span data-ttu-id="f5fcb-109">コンフィギュレーション キーが削除され、キー ID が ID1、ID2、ID5 などである場合、このメソッドはそれらの ID と比較してコンフィギュレーション キーの数を区別します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-109">In situations in which a configuration key has been deleted and the key IDs are ID1, ID2, ID5, and so on, this method will distinguish the number of configuration keys compared to their IDs.</span></span> <span data-ttu-id="f5fcb-110">新しい ConfigurationKeySet が作成されるとき、すべてのコンフィギュレーション キーが有効になります。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-110">When a new ConfigurationKeySet is created, all configuration keys are enabled.</span></span> <span data-ttu-id="f5fcb-111">システムは loadSystemSetup メソッドを呼び出し、構成タイプが格納されている SysConfig テーブルをスキャンします。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-111">The system will then call the loadSystemSetup method, which scans the SysConfig table where the configuration types are stored.</span></span> <span data-ttu-id="f5fcb-112">コンフィギュレーション キーの設定をループし、有効になっているものを識別します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-112">It loops through the configuration key setup and identifies what is enabled.</span></span> <span data-ttu-id="f5fcb-113">次に、有効なメソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-113">Next, the enabled method is called.</span></span> <span data-ttu-id="f5fcb-114">構成キーが無効になるたびに、すべてのサブ構成キーも自動的に無効になります。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-114">Every time a configuration key is disabled, all sub-configuration keys are also automatically disabled.</span></span> <span data-ttu-id="f5fcb-115">トップ ノードが有効でサブノードの 1 つが無効になっている場合、カーネルはトップ ノードが無効になったときに必ずどのコンフィギュレーション キー サブ ノードが以前に無効にされたかを記録します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-115">In a situation in which a top node is enabled and one of the sub-nodes is disabled, the kernel will remember which configuration key sub-nodes were previously disabled whenever a top node is disabled.</span></span>

## <a name="examples"></a><span data-ttu-id="f5fcb-116">例</span><span class="sxs-lookup"><span data-stu-id="f5fcb-116">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f5fcb-117">メソッド</span><span class="sxs-lookup"><span data-stu-id="f5fcb-117">Methods</span></span>

| <span data-ttu-id="f5fcb-118">方法</span><span class="sxs-lookup"><span data-stu-id="f5fcb-118">Method</span></span>                                                                            | <span data-ttu-id="f5fcb-119">説明</span><span class="sxs-lookup"><span data-stu-id="f5fcb-119">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5fcb-120">public int cnt()</span><span class="sxs-lookup"><span data-stu-id="f5fcb-120">public int cnt()</span></span>                                                                  | <span data-ttu-id="f5fcb-121">アプリケーション オブジェクト ツリー (AOT) で定義されているコンフィギュレーション キーの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-121">Retrieves the number of configuration keys that are defined in the Application Object Tree (AOT).</span></span> |
| <span data-ttu-id="f5fcb-122">public ConfigurationKeyId cnt2Id(int cnt)</span><span class="sxs-lookup"><span data-stu-id="f5fcb-122">public ConfigurationKeyId cnt2Id(int cnt)</span></span>                                         | <span data-ttu-id="f5fcb-123">*n* 番目のコンフィギュレーション キーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-123">Retrieves the ID of the *n*th configuration key.</span></span>                                                                        |
| <span data-ttu-id="f5fcb-124">public boolean enabled(ConfigurationKeyId configurationKeyId, \[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="f5fcb-124">public boolean enabled(ConfigurationKeyId configurationKeyId, \[boolean enable\])</span></span> | <span data-ttu-id="f5fcb-125">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-125">Determines whether to enable or disable the object.</span></span>                                                                     |
| <span data-ttu-id="f5fcb-126">public container pack()</span><span class="sxs-lookup"><span data-stu-id="f5fcb-126">public container pack()</span></span>                                                           | <span data-ttu-id="f5fcb-127">ConfigurationKeySet クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-127">Serializes the current instance of the ConfigurationKeySet class.</span></span>                                                       |
| <span data-ttu-id="f5fcb-128">public boolean touchedByUser(ConfigurationKeyId configurationKeyId)</span><span class="sxs-lookup"><span data-stu-id="f5fcb-128">public boolean touchedByUser(ConfigurationKeyId configurationKeyId)</span></span>               |                                                                                                                         |
| <span data-ttu-id="f5fcb-129">public void new(\[container container\])</span><span class="sxs-lookup"><span data-stu-id="f5fcb-129">public void new(\[container container\])</span></span>                                          | <span data-ttu-id="f5fcb-130">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-130">Initializes a new instance of the Object class.</span></span>                                                                         |
| <span data-ttu-id="f5fcb-131">public void loadSystemSetup()</span><span class="sxs-lookup"><span data-stu-id="f5fcb-131">public void loadSystemSetup()</span></span>                                                     |                                                                                                                         |

## <a name="method-cnt"></a><span data-ttu-id="f5fcb-132">メソッド cnt</span><span class="sxs-lookup"><span data-stu-id="f5fcb-132">Method cnt</span></span>

<span data-ttu-id="f5fcb-133">アプリケーション オブジェクト ツリー (AOT) で定義されているコンフィギュレーション キーの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-133">Retrieves the number of configuration keys that are defined in the Application Object Tree (AOT).</span></span>

```xpp
public int cnt()
```

### <a name="return-value---cnt"></a><span data-ttu-id="f5fcb-134">戻り値 -cnt</span><span class="sxs-lookup"><span data-stu-id="f5fcb-134">Return Value - cnt</span></span>

<span data-ttu-id="f5fcb-135">AOT で定義されているコンフィギュレーション キーの数。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-135">The number of configuration keys that are defined in the AOT.</span></span>

## <a name="method-cnt2id"></a><span data-ttu-id="f5fcb-136">メソッド cnt2Id</span><span class="sxs-lookup"><span data-stu-id="f5fcb-136">Method cnt2Id</span></span>

<span data-ttu-id="f5fcb-137">*n* 番目のコンフィギュレーション キーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-137">Retrieves the ID of the *n*th configuration key.</span></span>

```xpp
public ConfigurationKeyId cnt2Id(int cnt)
```

### <a name="parameters---cnt2id"></a><span data-ttu-id="f5fcb-138">パラメーター - cnt2Id</span><span class="sxs-lookup"><span data-stu-id="f5fcb-138">Parameters - cnt2Id</span></span>

<span data-ttu-id="f5fcb-139">cnt</span><span class="sxs-lookup"><span data-stu-id="f5fcb-139">cnt</span></span>  
<span data-ttu-id="f5fcb-140">コンフィギュレーション キーのインデックス。1 とコンフィギュレーション キーの間でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-140">The index of the configuration key, which must be between 1 and the number of configuration keys.</span></span>

### <a name="return-value---cnt2id"></a><span data-ttu-id="f5fcb-141">戻り値 - cnt2Id</span><span class="sxs-lookup"><span data-stu-id="f5fcb-141">Return Value - cnt2Id</span></span>

<span data-ttu-id="f5fcb-142">指定されたコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-142">The ID of the specified configuration key.</span></span>

### <a name="remarks---cnt2id"></a><span data-ttu-id="f5fcb-143">備考 - cnt2Id</span><span class="sxs-lookup"><span data-stu-id="f5fcb-143">Remarks - cnt2Id</span></span>

<span data-ttu-id="f5fcb-144">構成キーの数を調べるには、cnt メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-144">To find the number of configuration keys, use the cnt method.</span></span> <span data-ttu-id="f5fcb-145">一般に、すべての ID が使用されているわけではないため、インデックスおよび ID は異なります。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-145">In general, the index and ID will differ, because not all the IDs are used.</span></span>

### <a name="examples---cnt2id"></a><span data-ttu-id="f5fcb-146">例 - cnt2Id</span><span class="sxs-lookup"><span data-stu-id="f5fcb-146">Examples - cnt2Id</span></span>

```xpp
ConfigurationKeySet configKeySet = new ConfigurationKeySet(); 
DictConfigurationKey dictConfigurationKey; 
int i; 
```

```xpp
configKeySet.loadSystemSetup(); 
for (i=1; i<= configKeySet.cnt(); i++) 
{ 
    setPrefix('Disabled configurationkeys'); 
    if (!configKeySet.enabled( configKeySet.cnt2Id(i) )) 
    { 
        dictConfigurationKey =  
            new DictConfigurationKey(configKeySet.cnt2id(i)); 
        info (dictConfigurationKey.name()); 
    } 
}
```

## <a name="method-enabled"></a><span data-ttu-id="f5fcb-147">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="f5fcb-147">Method enabled</span></span>

<span data-ttu-id="f5fcb-148">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-148">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled(ConfigurationKeyId configurationKeyId, [boolean enable])
```

### <a name="parameters---enabled"></a><span data-ttu-id="f5fcb-149">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="f5fcb-149">Parameters - enabled</span></span>

<span data-ttu-id="f5fcb-150">configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="f5fcb-150">configurationKeyId</span></span>  
<span data-ttu-id="f5fcb-151">構成キーの状態を設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-151">The value to which to set the state of the configuration key; optional.</span></span>

<!-- -->

<span data-ttu-id="f5fcb-152">enable</span><span class="sxs-lookup"><span data-stu-id="f5fcb-152">enable</span></span>  
<span data-ttu-id="f5fcb-153">構成キーの状態を設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-153">The value to which to set the state of the configuration key; optional.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="f5fcb-154">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="f5fcb-154">Return Value - enabled</span></span>

<span data-ttu-id="f5fcb-155">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-155">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="f5fcb-156">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="f5fcb-156">Remarks - enabled</span></span>

<span data-ttu-id="f5fcb-157">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-157">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="f5fcb-158">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-158">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="f5fcb-159">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-159">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

### <a name="examples---enabled"></a><span data-ttu-id="f5fcb-160">例 - enabled</span><span class="sxs-lookup"><span data-stu-id="f5fcb-160">Examples - enabled</span></span>

<span data-ttu-id="f5fcb-161">この例では、ConfigurationKeySet.enabled メソッドの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-161">This example demonstrates the use of the ConfigurationKeySet.enabled method.</span></span>

```xpp
static void testConfigKey(Args _args) 
{ 
    ConfigurationKeySet configKey = new ConfigurationKeySet(); 
```

```xpp
    configKey.loadSystemSetup(); 
```

```xpp
    // Set the enable value to false. 
    configKey.enabled(configurationkeynum(RouteApprove), false); 
    SysDictConfigurationKey::save(configKey.pack()); 
    SysSecurity::reload(true); 
    print isConfigurationkeyEnabled(configurationkeynum(RouteApprove)); 
```

```xpp
    // Set the enable value to true. 
    configKey.enabled(configurationkeynum(RouteApprove), true); 
    //Save the configuration key setup. 
    SysDictConfigurationKey::save(configKey.pack()); 
    SysSecurity::reload(true); 
```

```xpp
    print isConfigurationkeyEnabled(configurationkeynum(RouteApprove)); 
```

```xpp
    pause; 
}
```

## <a name="method-pack"></a><span data-ttu-id="f5fcb-162">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="f5fcb-162">Method pack</span></span>

<span data-ttu-id="f5fcb-163">ConfigurationKeySet クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-163">Serializes the current instance of the ConfigurationKeySet class.</span></span>

```xpp
public container pack()
```

### <a name="return-value---pack"></a><span data-ttu-id="f5fcb-164">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="f5fcb-164">Return Value - pack</span></span>

<span data-ttu-id="f5fcb-165">ConfigurationKeySet クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-165">A container that contains the current instance of the ConfigurationKeySet class.</span></span>

## <a name="method-touchedbyuser"></a><span data-ttu-id="f5fcb-166">メソッド touchedByUser</span><span class="sxs-lookup"><span data-stu-id="f5fcb-166">Method touchedByUser</span></span>

```xpp
public boolean touchedByUser(ConfigurationKeyId configurationKeyId)
```

### <a name="parameters---touchedbyuser"></a><span data-ttu-id="f5fcb-167">パラメーター - touchedByUser</span><span class="sxs-lookup"><span data-stu-id="f5fcb-167">Parameters - touchedByUser</span></span>

<span data-ttu-id="f5fcb-168">configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="f5fcb-168">configurationKeyId</span></span>  

### <a name="return-value---touchedbyuser"></a><span data-ttu-id="f5fcb-169">戻り値 - touchedByUser</span><span class="sxs-lookup"><span data-stu-id="f5fcb-169">Return Value - touchedByUser</span></span>

## <a name="method-new"></a><span data-ttu-id="f5fcb-170">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f5fcb-170">Method new</span></span>

<span data-ttu-id="f5fcb-171">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f5fcb-171">Initializes a new instance of the Object class.</span></span>

```xpp
public void new([container container])
```

### <a name="parameters---new"></a><span data-ttu-id="f5fcb-172">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="f5fcb-172">Parameters - new</span></span>

<span data-ttu-id="f5fcb-173">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f5fcb-173">container</span></span>  

## <a name="method-loadsystemsetup"></a><span data-ttu-id="f5fcb-174">メソッド loadSystemSetup</span><span class="sxs-lookup"><span data-stu-id="f5fcb-174">Method loadSystemSetup</span></span>

```xpp
public void loadSystemSetup()
```


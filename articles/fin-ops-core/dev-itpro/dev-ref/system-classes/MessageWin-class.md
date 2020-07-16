---
title: MessageWin クラス
description: このトピックでは､MessageWin クラスについて説明します。
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
ms.openlocfilehash: 577832717070aee36945c03db716af3dcb121394
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502573"
---
# <a name="class-messagewin"></a><span data-ttu-id="40bf6-103">クラス MessageWin</span><span class="sxs-lookup"><span data-stu-id="40bf6-103">Class MessageWin</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MessageWin extends Object
```

<span data-ttu-id="40bf6-104">MessageWin クラスを使用すると、messageWindow クラスの開発環境にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="40bf6-104">The MessageWin class gives access to the messageWindow class development environment.</span></span>

## <a name="remarks"></a><span data-ttu-id="40bf6-105">備考</span><span class="sxs-lookup"><span data-stu-id="40bf6-105">Remarks</span></span>

<span data-ttu-id="40bf6-106">さらに MessageWin オブジェクトをインスタンス化することができますが、画面上に同一のメッセージ ウィンドウを参照します。</span><span class="sxs-lookup"><span data-stu-id="40bf6-106">Although you can instantiate more MessageWin objects, they will all refer to the same message window on the screen.</span></span>

## <a name="examples"></a><span data-ttu-id="40bf6-107">例</span><span class="sxs-lookup"><span data-stu-id="40bf6-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="40bf6-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="40bf6-108">Methods</span></span>

| <span data-ttu-id="40bf6-109">方法</span><span class="sxs-lookup"><span data-stu-id="40bf6-109">Method</span></span>                        | <span data-ttu-id="40bf6-110">説明</span><span class="sxs-lookup"><span data-stu-id="40bf6-110">Description</span></span>                                           |
|-------------------------------|-------------------------------------------------------|
| <span data-ttu-id="40bf6-111">public void clear()</span><span class="sxs-lookup"><span data-stu-id="40bf6-111">public void clear()</span></span>           | <span data-ttu-id="40bf6-112">メッセージ ウィンドウをクリアします。</span><span class="sxs-lookup"><span data-stu-id="40bf6-112">Clears the message window.</span></span>                            |
| <span data-ttu-id="40bf6-113">public void activate()</span><span class="sxs-lookup"><span data-stu-id="40bf6-113">public void activate()</span></span>        | <span data-ttu-id="40bf6-114">メッセージ ウィンドウを現在のアクティブ ウィンドウにします。</span><span class="sxs-lookup"><span data-stu-id="40bf6-114">Makes the message window the currently active window.</span></span> |
| <span data-ttu-id="40bf6-115">public void addLine(str line)</span><span class="sxs-lookup"><span data-stu-id="40bf6-115">public void addLine(str line)</span></span> | <span data-ttu-id="40bf6-116">行をメッセージ ウィンドウに記述します。</span><span class="sxs-lookup"><span data-stu-id="40bf6-116">Writes a line to the message window.</span></span>                  |

## <a name="method-clear"></a><span data-ttu-id="40bf6-117">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="40bf6-117">Method clear</span></span>

<span data-ttu-id="40bf6-118">メッセージ ウィンドウをクリアします。</span><span class="sxs-lookup"><span data-stu-id="40bf6-118">Clears the message window.</span></span>

```xpp
public void clear()
```

## <a name="method-activate"></a><span data-ttu-id="40bf6-119">メソッド activate</span><span class="sxs-lookup"><span data-stu-id="40bf6-119">Method activate</span></span>

<span data-ttu-id="40bf6-120">メッセージ ウィンドウを現在のアクティブ ウィンドウにします。</span><span class="sxs-lookup"><span data-stu-id="40bf6-120">Makes the message window the currently active window.</span></span>

```xpp
public void activate()
```

### <a name="remarks---activate"></a><span data-ttu-id="40bf6-121">備考 - activate</span><span class="sxs-lookup"><span data-stu-id="40bf6-121">Remarks - activate</span></span>

<span data-ttu-id="40bf6-122">バージョン 2.11 より前に、行が追加されたり内容が消去されるとメッセージ ウィンドウがフォーカスを取得します。</span><span class="sxs-lookup"><span data-stu-id="40bf6-122">Before version 2.11, the message window would get focus when lines were added or contents were cleared.</span></span> <span data-ttu-id="40bf6-123">バージョン 2.11 以降では、開発者は、メッセージ ウィンドウを一番上のウィンドウにするためにこのメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="40bf6-123">Starting in version 2.11, the developer must call this method to make the message window the top window.</span></span>

## <a name="method-addline"></a><span data-ttu-id="40bf6-124">メソッド addLine</span><span class="sxs-lookup"><span data-stu-id="40bf6-124">Method addLine</span></span>

<span data-ttu-id="40bf6-125">行をメッセージ ウィンドウに記述します。</span><span class="sxs-lookup"><span data-stu-id="40bf6-125">Writes a line to the message window.</span></span>

```xpp
public void addLine(str line)
```

### <a name="parameters---addline"></a><span data-ttu-id="40bf6-126">パラメーター - addLine</span><span class="sxs-lookup"><span data-stu-id="40bf6-126">Parameters - addLine</span></span>

<span data-ttu-id="40bf6-127">明細行</span><span class="sxs-lookup"><span data-stu-id="40bf6-127">line</span></span>  
<span data-ttu-id="40bf6-128">メッセージ ウィンドウへの書き込み明細行を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="40bf6-128">A string that contains the line to write to the message window.</span></span>


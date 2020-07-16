---
title: systemSequence クラス
description: このトピックでは、systemSequence クラスについて説明します。
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
ms.openlocfilehash: ef5dddfa74bd867868a98addd0804cac7e65178b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503000"
---
# <a name="class-systemsequence"></a><span data-ttu-id="95ae2-103">クラス systemSequence</span><span class="sxs-lookup"><span data-stu-id="95ae2-103">Class systemSequence</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class systemSequence extends Object
```

<span data-ttu-id="95ae2-104">systemSequence クラスは、システム シーケンス ジェネレータを手動で制御し、すべての SQL テーブルに対して一意の RecIds を提供します。</span><span class="sxs-lookup"><span data-stu-id="95ae2-104">The systemSequence class takes manual control of the system sequence generator and delivers unique RecIds for all SQL tables.</span></span>

## <a name="remarks"></a><span data-ttu-id="95ae2-105">備考</span><span class="sxs-lookup"><span data-stu-id="95ae2-105">Remarks</span></span>

<span data-ttu-id="95ae2-106">SQL テーブルにレコードが挿入されると、各レコードが関連付けられている会社に関係なく、各レコードに一意の RecId が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="95ae2-106">When records are inserted into SQL tables, a unique RecId is assigned to each record�regardless of the company each record is associated with.</span></span> <span data-ttu-id="95ae2-107">このクラスを使用するときは十分に注意してください。データの整合性が失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="95ae2-107">Use extreme caution when you use this class�data integrity could be destroyed.</span></span> <span data-ttu-id="95ae2-108">このクラスは、通常、データのインポートやエクスポート ルーチン、または非常に大きなジョブに使用されます。</span><span class="sxs-lookup"><span data-stu-id="95ae2-108">This class is typically used for data import or export routines, or for very large jobs.</span></span> <span data-ttu-id="95ae2-109">レコード ID は、int64 データ型の値です。</span><span class="sxs-lookup"><span data-stu-id="95ae2-109">The record ID is an int64 data type value.</span></span> <span data-ttu-id="95ae2-110">レコード ID が割り当てられる範囲は、5637144576 から 2 ^ 63 (9223372036854775808) までです。</span><span class="sxs-lookup"><span data-stu-id="95ae2-110">The range in which record IDs are allocated is from 5637144576 to 2^63 (9223372036854775808).</span></span> <span data-ttu-id="95ae2-111">大きい未使用の RecId 範囲が作成された場合、途中で RecId がなくなることがあります。</span><span class="sxs-lookup"><span data-stu-id="95ae2-111">RecIds can be used up prematurely if large, unused ranges of RecIds are created.</span></span> <span data-ttu-id="95ae2-112">使用されている Recid 範囲の間にある未使用の RecId 範囲を再利用するのは、非常に複雑なプロセスです。</span><span class="sxs-lookup"><span data-stu-id="95ae2-112">Reclaiming unused ranges of RecIds that lie between used ranges of RecIds is a very complicated process.</span></span>

## <a name="examples"></a><span data-ttu-id="95ae2-113">例</span><span class="sxs-lookup"><span data-stu-id="95ae2-113">Examples</span></span>

<span data-ttu-id="95ae2-114">次の例では、CustTable テーブルの int64max 値を予約しています。</span><span class="sxs-lookup"><span data-stu-id="95ae2-114">The following example reserves the int64max value for the CustTable table.</span></span>

```xpp
static public void Main(Args _args) 
{ 
    systemSequence seq; 
    seq = new SystemSequence(); 
    if (seq) 
    { 
        // Allocate 20 recordIds for CustTable table. 
        seq.reserveValues(20, tablenum(CustTable)); 
        // Suspend automatic recId allocation. 
        Seq.suspendRecIds(tablenum(CustTable)); 
        // Manually generate recIds in the range allocated. 
        // Remove the recId suspension. 
        Seq.removeRecIdSuspension(); 
      } 
}
```

## <a name="methods"></a><span data-ttu-id="95ae2-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="95ae2-115">Methods</span></span>

| <span data-ttu-id="95ae2-116">方法</span><span class="sxs-lookup"><span data-stu-id="95ae2-116">Method</span></span>                                                             | <span data-ttu-id="95ae2-117">説明</span><span class="sxs-lookup"><span data-stu-id="95ae2-117">Description</span></span>                                                                                                                     |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95ae2-118">public Int64 flushValues(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="95ae2-118">public Int64 flushValues(TableId tableId)</span></span>                          | <span data-ttu-id="95ae2-119">指定されたテーブルのシステム シーケンス キャッシュから予約された recIds をフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="95ae2-119">Flushes the reserved recIds from the System Sequence cache for a given table</span></span>                                                    |
| <span data-ttu-id="95ae2-120">public Int64 reserveTransids(Int64 nReserved, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="95ae2-120">public Int64 reserveTransids(Int64 nReserved, \[TableId tableId\])</span></span> |                                                                                                                                 |
| <span data-ttu-id="95ae2-121">public Int64 reserveValues(Int64 nReserved, TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="95ae2-121">public Int64 reserveValues(Int64 nReserved, TableId tableId)</span></span>       | <span data-ttu-id="95ae2-122">recIds の自動割り当てが中断されている場合に、新しいレコードに割り当てることのできる recIds の範囲を事前割り当てします。</span><span class="sxs-lookup"><span data-stu-id="95ae2-122">Preallocates a range of recIds that can be allocated to new records when the automatic assignment of recIds has been suspended.</span></span> |
| <span data-ttu-id="95ae2-123">public void suspendTransIds(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="95ae2-123">public void suspendTransIds(TableId tableId)</span></span>                       |                                                                                                                                 |
| <span data-ttu-id="95ae2-124">public void suspendRecIds(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="95ae2-124">public void suspendRecIds(TableId tableId)</span></span>                         |                                                                                                                                 |
| <span data-ttu-id="95ae2-125">public void removeRecIdSuspension(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="95ae2-125">public void removeRecIdSuspension(\[TableId tableId\])</span></span>             |                                                                                                                                 |
| <span data-ttu-id="95ae2-126">public void new()</span><span class="sxs-lookup"><span data-stu-id="95ae2-126">public void new()</span></span>                                                  | <span data-ttu-id="95ae2-127">systemSequence クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="95ae2-127">Initializes a new instance of the systemSequence class.</span></span>                                                                         |
| <span data-ttu-id="95ae2-128">public void removeTransIdSuspension(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="95ae2-128">public void removeTransIdSuspension(\[TableId tableId\])</span></span>           |                                                                                                                                 |

## <a name="method-flushvalues"></a><span data-ttu-id="95ae2-129">メソッド flushValues</span><span class="sxs-lookup"><span data-stu-id="95ae2-129">Method flushValues</span></span>

<span data-ttu-id="95ae2-130">指定されたテーブルのシステム シーケンス キャッシュから予約された recIds をフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="95ae2-130">Flushes the reserved recIds from the System Sequence cache for a given table</span></span>

```xpp
public Int64 flushValues(TableId tableId)
```

### <a name="parameters---flushvalues"></a><span data-ttu-id="95ae2-131">パラメーター - flushValues</span><span class="sxs-lookup"><span data-stu-id="95ae2-131">Parameters - flushValues</span></span>

<span data-ttu-id="95ae2-132">tableId</span><span class="sxs-lookup"><span data-stu-id="95ae2-132">tableId</span></span>  

### <a name="return-value---flushvalues"></a><span data-ttu-id="95ae2-133">戻り値 - flushValues</span><span class="sxs-lookup"><span data-stu-id="95ae2-133">Return Value - flushValues</span></span>

<span data-ttu-id="95ae2-134">キャッシュからフラッシュされた recIds の数。</span><span class="sxs-lookup"><span data-stu-id="95ae2-134">The number of recIds flushed from the cache.</span></span>

### <a name="remarks---flushvalues"></a><span data-ttu-id="95ae2-135">備考 - flushValues</span><span class="sxs-lookup"><span data-stu-id="95ae2-135">Remarks - flushValues</span></span>

<span data-ttu-id="95ae2-136">テーブルへのその後挿入によりテーブルの recId が予約され、システム シーケンス キャッシュにはテーブルの recId の予約済み範囲が入力されます。</span><span class="sxs-lookup"><span data-stu-id="95ae2-136">Subsequent inserts on the table reserve the recIds for the table and System Sequence cache is populated with the reserved range of recIds for the table.</span></span>

## <a name="method-reservetransids"></a><span data-ttu-id="95ae2-137">メソッド reserveTransids</span><span class="sxs-lookup"><span data-stu-id="95ae2-137">Method reserveTransids</span></span>

```xpp
public Int64 reserveTransids(Int64 nReserved, [TableId tableId])
```

### <a name="parameters---reservetransids"></a><span data-ttu-id="95ae2-138">パラメーター - reserveTransids</span><span class="sxs-lookup"><span data-stu-id="95ae2-138">Parameters - reserveTransids</span></span>

<span data-ttu-id="95ae2-139">nReserved</span><span class="sxs-lookup"><span data-stu-id="95ae2-139">nReserved</span></span>  

<!-- -->

<span data-ttu-id="95ae2-140">tableId</span><span class="sxs-lookup"><span data-stu-id="95ae2-140">tableId</span></span>  

### <a name="return-value---reservetransids"></a><span data-ttu-id="95ae2-141">戻り値 - reserveTransids</span><span class="sxs-lookup"><span data-stu-id="95ae2-141">Return Value - reserveTransids</span></span>

## <a name="method-reservevalues"></a><span data-ttu-id="95ae2-142">メソッド reserveValues</span><span class="sxs-lookup"><span data-stu-id="95ae2-142">Method reserveValues</span></span>

<span data-ttu-id="95ae2-143">recIds の自動割り当てが中断されている場合に、新しいレコードに割り当てることのできる recIds の範囲を事前割り当てします。</span><span class="sxs-lookup"><span data-stu-id="95ae2-143">Preallocates a range of recIds that can be allocated to new records when the automatic assignment of recIds has been suspended.</span></span>

```xpp
public Int64 reserveValues(Int64 nReserved, TableId tableId)
```

### <a name="parameters---reservevalues"></a><span data-ttu-id="95ae2-144">パラメーター - reserveValues</span><span class="sxs-lookup"><span data-stu-id="95ae2-144">Parameters - reserveValues</span></span>

<span data-ttu-id="95ae2-145">nReserved</span><span class="sxs-lookup"><span data-stu-id="95ae2-145">nReserved</span></span>  

<!-- -->

<span data-ttu-id="95ae2-146">tableId</span><span class="sxs-lookup"><span data-stu-id="95ae2-146">tableId</span></span>  

### <a name="return-value---reservevalues"></a><span data-ttu-id="95ae2-147">戻り値 - reserveValues</span><span class="sxs-lookup"><span data-stu-id="95ae2-147">Return Value - reserveValues</span></span>

<span data-ttu-id="95ae2-148">最初に使用可能な予約済み recId。</span><span class="sxs-lookup"><span data-stu-id="95ae2-148">The first usable reserved recId.</span></span>

### <a name="remarks---reservevalues"></a><span data-ttu-id="95ae2-149">備考 - reserveValues</span><span class="sxs-lookup"><span data-stu-id="95ae2-149">Remarks - reserveValues</span></span>

<span data-ttu-id="95ae2-150">予約した recIds の範囲は、すぐに予約されています。</span><span class="sxs-lookup"><span data-stu-id="95ae2-150">The range of recIds that you reserved are reserved immediately.</span></span>

## <a name="method-suspendtransids"></a><span data-ttu-id="95ae2-151">メソッド suspendTransIds</span><span class="sxs-lookup"><span data-stu-id="95ae2-151">Method suspendTransIds</span></span>

```xpp
public void suspendTransIds(TableId tableId)
```

### <a name="parameters---suspendtransids"></a><span data-ttu-id="95ae2-152">パラメーター - suspendTransIds</span><span class="sxs-lookup"><span data-stu-id="95ae2-152">Parameters - suspendTransIds</span></span>

<span data-ttu-id="95ae2-153">tableId</span><span class="sxs-lookup"><span data-stu-id="95ae2-153">tableId</span></span>  

## <a name="method-suspendrecids"></a><span data-ttu-id="95ae2-154">メソッド suspendRecIds</span><span class="sxs-lookup"><span data-stu-id="95ae2-154">Method suspendRecIds</span></span>

```xpp
public void suspendRecIds(TableId tableId)
```

### <a name="parameters---suspendrecids"></a><span data-ttu-id="95ae2-155">パラメーター - suspendRecIds</span><span class="sxs-lookup"><span data-stu-id="95ae2-155">Parameters - suspendRecIds</span></span>

<span data-ttu-id="95ae2-156">tableId</span><span class="sxs-lookup"><span data-stu-id="95ae2-156">tableId</span></span>  

## <a name="method-removerecidsuspension"></a><span data-ttu-id="95ae2-157">メソッド removeRecIdSuspension</span><span class="sxs-lookup"><span data-stu-id="95ae2-157">Method removeRecIdSuspension</span></span>

```xpp
public void removeRecIdSuspension([TableId tableId])
```

### <a name="parameters---removerecidsuspension"></a><span data-ttu-id="95ae2-158">パラメーター - removeRecIdSuspension</span><span class="sxs-lookup"><span data-stu-id="95ae2-158">Parameters - removeRecIdSuspension</span></span>

<span data-ttu-id="95ae2-159">tableId</span><span class="sxs-lookup"><span data-stu-id="95ae2-159">tableId</span></span>  

## <a name="method-new"></a><span data-ttu-id="95ae2-160">メソッド new</span><span class="sxs-lookup"><span data-stu-id="95ae2-160">Method new</span></span>

<span data-ttu-id="95ae2-161">systemSequence クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="95ae2-161">Initializes a new instance of the systemSequence class.</span></span>

```xpp
public void new()
```

## <a name="method-removetransidsuspension"></a><span data-ttu-id="95ae2-162">メソッド removeTransIdSuspension</span><span class="sxs-lookup"><span data-stu-id="95ae2-162">Method removeTransIdSuspension</span></span>

```xpp
public void removeTransIdSuspension([TableId tableId])
```

### <a name="parameters---removetransidsuspension"></a><span data-ttu-id="95ae2-163">パラメーター - removeTransIdSuspension</span><span class="sxs-lookup"><span data-stu-id="95ae2-163">Parameters - removeTransIdSuspension</span></span>

<span data-ttu-id="95ae2-164">tableId</span><span class="sxs-lookup"><span data-stu-id="95ae2-164">tableId</span></span>  




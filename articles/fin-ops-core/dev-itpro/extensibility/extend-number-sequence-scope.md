---
title: 番号順序スコープの拡張
description: このトピックでは、開発者が番号シーケンスのスコープを拡張する方法について説明します。
author: RobinARH
ms.date: 04/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 10031
ms.assetid: 4be8b7a1-9632-4368-af41-6811cd100a37
ms.search.region: Global
ms.author: lgou
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf6cd0ec64cfaece4bcba733c1f87de403711e24
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749650"
---
# <a name="extend-the-scope-of-number-sequences"></a><span data-ttu-id="f7982-103">番号順序スコープの拡張</span><span class="sxs-lookup"><span data-stu-id="f7982-103">Extend the scope of number sequences</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7982-104">このトピックでは、数値シーケンスのスコープを拡張する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f7982-104">This topic shows you how to extend the number sequence scope.</span></span>

<span data-ttu-id="f7982-105">数字シーケンスの範囲は、数字シーケンスを使用する組織を定義します。</span><span class="sxs-lookup"><span data-stu-id="f7982-105">The scope of a number sequence defines which organization uses the number sequence.</span></span> <span data-ttu-id="f7982-106">範囲は、**共有**、**会社**、**法人**、または **作業単位** のいずれかにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7982-106">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="f7982-107">**会社** と **法人** スコープを会計カレンダー期間と組み合わせて、より具体的な番号順序を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f7982-107">**Company** and **Legal entity** scopes can be combined with fiscal calendar periods to create even more specific number sequences.</span></span> <span data-ttu-id="f7982-108">新しい番号順序の範囲は、拡張機能を通じて追加できます。</span><span class="sxs-lookup"><span data-stu-id="f7982-108">New number sequence scopes can be added through extensions.</span></span>  

<span data-ttu-id="f7982-109">新しいスコープを作成してクライアントに表示させるには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f7982-109">To create a new scope and have it show up in the client, complete the following steps:</span></span>

1. <span data-ttu-id="f7982-110">**NumberSeqParameterType** の列挙型拡張を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-110">Create an enum extension for **NumberSeqParameterType**.</span></span> <span data-ttu-id="f7982-111">拡張機能に、新しいスコープ タイプの新しい列挙値を追加します。</span><span class="sxs-lookup"><span data-stu-id="f7982-111">In the extension, add a new enum value for the new scope type.</span></span> 
2. <span data-ttu-id="f7982-112">**NumberSequenceType** の列挙型拡張を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-112">Create an enum extension for **NumberSequenceType**.</span></span> <span data-ttu-id="f7982-113">新しいスコープ タイプの新しい列挙値を追加します。</span><span class="sxs-lookup"><span data-stu-id="f7982-113">Add a new enum value for the new scope type.</span></span> <span data-ttu-id="f7982-114">**NumberSequenceType** 列挙は、**NumberSequenceTableEntity** および **NumberSequencesReferenceEntity** で使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7982-114">The **NumberSequenceType** enum is used in **NumberSequenceTableEntity** and **NumberSequencesReferenceEntity**.</span></span>
3. <span data-ttu-id="f7982-115">**NumberSequenceScope** テーブル拡張子を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-115">Create a table extension for the **NumberSequenceScope** table.</span></span> <span data-ttu-id="f7982-116">新しいスコープ タイプの新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7982-116">Add a new field for the new scope type.</span></span>
4. <span data-ttu-id="f7982-117">**NumberSeqScope** クラスの拡張クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-117">Create an extension class for **NumberSeqScope** class.</span></span>
   1. <span data-ttu-id="f7982-118">**NumberSeqScope::getValidScopeTypes** メソッドのポスト ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-118">Create a post handler for the **NumberSeqScope::getValidScopeTypes** method.</span></span> <span data-ttu-id="f7982-119">イベント ハンドラー メソッドでは、有効なスコープ タイプのリストに新しいスコープ タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7982-119">In the event handler method, add the new scope type to the valid scope types list.</span></span>
   1. <span data-ttu-id="f7982-120">**onGetFormatSegmentShortName** デリゲートのイベント ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-120">Create an event handler for the **onGetFormatSegmentShortName** delegate.</span></span> <span data-ttu-id="f7982-121">イベント ハンドラーで、新しいスコープ タイプの短縮名を返します。</span><span class="sxs-lookup"><span data-stu-id="f7982-121">In the event handler, return the short name for the new scope type.</span></span>
   1. <span data-ttu-id="f7982-122">**NumberSeqScope::find** メソッドのポスト ハンドラーを作成し、対応する **NumberSeqScope** インスタンスが見つかるように新しいスコープ タイプのロジックを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7982-122">Create a post handler for the **NumberSeqScope::find** method and add logic for the new scope type so the corresponding **NumberSeqScope** instance can be found.</span></span>   
   1. <span data-ttu-id="f7982-123">**NumberSeqScope::getId** メソッドのポスト ハンドラーを作成し、新しいスコープ タイプのロジックを追加すると、**NumberSequenceScope** テーブルに対応するレコードが見つかる (存在しない場合は作成される) ようになります。</span><span class="sxs-lookup"><span data-stu-id="f7982-123">Create a post handler for the **NumberSeqScope::getId** method and add logic for the new scope type, so the corresponding record can be found (or created if it does not exist) in the **NumberSequenceScope** table.</span></span> 
5. <span data-ttu-id="f7982-124">**NumberSequenceScopeFactory** クラスの拡張クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-124">Create an extension class for the **NumberSequenceScopeFactory** class.</span></span> <span data-ttu-id="f7982-125">新しいスコープ タイプを表す新しい **NumberSeqScope** を初期化するメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7982-125">Add a method that initializes the new **NumberSeqScope** that represents the new scope type.</span></span>
6. <span data-ttu-id="f7982-126">**NumberSequenceDetails** フォームのフォーム拡張を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-126">Create a form extension for the **NumberSequenceDetails** form.</span></span> <span data-ttu-id="f7982-127">**スコープ** タブに新しいスコープ タイプを表示するコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7982-127">Add controls that show the new scope type to the **Scope** tab.</span></span>
7. <span data-ttu-id="f7982-128">**NumberSequenceDetails** フォームの拡張クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-128">Create an extension class for the **NumberSequenceDetails** form.</span></span>
   1. <span data-ttu-id="f7982-129">新しいスコープ タイプが **スコープ** ボックスで選択されたときに新しいスコープ タイプを表示するために、**updateScopeControlVisibility** メソッドのポスト ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-129">Create a post handler for the **updateScopeControlVisibility** method to show the new scope type when the new scope type is selected in the **Scope** box.</span></span>
   2. <span data-ttu-id="f7982-130">**updateScopeControlValues** メソッドのポスト ハンドラーを作成して、**スコープ** タブのコントロールの値を更新します。</span><span class="sxs-lookup"><span data-stu-id="f7982-130">Create a post handler for the **updateScopeControlValues** method to update the values of the controls in the **Scope** tab.</span></span>
   3. <span data-ttu-id="f7982-131">新しいスコープ タイプが選択されたときに **NumberSeqScope** インスタンスを初期化するための **createScope** メソッドのポスト ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-131">Create a post handler for the **createScope** method to initialize a **NumberSeqScope** instance when the new scope type is selected.</span></span>
   4. <span data-ttu-id="f7982-132">新しいスコープ タイプの短い名前を返す **getShortNameForParameterType** デリゲートのイベント ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-132">Create an event handler for the **getShortNameForParameterType** delegate to return the short name for the new scope type.</span></span>
8. <span data-ttu-id="f7982-133">**NumberSequenceTableEntity** および **NumberSequencesReferenceEntity** データ エンティティの拡張クラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7982-133">Add an extension class for the **NumberSequenceTableEntity** and **NumberSequencesReferenceEntity** data entities.</span></span> <span data-ttu-id="f7982-134">新しいスコープ タイプの **NumberSequenceScope** を生成するために、**GenerateNumberSequenceScopeTypes** メソッドと **GenerateNumberSequenceScopeValues** メソッドのポスト ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7982-134">Create post handlers for the **GenerateNumberSequenceScopeTypes** and **GenerateNumberSequenceScopeValues** methods to generate the **NumberSequenceScope** for the new scope type.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
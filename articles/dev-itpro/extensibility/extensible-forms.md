---
title: 拡張可能フォームの書き込み
description: このトピックでは、拡張可能フォームを書き込む方法について説明します。
author: smithanataraj
manager: AnnBe
ms.date: 09/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: smithanataraj
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 35a96953c561277a30adc82fa72a8dee95176f31
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833426"
---
# <a name="write-extensible-forms"></a><span data-ttu-id="8b3df-103">拡張可能フォームの書き込み</span><span class="sxs-lookup"><span data-stu-id="8b3df-103">Write extensible forms</span></span>

[!include [banner](../includes/banner.md)]

## <a name="methods-on-forms"></a><span data-ttu-id="8b3df-104">フォーム上のメソッド</span><span class="sxs-lookup"><span data-stu-id="8b3df-104">Methods on forms</span></span>
+ <span data-ttu-id="8b3df-105">一般に、拡張可能なメソッドを記述するためのガイドラインは、フォーム メソッドにも適用されます。</span><span class="sxs-lookup"><span data-stu-id="8b3df-105">In general, the guidelines for writing extensible methods also apply to form methods.</span></span>
+ <span data-ttu-id="8b3df-106">コマンド チェーン (CoC) は、フォームの非プライベート メンバー (クラスの非プライベート メンバーと同じ) にアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="8b3df-106">Chain of Command (CoC) gives access to the form's non-private members, which are the same as the non-private members for classes.</span></span>
+ <span data-ttu-id="8b3df-107">CoC は入れ子になったクラスで有効になります。</span><span class="sxs-lookup"><span data-stu-id="8b3df-107">CoC is enabled for nested classes.</span></span> <span data-ttu-id="8b3df-108">そのため、フォーム上のさまざまなレベルで定義されているメソッドは拡張可能です。</span><span class="sxs-lookup"><span data-stu-id="8b3df-108">Therefore, methods that are defined in various levels on the form are extensible.</span></span>

> [!NOTE]
> <span data-ttu-id="8b3df-109">フォームのメソッドの 1 つの制限として、データ ソース メソッドの場合、カーネルで定義されているメソッドのみで拡張が有効になります。つまり、フォーム データ ソースで定義されたメソッドは拡張可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="8b3df-109">One limitation of methods on forms, that for form data source methods only methods that are defined in the kernel are enabled for extensions, i.e. methods defined on the form data source are not extensible.</span></span> <span data-ttu-id="8b3df-110">これは今後のプラットフォーム更新で使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b3df-110">This will be available in an upcoming Platform Update.</span></span>

## <a name="field-groups"></a><span data-ttu-id="8b3df-111">フィールド グループ</span><span class="sxs-lookup"><span data-stu-id="8b3df-111">Field groups</span></span>
<span data-ttu-id="8b3df-112">可能であれば必ずフィールド グループの使用を検討してください。</span><span class="sxs-lookup"><span data-stu-id="8b3df-112">Consider using field groups whenever possible.</span></span> <span data-ttu-id="8b3df-113">これにより、独立系ソフトウェア ベンダー (ISV) はフィールド グループを拡張するときにそのフィールドを無料で追加できます。</span><span class="sxs-lookup"><span data-stu-id="8b3df-113">In this way, independent software vendors (ISVs) can add their fields for free when they extend a field group.</span></span>

## <a name="form-controls"></a><span data-ttu-id="8b3df-114">フォーム コントロール</span><span class="sxs-lookup"><span data-stu-id="8b3df-114">Form controls</span></span>
<span data-ttu-id="8b3df-115">コントロールが移動により拡張不可になった場合、フォーム コントロールでの移動により中断が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b3df-115">Moving around form controls could potentially cause a break if the controls are made non-extensible by moving.</span></span>

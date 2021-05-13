---
title: 拡張可能フォームの書き込み
description: このトピックでは、拡張可能フォームを書き込む方法について説明します。
author: smithanataraj
ms.date: 09/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 452d29cfa54fa5eb30a71092c00880d167780f9b
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866043"
---
# <a name="write-extensible-forms"></a><span data-ttu-id="b150f-103">拡張可能フォームの書き込み</span><span class="sxs-lookup"><span data-stu-id="b150f-103">Write extensible forms</span></span>

[!include [banner](../includes/banner.md)]

## <a name="methods-on-forms"></a><span data-ttu-id="b150f-104">フォーム上のメソッド</span><span class="sxs-lookup"><span data-stu-id="b150f-104">Methods on forms</span></span>
+ <span data-ttu-id="b150f-105">一般に、拡張可能なメソッドを記述するためのガイドラインは、フォーム メソッドにも適用されます。</span><span class="sxs-lookup"><span data-stu-id="b150f-105">In general, the guidelines for writing extensible methods also apply to form methods.</span></span>
+ <span data-ttu-id="b150f-106">コマンド チェーン (CoC) は、フォームの非プライベート メンバー (クラスの非プライベート メンバーと同じ) にアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="b150f-106">Chain of Command (CoC) gives access to the form's non-private members, which are the same as the non-private members for classes.</span></span>
+ <span data-ttu-id="b150f-107">CoC は入れ子になったクラスで有効になります。</span><span class="sxs-lookup"><span data-stu-id="b150f-107">CoC is enabled for nested classes.</span></span> <span data-ttu-id="b150f-108">そのため、フォーム上のさまざまなレベルで定義されているメソッドは拡張可能です。</span><span class="sxs-lookup"><span data-stu-id="b150f-108">Therefore, methods that are defined in various levels on the form are extensible.</span></span>

> [!NOTE]
> <span data-ttu-id="b150f-109">フォームのメソッドの 1 つの制限として、データ ソース メソッドの場合、カーネルで定義されているメソッドのみで拡張が有効になります。つまり、フォーム データ ソースで定義されたメソッドは拡張可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="b150f-109">One limitation of methods on forms, that for form data source methods only methods that are defined in the kernel are enabled for extensions, i.e. methods defined on the form data source are not extensible.</span></span> <span data-ttu-id="b150f-110">これは今後のプラットフォーム更新で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b150f-110">This will be available in an upcoming Platform Update.</span></span>

## <a name="field-groups"></a><span data-ttu-id="b150f-111">フィールド グループ</span><span class="sxs-lookup"><span data-stu-id="b150f-111">Field groups</span></span>
<span data-ttu-id="b150f-112">可能であれば必ずフィールド グループの使用を検討してください。</span><span class="sxs-lookup"><span data-stu-id="b150f-112">Consider using field groups whenever possible.</span></span> <span data-ttu-id="b150f-113">これにより、独立系ソフトウェア ベンダー (ISV) はフィールド グループを拡張するときにそのフィールドを無料で追加できます。</span><span class="sxs-lookup"><span data-stu-id="b150f-113">In this way, independent software vendors (ISVs) can add their fields for free when they extend a field group.</span></span>

## <a name="form-controls"></a><span data-ttu-id="b150f-114">フォーム コントロール</span><span class="sxs-lookup"><span data-stu-id="b150f-114">Form controls</span></span>
<span data-ttu-id="b150f-115">コントロールが移動により拡張不可になった場合、フォーム コントロールでの移動により中断が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b150f-115">Moving around form controls could potentially cause a break if the controls are made non-extensible by moving.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
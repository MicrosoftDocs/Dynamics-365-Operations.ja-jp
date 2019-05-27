---
title: 最新の更新プログラムに対してコードをコンパイルするための計画と準備
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations から最新の更新プログラムを使用してパートナー コードをコンパイルするときに、開発者が遭遇する可能性のある潜在的な問題を取り上げます。
author: dfroslie
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: ''
ms.service: Dynamics365Operations
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 102343
ms.assetid: e48d7424-371a-49ee-882c-07b7ceb00183
ms.search.region: Global
ms.author: dfroslie
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 67db20afb762258433f63a8d7604658979316468
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537197"
---
# <a name="plan-and-prepare-for-compiling-code-against-the-latest-update"></a><span data-ttu-id="56ee8-103">最新の更新プログラムに対してコードをコンパイルするための計画と準備</span><span class="sxs-lookup"><span data-stu-id="56ee8-103">Plan and prepare for compiling code against the latest update</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56ee8-104">1 つのバージョンのサービス プランの展開では、Microsoft はバイナリおよび機能の観点から下位互換性の確保に努めています。</span><span class="sxs-lookup"><span data-stu-id="56ee8-104">With the rollout of the One Version servicing plan, Microsoft is committed to backward compatibility from a binary and functional perspective.</span></span> <span data-ttu-id="56ee8-105">1 つのバージョンの詳細については、[1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-and-ops/get-started/one-version.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56ee8-105">For detailed information about One Version, see [One Version service updates FAQ](../../fin-and-ops/get-started/one-version.md).</span></span> <span data-ttu-id="56ee8-106">下位互換性が優先事項であっても、開発活動の結果コードの変更が必要になる状況があります。</span><span class="sxs-lookup"><span data-stu-id="56ee8-106">Even with backward compatibility as a priority, there are situations where development activities may result in required code changes.</span></span> <span data-ttu-id="56ee8-107">そのような状況の一部を次に示します。</span><span class="sxs-lookup"><span data-stu-id="56ee8-107">Some of those situations are described below.</span></span> 

- <span data-ttu-id="56ee8-108">Microsoft が列挙を拡張可能にするとき、バイナリと互換性のある変更と見なされます。</span><span class="sxs-lookup"><span data-stu-id="56ee8-108">When Microsoft makes an enumeration extensible, it is considered a binary compatible change.</span></span> <span data-ttu-id="56ee8-109">コンパイラは、非拡張可能列挙の整数値に依存する安全ではない拡張可能列挙操作をチェックします。</span><span class="sxs-lookup"><span data-stu-id="56ee8-109">The compiler checks for unsafe extensible enumeration operations that depend on the integer value of a non-extensible enumeration.</span></span> <span data-ttu-id="56ee8-110">安全ではない拡張可能列挙操作を含むすべてのパートナー コードは、再コンパイル時にコンパイラ エラーとなるため、変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="56ee8-110">Any partner code that contains unsafe extensible enumeration operations will have compiler errors when re-compiled and will need to be modified.</span></span> <span data-ttu-id="56ee8-111">詳細については、[拡張機能による列挙への値の追加](../extensibility/add-enum-value.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56ee8-111">For more information, see [Add values to enums through extension](../extensibility/add-enum-value.md).</span></span>

- <span data-ttu-id="56ee8-112">コンパイル時に生じる可能性のある未解決の参照を避けるため、パートナー モデルは最上位レベルのモジュールと下位のモジュールを参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="56ee8-112">To avoid possible unresolved references when compiling, a partner model should reference the top-level modules and sub-modules.</span></span> <span data-ttu-id="56ee8-113">これを行わないと、参照されていない下位モジュールに新しいリソースを追加する Microsoft の変更により、未解決の参照が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="56ee8-113">If this is not done, a Microsoft change that adds new resources in an unreferenced sub-module may cause an unresolved reference.</span></span> <span data-ttu-id="56ee8-114">コンパイル エラーを解決するには、参照として下位モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="56ee8-114">To resolve the compilation error, add the sub-module as a reference.</span></span>

- <span data-ttu-id="56ee8-115">いくつかのメソッドは、将来完全に非推奨となることを示すため、非推奨属性が設定されます。</span><span class="sxs-lookup"><span data-stu-id="56ee8-115">Some methods will be attributed as obsolete to signal that they will be fully deprecated in the future.</span></span> <span data-ttu-id="56ee8-116">古いメソッドの呼び出しまたはラップのために生成されたコンパイラ警告は、予想されるコード パスがまだ存在することを確認するために調べる必要があります。</span><span class="sxs-lookup"><span data-stu-id="56ee8-116">Any compiler warning that is generated due to the calling or wrapping of an obsolete method should be investigated to ensure that the expected code path still exists.</span></span> <span data-ttu-id="56ee8-117">場合によっては、Microsoft コードが古いメソッドの代わりに新しいメソッドを直接呼び出します。</span><span class="sxs-lookup"><span data-stu-id="56ee8-117">In some cases, Microsoft code will directly call the new method in place of the obsolete method.</span></span> <span data-ttu-id="56ee8-118">この場合、古いメソッドに基づいて構築されたコードは実行されません (予期される場合)。</span><span class="sxs-lookup"><span data-stu-id="56ee8-118">When this happens, the code built around the obsolete method will not execute when expected.</span></span>

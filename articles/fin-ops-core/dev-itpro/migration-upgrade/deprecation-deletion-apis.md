---
title: 方法とメタデータの要素の廃止
description: このトピックでは、コード ベースの拡大に伴って古くなるメソッドよびメタデータ要素の廃止に関する情報が提供されます。
author: jorisdg
manager: AnnBe
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: a713a405b84ad5b7ead5538aa882c7514585107d
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983679"
---
# <a name="deprecation-of-methods-and-metadata-elements"></a><span data-ttu-id="7bef2-103">方法とメタデータの要素の廃止</span><span class="sxs-lookup"><span data-stu-id="7bef2-103">Deprecation of methods and metadata elements</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7bef2-104">Microsoft コード ベースが進歩すると共に、いくつかのメソッドとメタデータ要素が不要になります。</span><span class="sxs-lookup"><span data-stu-id="7bef2-104">As the Microsoft code base continues to evolve, some methods and metadata elements will no longer be required.</span></span> <span data-ttu-id="7bef2-105">Microsoft は、これらの古いメソッドとメタデータ要素を廃止とマークします。</span><span class="sxs-lookup"><span data-stu-id="7bef2-105">Microsoft will mark these obsolete methods and metadata elements for deprecation.</span></span>

- <span data-ttu-id="7bef2-106">メソッドは **SysObsolete** 属性でマークされます。</span><span class="sxs-lookup"><span data-stu-id="7bef2-106">Methods are marked with the **SysObsolete** attribute.</span></span> <span data-ttu-id="7bef2-107">通常、この属性は、代わりの方法を推奨します。</span><span class="sxs-lookup"><span data-stu-id="7bef2-107">Typically, this attribute recommends an alternative to the method.</span></span>
- <span data-ttu-id="7bef2-108">メタデータ要素の場合、**IsObsolete**プロパティが**Yes**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7bef2-108">For metadata elements, the **IsObsolete** property is set to **Yes**.</span></span>

<span data-ttu-id="7bef2-109">廃止は、バイナリとデザイン時の両方と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="7bef2-109">The deprecation is compatible with both binaries and design time.</span></span> <span data-ttu-id="7bef2-110">参照元のコードは引き続き正常に機能し、当座はアクションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="7bef2-110">The referencing code will continue to work as expected, and no immediate action is required.</span></span> <span data-ttu-id="7bef2-111">コンパイル時、非推奨の成果物への参照がコンパイル**警告**として報告されます。</span><span class="sxs-lookup"><span data-stu-id="7bef2-111">During compilation, any references to deprecated artifacts are reported as compile **warnings**.</span></span>

## <a name="cleanup-of-deprecated-elements"></a><span data-ttu-id="7bef2-112">非推奨の要素のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="7bef2-112">Cleanup of deprecated elements</span></span>

<span data-ttu-id="7bef2-113">12 か月の期間後、Microsoft は古いメソッドおよびメタデータ要素を削除する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7bef2-113">After a period of at least 12 months, Microsoft might delete obsolete methods and metadata elements.</span></span>

<span data-ttu-id="7bef2-114">ただし、テレメトリが、古い形式のメソッドやメタデータ要素がまだ使用されていることを示す場合、Microsoft は、消費者の中断リスクを減らすため削除**しません**。</span><span class="sxs-lookup"><span data-stu-id="7bef2-114">However, if telemetry shows that any obsolete methods or metadata elements are still used, Microsoft will **not** delete them, to reduce the risk that consumers will be broken.</span></span>

## <a name="minimize-your-risk-of-being-affected"></a><span data-ttu-id="7bef2-115">影響を受けるリスクを最小限にする</span><span class="sxs-lookup"><span data-stu-id="7bef2-115">Minimize your risk of being affected</span></span>

<span data-ttu-id="7bef2-116">ここでは、メソッドおよびメタデータ要素が非推奨になるときに受ける影響を避けるために、Microsoft のコード ベースの消費者が使用できるヒントを示します。</span><span class="sxs-lookup"><span data-stu-id="7bef2-116">Here are some tips that you, as a consumer of the Microsoft code base, can use to avoid being affected when methods and metadata elements are deprecated:</span></span>

- <span data-ttu-id="7bef2-117">少なくとも 12 か月ごとに、コード ベースを最新のコード ベースでコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="7bef2-117">Compile your code base at least every 12 months on top of the latest code base.</span></span> <span data-ttu-id="7bef2-118">非推奨の成果物が使用されるために警告が表示される場合は、できるだけ早く警告を解決します。</span><span class="sxs-lookup"><span data-stu-id="7bef2-118">If you receive any warnings because deprecated artifacts are used, address those warnings as soon as possible.</span></span>
- <span data-ttu-id="7bef2-119">非推奨の成果物での**新しい**依存関係は避けてください。</span><span class="sxs-lookup"><span data-stu-id="7bef2-119">Avoid **new** dependencies on deprecated artifacts.</span></span> <span data-ttu-id="7bef2-120">リリースが利用可能になるタイミングとテレメトリが利用可能になるタイミングには時間差があるため、Microsoft は成果物を削除する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7bef2-120">Microsoft might have just deleted the artifact, because there is a time window between when releases and telemetry are available.</span></span>

## <a name="list-of-deprecated-methods-and-metadata-elements"></a><span data-ttu-id="7bef2-121">非推奨のメソッドとメタデータの要素のリスト</span><span class="sxs-lookup"><span data-stu-id="7bef2-121">List of deprecated methods and metadata elements</span></span>

<span data-ttu-id="7bef2-122">参考のため、CustomerSource の[方法とメタデータの要素の廃止](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/DeprecationMME)ページにある Microsoft Excel ファイルをダウンロードしてください。各メジャー リリースで非推奨とマークされた成果物が示されています。</span><span class="sxs-lookup"><span data-stu-id="7bef2-122">For reference, download the Microsoft Excel file, available on the [Deprecation of methods and metadata elements](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/DeprecationMME) page of CustomerSource, which shows the artifacts that have been marked for deprecation in each major release.</span></span>

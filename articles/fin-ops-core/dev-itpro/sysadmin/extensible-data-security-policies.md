---
title: 拡張可能なデータ セキュリティ ポリシー
description: このトピックでは、Finance and Operations アプリにおける拡張可能なデータ セキュリティ (XDS) ポリシーの概要を提供します。
author: Peakerbl
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: sericks
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 04a2bfac48cc74d3183c6d6af1bbafead0c1b80b
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944667"
---
# <a name="extensible-data-security-policies"></a><span data-ttu-id="bf210-103">拡張可能なデータ セキュリティ ポリシー</span><span class="sxs-lookup"><span data-stu-id="bf210-103">Extensible data security policies</span></span> 
[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf210-104">このトピックでは、Finance and Operations アプリにおける拡張可能なデータ セキュリティ (XDS) ポリシーの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="bf210-104">This topic provides an overview of Extensible Data Security (XDS) policies in Finance and Operations apps.</span></span> <span data-ttu-id="bf210-105">XDS を使用すると、開発者は、セキュリティ ポリシーに基づいてテーブル レコードへのアクセスを制限することにより、ロールベースのセキュリティを補うことができます。</span><span class="sxs-lookup"><span data-stu-id="bf210-105">XDS allows developers to supplement role-based security by restricting access to table records based on security policies.</span></span> <span data-ttu-id="bf210-106">ポリシー内のクエリにはフィルターが適用されます。また、そのフィルターの条件を満たすレコードだけが、制限されたテーブルからアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="bf210-106">The query in the policy applies a filter and only records that satisfy the conditions of the filter will be accessible from the restricted tables.</span></span>

## <a name="data-security-policy-components"></a><span data-ttu-id="bf210-107">データ セキュリティ ポリシー コンポーネント</span><span class="sxs-lookup"><span data-stu-id="bf210-107">Data security policy components</span></span>

-   <span data-ttu-id="bf210-108">**制約付きテーブル**: データがフィルタ処理またはセキュリティ保護されているテーブル。</span><span class="sxs-lookup"><span data-stu-id="bf210-108">**Constrained tables**: The table or tables from which data is filtered or secured.</span></span> <span data-ttu-id="bf210-109">たとえば、顧客に基づく取引へのアクセスを保護するポリシーでは、**CustTrans** は制約されたテーブルの例になります。</span><span class="sxs-lookup"><span data-stu-id="bf210-109">For example, in a policy that secures access to transactions based on customer, the **CustTrans** would be an example of a constrained table.</span></span>

-   <span data-ttu-id="bf210-110">**プライマリ テーブル**: 関連する制約付きテーブルの内容を保護するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf210-110">**Primary table**: Used to secure the content of the related constrained table.</span></span> <span data-ttu-id="bf210-111">次の例では、**CustTable** テーブルがプライマリ テーブルになります。</span><span class="sxs-lookup"><span data-stu-id="bf210-111">In the example below, the **CustTable** table would be the primary table.</span></span>
    <span data-ttu-id="bf210-112">プライマリ テーブルには、制約されたテーブルと明示的な関係である必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf210-112">The primary table must have an explicit relationship to the constrained tables.</span></span>

-   <span data-ttu-id="bf210-113">**ポリシー クエリ**: プライマリ テーブルの内容に対する範囲条件を使用して、制約を適用するテーブル コンテンツを保護するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf210-113">**Policy query**: Used to secure the constrained tables content using a range condition on the primary table contents.</span></span> <span data-ttu-id="bf210-114">範囲に含まれるレコードのみがアクセス可能になります。</span><span class="sxs-lookup"><span data-stu-id="bf210-114">Only records that are included in the range will be accessible.</span></span> <span data-ttu-id="bf210-115">この範囲は、顧客の特定の値に基づいている場合などに使用できます。</span><span class="sxs-lookup"><span data-stu-id="bf210-115">The range can, for example, be based on a specific value for Customer.</span></span>

-   <span data-ttu-id="bf210-116">**コンテキスト** – ポリシーが適用される条件を制御します。</span><span class="sxs-lookup"><span data-stu-id="bf210-116">**Context** – Controls the conditions under which a policy is applicable.</span></span>
    <span data-ttu-id="bf210-117">主に 2 種類のコンテンツを利用できます。</span><span class="sxs-lookup"><span data-stu-id="bf210-117">Two main types of contexts are available:</span></span>

    -   <span data-ttu-id="bf210-118">**ロール コンテキスト**: ユーザーが割り当てられているロールに基づきます。</span><span class="sxs-lookup"><span data-stu-id="bf210-118">**Role context**: Based on the roles that the user is assigned.</span></span> <span data-ttu-id="bf210-119">ロール コンテキストには 2 つのサブオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="bf210-119">There are two sub-options for role context:</span></span>

        -   <span data-ttu-id="bf210-120">**RoleName** – セキュリティ ポリシーは、RoleName の値と等しいロールに割り当てられているアプリケーション ユーザーにのみ適用されることを示します。</span><span class="sxs-lookup"><span data-stu-id="bf210-120">**RoleName** – Indicates that the security policy is only applied to the application user assigned to the role equal to the value of RoleName.</span></span>

        -   <span data-ttu-id="bf210-121">**RoleProperty** – この値は、**ContextString** プロパティと組み合わせて使用され、複数のロール コンテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="bf210-121">**RoleProperty** – This value is used in combination with the **ContextString** property to specify multiple user roles context.</span></span> <span data-ttu-id="bf210-122">ポリシーの **ロール プロパティ** フィールドで定義されているコンテキスト文字列の値が、割り当てられたユーザー ロールの **ContextString** フィールドの値と同じである場合に適用されます。</span><span class="sxs-lookup"><span data-stu-id="bf210-122">It is applied when the Context String value defined in the **Role Property** field for the policy is the same as the **ContextString** field value for the assigned user roles.</span></span>

    -   <span data-ttu-id="bf210-123">**アプリケーション コンテキスト**: XDS::SetContext API を使用しているアプリケーションによって設定されたコンテキスト文字列が、ポリシーの **コンテキスト文字列** フィールドで定義した値と同じである場合に適用されます。</span><span class="sxs-lookup"><span data-stu-id="bf210-123">**Application context**: Applied if the context string set by the application using the XDS::SetContext API is the same as the value defined in the **Context String** field for the policy.</span></span>

        ![AOTXDS 概念モデル](media/c74bc4ea12f084dfbaddb024685843e8.jpg)

<span data-ttu-id="bf210-125">アプリケーション オブジェクト ツリー (AOT) では、ポリシーとそのコンポーネントが **セキュリティ \> ポリシー** に基づいて表示されます。</span><span class="sxs-lookup"><span data-stu-id="bf210-125">In the Application Object Tree (AOT), policies and their components are displayed under **Security \> Policies.**</span></span>

## <a name="important-considerations"></a><span data-ttu-id="bf210-126">重要な考慮事項</span><span class="sxs-lookup"><span data-stu-id="bf210-126">Important considerations</span></span>

<span data-ttu-id="bf210-127">ポリシー クエリは、指定された制約付きテーブルを含む選択、更新、削除、および挿入の各操作において WHERE 句または ON 句に追加されます。</span><span class="sxs-lookup"><span data-stu-id="bf210-127">The policy query is added to the WHERE clause, or ON clause, on SELECT, UPDATE, DELETE and INSERT operations involving the specified constrained tables.</span></span> <span data-ttu-id="bf210-128">入念に設計され、テストされていない限り、ポリシー クエリはパフォーマンスに重要な影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bf210-128">Unless carefully designed and tested, policy queries can have a significant performance impact.</span></span> <span data-ttu-id="bf210-129">したがって、拡張可能なデータ セキュリティ ポリシーを開発する場合は、必ず単純ですが、重要なガイドラインに従ってください。</span><span class="sxs-lookup"><span data-stu-id="bf210-129">Therefore, make sure to follow simple but important guidelines when developing an extensible data security policy.</span></span> <span data-ttu-id="bf210-130">詳細については、[拡張可能なデータ セキュリティ ポリシーの開発 (ホワイト ペーパー) [AX 2012]](/dynamicsax-2012/appuser-itpro/developing-extensible-data-security-policies-white-paper) の「拡張可能なデータ セキュリティ ポリシーの開発」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf210-130">For more information, see the "Developing efficient extensible data security policies" section in [Developing Extensible Data Security Policies (White paper) [AX 2012]](/dynamicsax-2012/appuser-itpro/developing-extensible-data-security-policies-white-paper).</span></span>

<span data-ttu-id="bf210-131">2 つ以上のセキュリティ ポリシーが適用されている場合は、各ポリシーに含まれるレコードの交差 (和集合ではない) のみが、アクセス可能なレコードとなります。</span><span class="sxs-lookup"><span data-stu-id="bf210-131">When two or more security policies apply, the intersection (not the union) of the records that are included by each policy are the only records that can be accessed.</span></span> <span data-ttu-id="bf210-132">つまり、レコードへのアクセスを許可する前に、レコードが適用可能なすべてのセキュリティ ポリシーを満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf210-132">This means that a record must satisfy all the applicable security policies before access to the record is allowed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bf210-133">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bf210-133">Additional resources</span></span>

<span data-ttu-id="bf210-134">ポリシーをデバッグする方法の詳細については、制限されたテーブルのチェーン、式に基づくテーブルの関係を含むより詳細なポリシーを作成し、これらのリソースを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf210-134">For information about how to debug policies, create more advanced policies, including chaining of restricted tables, table relations based on expressions and much more please refer to these resources:</span></span>

- [<span data-ttu-id="bf210-135">単純なセキュリティ ポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="bf210-135">Create a simple security policy</span></span>](create-simple-security-policy.md)

- <span data-ttu-id="bf210-136">[拡張可能なデータ セキュリティ ポリシーの開発 (ホワイト ペーパー) [AX 2012]](/dynamicsax-2012/appuser-itpro/developing-extensible-data-security-policies-white-paper)</span><span class="sxs-lookup"><span data-stu-id="bf210-136">[Developing Extensible Data Security Policies (white paper) [AX 2012]](/dynamicsax-2012/appuser-itpro/developing-extensible-data-security-policies-white-paper)</span></span>

- <span data-ttu-id="bf210-137">[拡張可能なデータ セキュリティを使用して分析コード値ごとのデータの保護 (ホワイト ペーパー) [AX 2012]](/dynamicsax-2012/appuser-itpro/securing-data-by-dimension-value-by-using-extensible-data-security-white-paper)</span><span class="sxs-lookup"><span data-stu-id="bf210-137">[Securing Data by Dimension Value by using Extensible Data Security (white paper) [AX 2012]](/dynamicsax-2012/appuser-itpro/securing-data-by-dimension-value-by-using-extensible-data-security-white-paper)</span></span>

- <span data-ttu-id="bf210-138">[拡張可能なデータ セキュリティの例 – Andre Arnaud De Calavon [ブログ]](https://dynamicspedia.com/tag/xds/)</span><span class="sxs-lookup"><span data-stu-id="bf210-138">[Extensible Data Security examples – by Andre Arnaud De Calavon [blog]](https://dynamicspedia.com/tag/xds/)</span></span>

- <span data-ttu-id="bf210-139">[D365FO - Alex Meyer [ブログ]での拡張可能なデータ セキュリティ (XDS) フレームワーク](https://alexdmeyer.com/2019/02/20/extensible-data-security-xds-framework-in-d365fo/)</span><span class="sxs-lookup"><span data-stu-id="bf210-139">[Extensible Data Security (XDS) Framework in D365FO - by Alex Meyer [blog]](https://alexdmeyer.com/2019/02/20/extensible-data-security-xds-framework-in-d365fo/)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

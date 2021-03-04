---
title: Dynamics 365 for Finance and Operations Enterprise Edition プラットフォーム更新プログラム 9 (2017 年 7 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations Enterprise Edition プラットフォーム更新プログラム 9 の新機能または変更された機能について説明します。 このバージョンは 2017 年 7 月にリリースされました。
author: tonyafehr
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: b2b57475670eed8db99c87a9f5bfb923273f9596
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797803"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-enterprise-edition-platform-update-9-july-2017"></a><span data-ttu-id="d7f5f-104">Dynamics 365 for Finance and Operations Enterprise Edition プラットフォーム更新プログラム 9 (2017 年 7 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="d7f5f-104">What's new or changed in Dynamics 365 for Finance and Operations, Enterprise edition platform update 9 (July 2017)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7f5f-105">このトピックでは、Dynamics 365 for Finance and Operations Enterprise Edition プラットフォーム更新プログラム 9 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-105">This topic describes features that are either new or changed in Dynamics 365 for Finance and Operations, Enterprise edition platform update 9.</span></span> <span data-ttu-id="d7f5f-106">このバージョンは 2017 年 7 月にリリースされ、ビルド番号は 7.0.4612.35162 です。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-106">This version was released in July 2017 and has a build number of 7.0.4612.35162.</span></span>

<span data-ttu-id="d7f5f-107">新機能についての補足情報の検索および開発中の新機能に関する詳細については、[Dynamics 365 ロードマップ](https://roadmap.dynamics.com/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-107">Go to the [Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to find supplemental information about new features and learn more about what new features are in development.</span></span> <span data-ttu-id="d7f5f-108">プラットフォーム更新プログラム 9 に含まれるバグ修正の詳細については、Lifecycle Services (LCS) にログインし、この [サポート技術情報記事](https://go.microsoft.com/fwlink/?linkid=853624) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-108">For information about the bug fixes included in Platform update 9, log in to Lifecycle Services (LCS) and view this [KB article](https://go.microsoft.com/fwlink/?linkid=853624).</span></span>

## <a name="batch-job-history-clean-up"></a><span data-ttu-id="d7f5f-109">バッチ ジョブ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="d7f5f-109">Batch job history clean-up</span></span>

<span data-ttu-id="d7f5f-110">バッチ ジョブの履歴をクリーンアップする機能が追加されました (Dynamics AX 2012 で使用できた機能)。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-110">Functionality to clean up the history of batch jobs has been added (this functionality was available in Dynamics AX 2012).</span></span> <span data-ttu-id="d7f5f-111">この機能を使用すると、ボタンをクリックしてバッチジョブ履歴のすべてまたは一部を削除できます。 </span><span class="sxs-lookup"><span data-stu-id="d7f5f-111">This feature allows you to delete all or any subset of batch job history by clicking a button.</span></span> <span data-ttu-id="d7f5f-112">特定のフォームを使用することで、バッチ ジョブの名前、会社、状態、または完了時間などの異なる基準で、バッチ ジョブ履歴をフィルターし、フィルター処理済みのサブセットを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-112">Using a specific form, you can filter the batch job history by different criteria, such as batch job name, company, status, or finished time, and then delete the filtered subset.</span></span> <span data-ttu-id="d7f5f-113">履歴を整理して関連性を維持することに加えて、この機能は長期間監視されていない場合に、履歴テーブル内に大量のエントリを持つ負のパフォーマンスを排除することによりパフォーマンスも向上させます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-113">In addition to keeping the history notes clean and relevant, this feature also provides performance enhancements by eliminating the negative performance impact of having a large volume of entries in history tables, if left unmonitored for long periods of time.</span></span> <span data-ttu-id="d7f5f-114">プラットフォーム更新プログラム 9 より前に、職務ごとに履歴を削除する必要があります。そのためには希望するすべての職務をカバーする余分な時間が必須です。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-114">Before Platform update 9, you needed to delete the history on a job-by-job basis, which required extra time to cover all the wanted jobs.</span></span>

<span data-ttu-id="d7f5f-115">**システム管理** ワークスペース - **バッチ ジョブ履歴クリーンアップ** に 2 つの新しいフォームが追加されました (通常およびカスタム バージョン)。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-115">Two new forms have been added to the **System Administration** workspace – **Batch job history clean-up** (regular and custom version).</span></span>

<span data-ttu-id="d7f5f-116">バッチ ジョブ履歴クリーンアップの通常バージョンを使用すると、指定した時間枠 (日) より古いすべての履歴エントリをすばやく消去できます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-116">The regular version of batch job history clean-up allows you to quickly clean all history entries older than a specified timeframe (in days).</span></span> <span data-ttu-id="d7f5f-117">\<Today\> - \<History limit\> よりも前に作成されたエントリは、**BatchJobHistory** テーブルから削除され、関連するレコード (**BatchHistory** および **BatchConstraintsHistory**) のリンク テーブルからも削除されます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-117">Any entry that was created prior to \<Today\> - \<History limit\> will be deleted from the **BatchJobHistory** table, as well as from linked tables with related records (**BatchHistory** and **BatchConstraintsHistory**).</span></span> <span data-ttu-id="d7f5f-118">このフォームでは、フィルター処理を実行する必要がないため、パフォーマンスの最適化が向上しました。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-118">This form has improved performance optimization because it doesn't have to execute any filtering.</span></span>

<span data-ttu-id="d7f5f-119">カスタム バッチ ジョブのクリーンアップ フォームは、特定のエントリを削除する必要がある場合にのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-119">The custom batch job clean-up form should be used only when specific entries need to be deleted.</span></span> <span data-ttu-id="d7f5f-120">このフォームを使用すると、状態、職務説明、会社、ユーザーなどの基準に基づいて、バッチ ジョブ履歴レコードの選択したタイプをクリーン アップできます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-120">This form allows you to clean up selected types of batch job history records, based on criteria such as status, job description, company, or user.</span></span> <span data-ttu-id="d7f5f-121">他の基準は、**フィルター** ボタンを使用して追加することができます、</span><span class="sxs-lookup"><span data-stu-id="d7f5f-121">Other criteria can be added using the **Filter** button.</span></span>

## <a name="change-of-usage-data-serialization-format"></a><span data-ttu-id="d7f5f-122">使用データのシリアル化形式の変更</span><span class="sxs-lookup"><span data-stu-id="d7f5f-122">Change of usage data serialization format</span></span>

<span data-ttu-id="d7f5f-123">通常、**SysLastValue** テーブルに格納されている使用状況データは、バイナリ形式でシリアル化されず、代わりに文字列形式でシリアル化されます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-123">The usage data that is typically stored in the **SysLastValue** table will no longer be serialized in binary format, and instead will be serialized in string format.</span></span> <span data-ttu-id="d7f5f-124">このフォーマットの変更により、規模、コードのデバッグ能力、システム全体の信頼性が向上し、アプリケーション レイヤーからキャッシュに影響を与えないように変更できます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-124">This format change increases the scale, ability to debug the code, and overall reliability of the system, which allows for changes from the application layer to not have an effect on caches.</span></span> <span data-ttu-id="d7f5f-125">ただし、技術的な理由により、アップグレード プロセス中にデータの整合性を確保し、およびシステムの整合性と信頼性を確保することはできません。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-125">However, due to technical reasons it is not possible to ensure the integrity of the data during the upgrade process and ensure system integrity and reliability.</span></span>

<span data-ttu-id="d7f5f-126">使用状況データは、プラットフォーム更新プログラム 9 に移行すると自動的にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-126">Usage data is automatically reset upon moving to Platform update 9.</span></span> <span data-ttu-id="d7f5f-127">ユーザーは、このプラットフォーム更新プロセスの一部として、使用状況データを失います。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-127">Users will lose their usage data as part of this platform update process.</span></span> <span data-ttu-id="d7f5f-128">これには、主にカスタムクエリや保存されたダイアログ転記の選択に使用されるデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-128">This mostly includes data used for custom queries and saved dialog posting selections.</span></span> <span data-ttu-id="d7f5f-129">個人用設定が影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-129">Personalization is not affected.</span></span>

<span data-ttu-id="d7f5f-130">新しいデータ形式は、バージョン管理され、下位互換性があり、今後のアプリケーションおよびプラットフォーム リリースのために、プラットフォーム更新プログラム 9 以降で常に保持されます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-130">The new data format is versioned, backward compatible, and always preserved from Platform update 9 onward for future application and platform releases.</span></span>

## <a name="method-wrapping-and-chain-of-command"></a><span data-ttu-id="d7f5f-131">メソッドのラッピングとコマンド チェーン</span><span class="sxs-lookup"><span data-stu-id="d7f5f-131">Method wrapping and chain of command</span></span>

### <a name="overview"></a><span data-ttu-id="d7f5f-132">概要</span><span class="sxs-lookup"><span data-stu-id="d7f5f-132">Overview</span></span>

<span data-ttu-id="d7f5f-133">拡張クラス (クラス強化とも呼ばれる) の機能が強化され、開発者は基本クラスで定義されたメソッドの周りに論理をラップすることができます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-133">The functionality of extension classes (also known as class augmentation) has been improved to allow developers to wrap logic around methods defined in a base class.</span></span> <span data-ttu-id="d7f5f-134">これにより、イベント ハンドラーを使用することがなくパブリック メソッドとプロテクト メソッドのロジックを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-134">This allows extending the logic of public and protected methods without the need to use event handlers.</span></span> <span data-ttu-id="d7f5f-135">メソッドをラップするときは、クラスのその他のパブリック メソッドと保護されたメソッド、および変数にもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-135">When you wrap a method, you can also access other public and protected methods and variables of the class.</span></span> <span data-ttu-id="d7f5f-136">こうすることで、トランザクションを開始し、クラスに関連付けられた状態変数を容易に管理することができます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-136">This way, you can start transactions and easily manage state variables associated with your class.</span></span>

<span data-ttu-id="d7f5f-137">以下のような状況を考えてください。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-137">Consider the following situation.</span></span> <span data-ttu-id="d7f5f-138">モデルには次のコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-138">A model contains the following code.</span></span>

```
class BaseClass1
{
    str method1(int arg) {
        …
    }
}
```

<span data-ttu-id="d7f5f-139">同じ名前を再利用してプレロジックおよびポストロジックを追加することによって、拡張クラスを使用している method1 の機能を拡張できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-139">It is now possible to extend the functionality of method1 using an extension class by reusing the same name to add pre-and post-logic to it.</span></span>

```
[ExtensionOf(ClassStr(BaseClass1))]
class BaseClass1_Extension
{
    str method1(int arg) {
        // Part 1
        var s = next method1(arg + 4);
        // Part 2
        return s;
    }
}
```

<span data-ttu-id="d7f5f-140">method1 と次のキーワードの使用の必要をラッピングするとメソッドの指揮命令系統 (CoC) が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-140">Wrapping method1 and the required use of the next keyword creates a Chain of Command (CoC) for the method.</span></span> <span data-ttu-id="d7f5f-141">次のコードの実行時の動作を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-141">Here is what happens when the following code executes.</span></span>

```
BaseClass1 c = new BaseClass1();
Print c.method1(33);
```

<span data-ttu-id="d7f5f-142">システムは method1 をラップするメソッドを検出します。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-142">The system will find any method that wraps method1.</span></span> <span data-ttu-id="d7f5f-143">BaseClass1\_Extension クラスの method1 など、これらのメソッドのうちいずれかをランダムに実行します。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-143">It will randomly execute one of these methods, such as method1 of the BaseClass1\_Extension class.</span></span> <span data-ttu-id="d7f5f-144">次の method1() への呼び出しが発生すると、システムは CoC 内の別のメソッドをランダムに選択するか、または存在しない場合は、元の実装を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-144">When the call to next method1() occurs, the system will randomly pick another method in the CoC or call the original implementation if none exist.</span></span>

### <a name="supported-versions"></a><span data-ttu-id="d7f5f-145">サポートされているバージョン</span><span class="sxs-lookup"><span data-stu-id="d7f5f-145">Supported versions</span></span>

<span data-ttu-id="d7f5f-146">このトピックで説明する機能は、Platform update 9 (CoC および保護されたメソッドと変数へのアクセス) の時点で利用できます。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-146">The functionality described in this topic is available as of Platform update 9 (CoC and access to protected methods and variables).</span></span>

<span data-ttu-id="d7f5f-147">ただし、この機能は強化されているクラスがプラットフォーム更新プログラム 9 でコンパイルされることを要求します。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-147">However, this functionality requires the class being augmented to be compiled on Platform update 9.</span></span> <span data-ttu-id="d7f5f-148">Dynamics 365 for Finance and Operations、Enterprise Edition アプリケーションの現在のリリースはプラットフォーム更新プログラム 8 またはそれ以前でコンパイルされているため、そのパッケージに定義されているメソッドをラップするにはプラットフォーム更新プログラム 9 以降の基本パッケージ (アプリケーション スイートなど) を再コンパイルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-148">Because the current releases of the Dynamics 365 for Finance and Operations, Enterprise edition applications have been compiled on Platform update 8 or earlier, you will need to recompile a base package (like Application Suite) on Platform update 9 or newer in order to wrap a method that is defined in that package.</span></span>

## <a name="odata-batch-request-size-configuration"></a><span data-ttu-id="d7f5f-149">OData バッチ要求サイズの構成</span><span class="sxs-lookup"><span data-stu-id="d7f5f-149">OData batch request size configuration</span></span>

<span data-ttu-id="d7f5f-150">既定の OData バッチ要求サイズは、1,000 レコードです。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-150">The default OData batch request size is 1,000 records.</span></span> <span data-ttu-id="d7f5f-151">Microsoft は、顧客の OData バッチ要求のサイズを変更できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-151">Microsoft can now change the size of OData batch requests for customers.</span></span> <span data-ttu-id="d7f5f-152">バッチ サイズを最大 5,000 レコードまで増やすには、LCS を介して Dynamics サービス エンジニアリング チーム (DSE) にサポート リクエストを記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-152">Customers must log a support request through LCS to the Dynamics Service Engineering team (DSE) to increase the batch size up to a maximum value of 5,000 records.</span></span> <span data-ttu-id="d7f5f-153">詳細については、[Dynamics サービス エンジニア リング チームへのサービス要求の送信](../../dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-153">For more information, see [Submit service requests to the Dynamics Service Engineering team](../../dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md)</span></span>

## <a name="system-startup-performance-for-virtual-machines"></a><span data-ttu-id="d7f5f-154">仮想マシンのシステム起動パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="d7f5f-154">System startup performance for virtual machines</span></span>

<span data-ttu-id="d7f5f-155">メタデータの読み込みのパフォーマンスの問題が解決されたため、仮想マシン システムが起動するときにシステムがフリーズすることはなくなりました。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-155">Performance issues with loading metadata have been addressed, so you should no longer experience a system freeze when a virtual machine starts.</span></span>

> [!NOTE]
> <span data-ttu-id="d7f5f-156">この問題は、ビルド コンピューター (参加リストがあり、コードをコンパイルする VM) として使用される仮想マシンで発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="d7f5f-156">This issue will still occur on virtual machines that are used as build machines (VMs that have enlistments and compile code).</span></span>

---
title: "小売チャネルの会計統合"
description: "このトピックでは、Retail POS の会計統合の概要を示します。"
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: ja-jp
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="c2c13-103">小売チャネルの会計統合</span><span class="sxs-lookup"><span data-stu-id="c2c13-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2c13-104">このトピックは、Microsoft Dynamics 365 for Retail で利用できる会計統合機能の概要です。</span><span class="sxs-lookup"><span data-stu-id="c2c13-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="c2c13-105">会計統合機能は、小売業界における不正を防止する地域の会計法をサポートするために設計されたフレームワークです。</span><span class="sxs-lookup"><span data-stu-id="c2c13-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="c2c13-106">会計統合を使用してカバーすることができる典型的なシナリオは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c2c13-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="c2c13-107">会計レシートを印刷し、顧客に提供する。</span><span class="sxs-lookup"><span data-stu-id="c2c13-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="c2c13-108">POS で実施された売上および返品に関連する情報の、当局が提供する外部サービスへの提出を確保する。</span><span class="sxs-lookup"><span data-stu-id="c2c13-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="c2c13-109">当局によって承認されたデジタル署名によるデータ保護の使用。</span><span class="sxs-lookup"><span data-stu-id="c2c13-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="c2c13-110">このトピックでは、ユーザーが次のタスクを実行できるように、会計統合を設定するためのガイドラインを示します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="c2c13-111">貯蓄、デジタル署名、会計データの保護された送信などの会計登録目的で使用する会計デバイスまたはサービスである会計コネクタをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="c2c13-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="c2c13-112">出力メソッドと会計ドキュメントの生成のアルゴリズムを定義するドキュメント プロバイダーをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="c2c13-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="c2c13-113">一連のステップと各ステップで使用されるコネクタのグループを定義する会計登録プロセスをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="c2c13-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="c2c13-114">会計登録プロセスを POS 機能プロファイルに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c2c13-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="c2c13-115">コネクタ技術プロファイルを、ハードウェア プロファイル (ローカルの会計コネクタ用) または POS 機能プロファイル (他の会計コネクタ タイプ用) のいずれかに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c2c13-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="c2c13-116">会計統合実行フロー</span><span class="sxs-lookup"><span data-stu-id="c2c13-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="c2c13-117">次のシナリオでは、一般的な会計統合実行フローを示します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="c2c13-118">会計登録プロセスの初期化</span><span class="sxs-lookup"><span data-stu-id="c2c13-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="c2c13-119">小売トランザクションが終了した後など、会計登録が必要なアクションを実行した後は、会計登録プロセスは現在の POS 機能プロファイルに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="c2c13-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="c2c13-120">会計コネクタを検索します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="c2c13-121">会計登録プロセスに含まれる会計登録ステップごとに、システムにより会計コネクタの一覧と照合されます。</span><span class="sxs-lookup"><span data-stu-id="c2c13-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="c2c13-122">これらのコネクタには、指定されたコネクタ グループに含まれる機能プロファイルと、現在のハードウェア プロファイル (**ローカル**のみに対応するコネクタ タイプ用) または現在の POS 機能プロファイル (他のコネクタ タイプ用) に関連した技術プロファイルを持つコネクタの一覧があります。</span><span class="sxs-lookup"><span data-stu-id="c2c13-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="c2c13-123">会計統合を実行します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="c2c13-124">システムは、検索されたコネクタとリンクされているアセンブリで定義されているすべての必要なアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="c2c13-125">これは、このコネクタの前の手順で見つかった機能プロファイルおよび技術プロファイルの設定に従って実行されます。</span><span class="sxs-lookup"><span data-stu-id="c2c13-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="c2c13-126">会計統合を使用する前に必要な設定</span><span class="sxs-lookup"><span data-stu-id="c2c13-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="c2c13-127">会計統合機能を使用する前に、次の設定を定義する必要があります:</span><span class="sxs-lookup"><span data-stu-id="c2c13-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="c2c13-128">会計機能プロファイル番号の**小売パラメーター**ページで番号順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="c2c13-129">以下の参照の**小売共有パラメーター**ページで番号順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="c2c13-130">会計技術プロファイル番号</span><span class="sxs-lookup"><span data-stu-id="c2c13-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="c2c13-131">会計コネクタ グループ番号</span><span class="sxs-lookup"><span data-stu-id="c2c13-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="c2c13-132">登録プロセス番号</span><span class="sxs-lookup"><span data-stu-id="c2c13-132">Registration process number</span></span>

- <span data-ttu-id="c2c13-133">会計統合のために使用する予定のデバイスまたはサービスごとに、**小売 > チャネル設定 > 会計統合 > 会計コネクタ**で**会計コネクタ**を作成します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="c2c13-134">すべての会計コネクタに**小売 > チャネル設定 > 会計統合 > 会計ドキュメント プロバイダー**で**会計ドキュメント プロバイダー**を作成します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="c2c13-135">データ マッピングは、会計ドキュメント プロバイダーの一部と見なされます。</span><span class="sxs-lookup"><span data-stu-id="c2c13-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="c2c13-136">同じコネクター (州固有の規則など) に異なるデータ マッピングを設定するには、異なる会計文書プロバイダーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2c13-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="c2c13-137">**小売 > チャンネル設定 > 会計統合 > コネクタ機能プロファイル**で会計ドキュメント プロバイダーごとに**コネクタ機能プロファイル**を作成します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="c2c13-138">コネクタ名を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-138">Select a connector name.</span></span>
  - <span data-ttu-id="c2c13-139">ドキュメント プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-139">Select a document provider.</span></span>
  - <span data-ttu-id="c2c13-140">**サービス設定**タブで VAT 率の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="c2c13-141">**データ マッピング**タブで VAT コード マッピングと支払/入金タイプのマッピングを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="c2c13-142">例</span><span class="sxs-lookup"><span data-stu-id="c2c13-142">Examples</span></span> 

  |  | <span data-ttu-id="c2c13-143">書式設定</span><span class="sxs-lookup"><span data-stu-id="c2c13-143">Format</span></span> | <span data-ttu-id="c2c13-144">例</span><span class="sxs-lookup"><span data-stu-id="c2c13-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="c2c13-145">VAT 率の設定</span><span class="sxs-lookup"><span data-stu-id="c2c13-145">VAT rates settings</span></span> | <span data-ttu-id="c2c13-146">値 : VATrate</span><span class="sxs-lookup"><span data-stu-id="c2c13-146">value : VATrate</span></span> | <span data-ttu-id="c2c13-147">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="c2c13-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="c2c13-148">VAT コードのマッピング</span><span class="sxs-lookup"><span data-stu-id="c2c13-148">VAT codes mapping</span></span> | <span data-ttu-id="c2c13-149">VATcode : 値</span><span class="sxs-lookup"><span data-stu-id="c2c13-149">VATcode : value</span></span> | <span data-ttu-id="c2c13-150">vat20: 1、vat18: 2</span><span class="sxs-lookup"><span data-stu-id="c2c13-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="c2c13-151">支払/入金タイプのマッピング</span><span class="sxs-lookup"><span data-stu-id="c2c13-151">Tender types mapping</span></span> | <span data-ttu-id="c2c13-152">TenderTyp: 値</span><span class="sxs-lookup"><span data-stu-id="c2c13-152">TenderTyp : value</span></span> | <span data-ttu-id="c2c13-153">現金 : 1, カード : 2</span><span class="sxs-lookup"><span data-stu-id="c2c13-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="c2c13-154">**小売 > チャネル設定 > 会計統合 > 会計コネクタ グループ**で**会計コネクタ グループ**を作成します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="c2c13-155">コネクタ グループは、同じ機能を実行し、会計登録プロセスの同じ段階で使用される会計コネクタにリンクされた機能プロファイルのサブセットです。</span><span class="sxs-lookup"><span data-stu-id="c2c13-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="c2c13-156">機能プロファイルをコネクタ グループに追加します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="c2c13-157">**機能プロファイル**ページで**追加**をクリックしてから、プロファイル番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="c2c13-158">機能プロファイルの使用を中断する場合は、**無効にする**を**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="c2c13-159">この変更は、現在のコネクタ グループのみに影響します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-159">This change affects the current connector group only.</span></span> <span data-ttu-id="c2c13-160">他のコネクタ グループで同じ機能プロファイルを引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="c2c13-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="c2c13-161">コネクタ グループ内では、各会計コネクタには 1 つの機能プロファイルしか含めることができません。</span><span class="sxs-lookup"><span data-stu-id="c2c13-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="c2c13-162">**小売 > チャネル設定 > 会計統合 > コネクタ技術プロファイル**で会計コネクタごとに**コネクタ技術プロファイル**を作成します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="c2c13-163">コネクタ名を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-163">Select a connector name.</span></span>
  - <span data-ttu-id="c2c13-164">コネクタ タイプを選択します:</span><span class="sxs-lookup"><span data-stu-id="c2c13-164">Select a connector type:</span></span> 
      - <span data-ttu-id="c2c13-165">**ローカル** - 物理デバイスまたはローカル コンピューターにインストールされるアプリケーションには、このタイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="c2c13-166">**内部** - 会計デバイスおよび Retail サーバーに接続されているサービスには、このタイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="c2c13-167">**外部** - 税務当局によって提供される Web ポータルなどの外部の会計サービスには、このタイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="c2c13-168">**接続**タブで設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="c2c13-169">以前に読み込まれたコンフィギュレーションの更新されたバージョンは、機能プロファイルと技術プロファイルの両方に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="c2c13-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="c2c13-170">適切なコネクタまたはドキュメント プロバイダーが既に使用されている場合は、通知されます。</span><span class="sxs-lookup"><span data-stu-id="c2c13-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="c2c13-171">既定では、機能および技術プロファイルで手動で作成されているすべての変更が保存されます。</span><span class="sxs-lookup"><span data-stu-id="c2c13-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="c2c13-172">これらのプロファイルをコンフィギュレーションの既定のパラメーター セットで上書きするには、**コネクタ機能プロファイル**ページおよび**コネクタ技術プロファイル**ページで**更新**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c2c13-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="c2c13-173">**小売 > チャネル設定 > 会計統合 > 会計登録プロセス**で会計統合の固有のプロセスごとに**会計登録プロセス**を作成します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="c2c13-174">登録プロセスは、登録ステップおよび各ステップで使用されるコネクタ グループの順序によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="c2c13-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="c2c13-175">プロセスに登録ステップを追加します:</span><span class="sxs-lookup"><span data-stu-id="c2c13-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="c2c13-176">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c2c13-176">Click **Add**.</span></span>
      - <span data-ttu-id="c2c13-177">コネクタ タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="c2c13-178">このフィールドは、システムが技術プロファイルでコネクタを検索する場所を、コネクタ タイプ**ローカル**のハードウェア プロファイル、または他の会計コネクタ タイプの POS 機能プロファイルのいずれかで定義します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="c2c13-179">コネクタ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="c2c13-180">**検証**をクリックして、登録プロセスの構造の整合性を確認します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="c2c13-181">次の場合に検証を行うことをお勧めします:</span><span class="sxs-lookup"><span data-stu-id="c2c13-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="c2c13-182">POS 機能プロファイルおよびハードウェア プロファイルへのバインディングを含む、すべての設定が完了した後の新しい登録プロセス。</span><span class="sxs-lookup"><span data-stu-id="c2c13-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="c2c13-183">既存の登録プロセスに更新を行った後。</span><span class="sxs-lookup"><span data-stu-id="c2c13-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="c2c13-184">**小売 > チャネル設定 > POS 設定 > POS プロファイル > 機能プロファイル**で会計登録プロセスを POS 機能プロファイルにバインドします。</span><span class="sxs-lookup"><span data-stu-id="c2c13-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="c2c13-185">**会計登録プロセス**タブで**編集**をクリックしてから、**プロセス番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="c2c13-186">**小売 > チャネル設定 > POS 設定 > POS プロファイル > ハードウェア プロファイル**でコネクタ技術プロファイルをハードウェア プロファイルにバインドします。</span><span class="sxs-lookup"><span data-stu-id="c2c13-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="c2c13-187">**会計技術プロファイル**タブで**編集**をクリックしてから、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c2c13-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="c2c13-188">**プロファイル番号**フィールドでコネクタ技術プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c2c13-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="c2c13-189">ハードウェア プロファイルには、複数の技術プロファイルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c2c13-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="c2c13-190">ただし、ハードウェア プロファイルにいずれかのコネクタ グループとの共通部分が 1 つ以上ある場合は、この方法はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="c2c13-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="c2c13-191">不適切な設定を避けるために、すべてのハードウェア プロファイルを更新した後は登録プロセスを検証することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c2c13-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>


<span data-ttu-id="92696-101">環境間でデータベースをコピーするとき、コピーされたデータベースが完全に機能するには、その前に環境の再プロビジョニング ツールを実行して、すべての Retail コンポーネントを確実に最新にしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="92696-101">When copying a database between environments, you will need to run the environment re-provisioning tool before the copied database is fully functional, to ensure that all Retail components are up-to-date.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92696-102">小売機能はすべての環境に含まれているため、Retail コンポーネントを使用しているかどうかに関係なく、このプロシージャを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="92696-102">We recommend that you run this procedure whether you are using Retail components or not, because Retail functionality is included in all environments.</span></span> 

<span data-ttu-id="92696-103">続行する前に、次の前提条件が満たされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92696-103">Before you continue, you must make sure that the following prerequisites are met:</span></span>

1. <span data-ttu-id="92696-104">ターゲット環境で 2017 年 7 月リリース以降が実行されている場合は、次の更新プログラムを適用します。</span><span class="sxs-lookup"><span data-stu-id="92696-104">If your target environment is running the July 2017 release or later, apply the following updates</span></span>

   -   <span data-ttu-id="92696-105">KB 4035399</span><span class="sxs-lookup"><span data-stu-id="92696-105">KB 4035399</span></span>
   -   <span data-ttu-id="92696-106">KB 4045801</span><span class="sxs-lookup"><span data-stu-id="92696-106">KB 4045801</span></span>
2. <span data-ttu-id="92696-107">ターゲット環境で 11 月リリース (バージョン 1611) が実行されている場合は、次の修正プログラムを適用します。</span><span class="sxs-lookup"><span data-stu-id="92696-107">If your target environment is running the November release (version 1611), apply the following hotfixes:</span></span>
   -   <span data-ttu-id="92696-108">KB 4025631</span><span class="sxs-lookup"><span data-stu-id="92696-108">KB 4025631</span></span>
   -   <span data-ttu-id="92696-109">KB 4035355</span><span class="sxs-lookup"><span data-stu-id="92696-109">KB 4035355</span></span>
   -   <span data-ttu-id="92696-110">KB 4035492</span><span class="sxs-lookup"><span data-stu-id="92696-110">KB 4035492</span></span>
   -   <span data-ttu-id="92696-111">KB 4010947</span><span class="sxs-lookup"><span data-stu-id="92696-111">KB 4010947</span></span>

3. <span data-ttu-id="92696-112">既定のチャネル データベースおよび既定のチャネル データ グループの名前は **既定** にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92696-112">The default channel database and the default channel data group must be named **Default**.</span></span> <span data-ttu-id="92696-113">これらの名前を変更していた場合は、名前を元に戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="92696-113">If you've renamed them, you must change the names back.</span></span>

<span data-ttu-id="92696-114">以下の手順に従って、環境再プロビジョニング ツールを実行します。</span><span class="sxs-lookup"><span data-stu-id="92696-114">Follow these steps to run the Environment reprovisioning tool.</span></span>

1. <span data-ttu-id="92696-115">共有アセット ライブラリで、**ソフトウェア配置可能なパッケージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92696-115">In the Shared asset library, select **Software deployable package**.</span></span>
2. <span data-ttu-id="92696-116">環境再プロビジョニング ツールをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="92696-116">Download the Environment reprovisioning tool.</span></span>
3. <span data-ttu-id="92696-117">自身のプロジェクトのアセット ライブラリで、**ソフトウェア配置可能パッケージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="92696-117">In the asset library for your project, select **Software deployable package**.</span></span>
4. <span data-ttu-id="92696-118">**新規作成** コマンドを選択して、新しいパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="92696-118">Select **New** to create a new package.</span></span>
5. <span data-ttu-id="92696-119">パッケージの名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="92696-119">Enter a name and description for the package.</span></span> <span data-ttu-id="92696-120">**環境再プロビジョニング ツール** をパッケージ名として使用できます。</span><span class="sxs-lookup"><span data-stu-id="92696-120">You can use **Environment reprovisioning tool** as the package name.</span></span>
6. <span data-ttu-id="92696-121">先ほどダウンロードしたパッケージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="92696-121">Upload the package that you downloaded earlier.</span></span>
7. <span data-ttu-id="92696-122">ターゲット環境の **環境の詳細** ページで、**管理** > **更新プログラムを適用** を順に選択します。</span><span class="sxs-lookup"><span data-stu-id="92696-122">On the **Environment details** page for your target environment, select **Maintain** > **Apply updates**.</span></span>
8. <span data-ttu-id="92696-123">先ほどアップロードした環境再プロビジョニング ツールを選択し、**適用** を選択してパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="92696-123">Select the Environment reprovisioning tool that you uploaded earlier, and then select **Apply** to apply the package.</span></span>
9. <span data-ttu-id="92696-124">パッケージの配置の進捗を監視します。</span><span class="sxs-lookup"><span data-stu-id="92696-124">Monitor the progress of the package deployment.</span></span> 

<span data-ttu-id="92696-125">配置可能パッケージを適用する方法の詳細については、[配置可能パッケージの適用](../deployment/create-apply-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92696-125">For more information about how to apply a deployable package, see [Apply a deployable package](../deployment/create-apply-deployable-package.md).</span></span> <span data-ttu-id="92696-126">配置可能パッケージを手動で適用する方法の詳細については、[配置可能パッケージのインストール](../deployment/install-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92696-126">For more information about how to manually apply a deployable package, see [Install a deployable package](../deployment/install-deployable-package.md).</span></span>

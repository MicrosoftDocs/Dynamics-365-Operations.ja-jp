<span data-ttu-id="1c313-101">環境間でデータベースをコピーする場合、環境再プロビジョニング ツールを実行し、すべての Retail コンポーネントを最新の状態にしない限り、コピーしたデータベースは完全には機能しません。</span><span class="sxs-lookup"><span data-stu-id="1c313-101">If you copy a database between environments, the copied database won't be fully functional until you run the Environment reprovisioning tool to make sure that all Retail components are up to date.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c313-102">Retail の機能はすべての環境に含まれているため、Retail コンポーネントを使用しない場合も、このプロシージャを完了しておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1c313-102">We recommend that you complete this procedure even if you don't use Retail components, because Retail functionality is included in all environments.</span></span> 

<span data-ttu-id="1c313-103">続行する前に、次の前提条件が満たされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c313-103">Before you continue, you must make sure that the following prerequisites are met:</span></span>

1. <span data-ttu-id="1c313-104">適切な更新プログラムがターゲット環境に適用されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c313-104">The appropriate updates are applied to the target environment:</span></span>

    - <span data-ttu-id="1c313-105">ターゲット環境で 7.3 リリース (2017 年 12 月) が実行されている場合は、次の更新プログラムを適用してください。</span><span class="sxs-lookup"><span data-stu-id="1c313-105">If the target environment runs the 7.3 release (December 2017), apply this update:</span></span>

        - <span data-ttu-id="1c313-106">KB 4091254</span><span class="sxs-lookup"><span data-stu-id="1c313-106">KB 4091254</span></span>

    - <span data-ttu-id="1c313-107">ターゲット環境で 7.2 リリース (2017 年 7 月) が実行されている場合は、次の更新プログラムを適用してください。</span><span class="sxs-lookup"><span data-stu-id="1c313-107">If the target environment runs the July 2017 release (7.2), apply these updates:</span></span>

        - <span data-ttu-id="1c313-108">KB 4035399</span><span class="sxs-lookup"><span data-stu-id="1c313-108">KB 4035399</span></span>
        - <span data-ttu-id="1c313-109">KB 4045801</span><span class="sxs-lookup"><span data-stu-id="1c313-109">KB 4045801</span></span>
        - <span data-ttu-id="1c313-110">KB 4091255</span><span class="sxs-lookup"><span data-stu-id="1c313-110">KB 4091255</span></span>

    - <span data-ttu-id="1c313-111">ターゲット環境でバージョン 1611 (2016 年 11 月、7.1 リリース) が実行されている場合は、次の更新プログラムを適用してください。</span><span class="sxs-lookup"><span data-stu-id="1c313-111">If the target environment runs version 1611 (November 2016, the 7.1 release), apply these updates:</span></span>

        - <span data-ttu-id="1c313-112">KB 4025631</span><span class="sxs-lookup"><span data-stu-id="1c313-112">KB 4025631</span></span>
        - <span data-ttu-id="1c313-113">KB 4035355</span><span class="sxs-lookup"><span data-stu-id="1c313-113">KB 4035355</span></span>
        - <span data-ttu-id="1c313-114">KB 4035492</span><span class="sxs-lookup"><span data-stu-id="1c313-114">KB 4035492</span></span>
        - <span data-ttu-id="1c313-115">KB 4010947</span><span class="sxs-lookup"><span data-stu-id="1c313-115">KB 4010947</span></span>

2. <span data-ttu-id="1c313-116">既定のチャネル データベースと既定のチャネル データ グループの名前はいずれも **既定** にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c313-116">Both the default channel database and the default channel data group must be named **Default**.</span></span> <span data-ttu-id="1c313-117">これらの名前を変更していた場合は、名前を元に戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c313-117">If you've renamed them, you must change the names back.</span></span>

<span data-ttu-id="1c313-118">以下の手順に従って、環境再プロビジョニング ツールを実行します。</span><span class="sxs-lookup"><span data-stu-id="1c313-118">Follow these steps to run the Environment reprovisioning tool.</span></span>

1. <span data-ttu-id="1c313-119">共有アセット ライブラリで、**ソフトウェア配置可能なパッケージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1c313-119">In the Shared asset library, select **Software deployable package**.</span></span>
2. <span data-ttu-id="1c313-120">環境再プロビジョニング ツールをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="1c313-120">Download the Environment reprovisioning tool.</span></span>
3. <span data-ttu-id="1c313-121">自身のプロジェクトのアセット ライブラリで、**ソフトウェア配置可能パッケージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1c313-121">In the asset library for your project, select **Software deployable package**.</span></span>
4. <span data-ttu-id="1c313-122">**新規作成** コマンドを選択して、新しいパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="1c313-122">Select **New** to create a new package.</span></span>
5. <span data-ttu-id="1c313-123">パッケージの名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c313-123">Enter a name and description for the package.</span></span> <span data-ttu-id="1c313-124">**環境再プロビジョニング ツール** をパッケージ名として使用できます。</span><span class="sxs-lookup"><span data-stu-id="1c313-124">You can use **Environment reprovisioning tool** as the package name.</span></span>
6. <span data-ttu-id="1c313-125">先ほどダウンロードしたパッケージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="1c313-125">Upload the package that you downloaded earlier.</span></span>
7. <span data-ttu-id="1c313-126">ターゲット環境の **環境の詳細** ページで、**管理** \> **更新プログラムを適用** を順に選択します。</span><span class="sxs-lookup"><span data-stu-id="1c313-126">On the **Environment details** page for your target environment, select **Maintain** \> **Apply updates**.</span></span>
8. <span data-ttu-id="1c313-127">先ほどアップロードした環境再プロビジョニング ツールを選択し、**適用** を選択してパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="1c313-127">Select the Environment reprovisioning tool that you uploaded earlier, and then select **Apply** to apply the package.</span></span>
9. <span data-ttu-id="1c313-128">パッケージの配置の進捗を監視します。</span><span class="sxs-lookup"><span data-stu-id="1c313-128">Monitor the progress of the package deployment.</span></span> 

<span data-ttu-id="1c313-129">配置可能パッケージを適用する方法の詳細については、[配置可能パッケージの適用](../deployment/create-apply-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c313-129">For more information about how to apply a deployable package, see [Apply a deployable package](../deployment/create-apply-deployable-package.md).</span></span> <span data-ttu-id="1c313-130">配置可能パッケージを手動で適用する方法の詳細については、[配置可能パッケージのインストール](../deployment/install-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c313-130">For more information about how to manually apply a deployable package, see [Install a deployable package](../deployment/install-deployable-package.md).</span></span>

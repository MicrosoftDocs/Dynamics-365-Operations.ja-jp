<span data-ttu-id="465bb-101">環境間でデータベースをコピーする場合、環境再プロビジョニング ツールを実行し、すべての Retail コンポーネントを最新の状態にしない限り、コピーしたデータベースは完全には機能しません。</span><span class="sxs-lookup"><span data-stu-id="465bb-101">If you copy a database between environments, the copied database won't be fully functional until you run the Environment reprovisioning tool to make sure that all Retail components are up to date.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="465bb-102">Retail の機能はすべての環境に含まれているため、Retail コンポーネントを使用しない場合も、この手順を完了しておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="465bb-102">We recommend that you complete this procedure even if you don't use Retail components, because Retail functionality is included in all environments.</span></span> 

<span data-ttu-id="465bb-103">続行する前に、次の前提条件が満たされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="465bb-103">Before you continue, you must make sure that the following prerequisites are met:</span></span>

1. <span data-ttu-id="465bb-104">適切な更新プログラムがターゲット環境に適用されています。</span><span class="sxs-lookup"><span data-stu-id="465bb-104">The appropriate updates are applied to the target environment:</span></span>

    - <span data-ttu-id="465bb-105">ターゲット環境で 7.3 リリース (2017 年 12 月) が実行されている場合は、次の更新プログラムを適用してください。</span><span class="sxs-lookup"><span data-stu-id="465bb-105">If the target environment runs the 7.3 release (December 2017), apply this update:</span></span>

        - <span data-ttu-id="465bb-106">KB 4091254</span><span class="sxs-lookup"><span data-stu-id="465bb-106">KB 4091254</span></span>

    - <span data-ttu-id="465bb-107">ターゲット環境で 7.2 リリース (2017 年 7 月) が実行されている場合は、次の更新プログラムを適用してください。</span><span class="sxs-lookup"><span data-stu-id="465bb-107">If the target environment runs the July 2017 release (7.2), apply these updates:</span></span>

        - <span data-ttu-id="465bb-108">KB 4035399</span><span class="sxs-lookup"><span data-stu-id="465bb-108">KB 4035399</span></span>
        - <span data-ttu-id="465bb-109">KB 4045801</span><span class="sxs-lookup"><span data-stu-id="465bb-109">KB 4045801</span></span>
        - <span data-ttu-id="465bb-110">KB 4091255</span><span class="sxs-lookup"><span data-stu-id="465bb-110">KB 4091255</span></span>

    - <span data-ttu-id="465bb-111">ターゲット環境でバージョン 1611 (2016 年 11 月、7.1 リリース) が実行されている場合は、次の更新プログラムを適用してください。</span><span class="sxs-lookup"><span data-stu-id="465bb-111">If the target environment runs version 1611 (November 2016, the 7.1 release), apply these updates:</span></span>

        - <span data-ttu-id="465bb-112">KB 4025631</span><span class="sxs-lookup"><span data-stu-id="465bb-112">KB 4025631</span></span>
        - <span data-ttu-id="465bb-113">KB 4035355</span><span class="sxs-lookup"><span data-stu-id="465bb-113">KB 4035355</span></span>
        - <span data-ttu-id="465bb-114">KB 4035492</span><span class="sxs-lookup"><span data-stu-id="465bb-114">KB 4035492</span></span>
        - <span data-ttu-id="465bb-115">KB 4010947</span><span class="sxs-lookup"><span data-stu-id="465bb-115">KB 4010947</span></span>

2. <span data-ttu-id="465bb-116">既定のチャネル データベースと既定のチャネル データ グループの名前は、いずれも **既定**にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="465bb-116">Both the default channel database and the default channel data group must be named **Default**.</span></span> <span data-ttu-id="465bb-117">これらの名前を変更していた場合は、名前を元に戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="465bb-117">If you've renamed them, you must change the names back.</span></span>

<span data-ttu-id="465bb-118">以下のステップに従って、環境再プロビジョニング ツールを実行します。</span><span class="sxs-lookup"><span data-stu-id="465bb-118">Follow these steps to run the Environment reprovisioning tool.</span></span>

1. <span data-ttu-id="465bb-119">**ソフトウェア配置可能パッケージ** セクションにある自身のプロジェクトの **資産ライブラリ** で、 **インポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="465bb-119">In your project's **Asset Library**, in the **Software deployable packages** section, click **Import**.</span></span>
2. <span data-ttu-id="465bb-120">共用資産の一覧から、 **環境再プロビジョニング ツール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="465bb-120">From the list of shared assets, select the **Environment Reprovisioning Tool**.</span></span>
3. <span data-ttu-id="465bb-121">ターゲット環境の **環境の詳細** ページで、 **管理** > **更新プログラムを適用**を順に選択します。</span><span class="sxs-lookup"><span data-stu-id="465bb-121">On the **Environment details** page for your target environment, select **Maintain** > **Apply updates**.</span></span>
4. <span data-ttu-id="465bb-122">先ほどアップロードした **環境再プロビジョニング** ツールを選択し、 **適用** を選択してパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="465bb-122">Select the **Environment Reprovisioning** tool that you uploaded earlier, and then select **Apply** to apply the package.</span></span>
5. <span data-ttu-id="465bb-123">パッケージの配置の進捗を監視します。</span><span class="sxs-lookup"><span data-stu-id="465bb-123">Monitor the progress of the package deployment.</span></span> 

<span data-ttu-id="465bb-124">配置可能パッケージを適用する方法の詳細については、 [配置可能パッケージの適用](../deployment/create-apply-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="465bb-124">For more information about how to apply a deployable package, see [Apply a deployable package](../deployment/create-apply-deployable-package.md).</span></span> <span data-ttu-id="465bb-125">配置可能パッケージを手動で適用する方法の詳細については、 [配置可能パッケージのインストール](../deployment/install-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="465bb-125">For more information about how to manually apply a deployable package, see [Install a deployable package](../deployment/install-deployable-package.md).</span></span>

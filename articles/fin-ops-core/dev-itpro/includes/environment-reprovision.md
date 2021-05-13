---
ms.openlocfilehash: eb5ecef9cb9b70e8395989ea271bdb717e573427
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920495"
---
> [!IMPORTANT]
> <span data-ttu-id="8bb0c-101">環境固有のレコードの中には、自動的なデータベース移動操作に含められないものがあり、その手順を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-101">Some environment-specific records are not included in automated database movement operations and require additional steps.</span></span> <span data-ttu-id="8bb0c-102">次のような役割があります。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-102">These include the following:</span></span>
> - <span data-ttu-id="8bb0c-103">Commerce セルフサービス インストーラー参照</span><span class="sxs-lookup"><span data-stu-id="8bb0c-103">Commerce self-service installer references</span></span>
> - <span data-ttu-id="8bb0c-104">Commerce Scale Unit チャネル データベースのコンフィギュレーション レコード</span><span class="sxs-lookup"><span data-stu-id="8bb0c-104">Commerce Scale Unit channel database configuration records</span></span>

<span data-ttu-id="8bb0c-105">環境間でデータベースをコピーすると、次の追加の手順を実行しない限り、移行先環境の Commerce の機能は完全には機能しません。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-105">If you copy a database between environments, Commerce capabilities in the destination environment will not be fully functional until you perform the following additional steps.</span></span>

### <a name="initialize-commerce-scale-units"></a><span data-ttu-id="8bb0c-106">Commerce Scale Unit の初期化</span><span class="sxs-lookup"><span data-stu-id="8bb0c-106">Initialize Commerce Scale Units</span></span>
<span data-ttu-id="8bb0c-107">データベースをサンドボックス UAT または実稼動環境に移動する場合は、データベースの移動操作が完了した後に、[Commerce Scale Unit を初期化](../deployment/Initialize-Retail-Channels.md)する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-107">If you are moving a database to a sandbox UAT or production environment, you must [Initialize Commerce Scale Unit](../deployment/Initialize-Retail-Channels.md) after the database movement operation is complete.</span></span> <span data-ttu-id="8bb0c-108">ソース環境からの Commerce Scale Unit の関連付けは、移行先の環境にコピーされません。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-108">The Commerce Scale Unit's association from the source environment will not copy over to the destination environment.</span></span> 

### <a name="synchronize-commerce-self-service-installers"></a><span data-ttu-id="8bb0c-109">Commerce のセルフサービス インストーラーの同期</span><span class="sxs-lookup"><span data-stu-id="8bb0c-109">Synchronize Commerce self-service installers</span></span>
<span data-ttu-id="8bb0c-110">HQ 内の Commerce セルフサービス インストーラーにアクセスできるようにするには、データベースの移動操作が完了した後に[セルフサービス インストーラーを同期](../../../commerce/dev-itpro/synchronize-installers.md)する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-110">To be able to access Commerce self-service installers in HQ, you must [Synchronize self-service installers](../../../commerce/dev-itpro/synchronize-installers.md) after the database movement operation is complete.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8bb0c-111">環境の再プロビジョニング手順は、データベース移動操作の一部として完全に自動化されており、これ以上手動で実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-111">The Environment re-provisioning step has now been fully automated as part of database movement operations, and no longer needs to be run manually.</span></span> <span data-ttu-id="8bb0c-112">環境の再プロビジョニング ツールはアセット ライブラリで引き続き使用でき、特定の状況でエラーの状態を軽減するために使用される場合もあります。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-112">The Environment re-provisioning tool is still available in the Asset Library and may be used in certain situations to mitigate error conditions.</span></span> 

<span data-ttu-id="8bb0c-113">移行先の環境で環境の再プロビジョニング ツールを実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-113">To run the Environment re-provisioning tool on the destination environment, run the following steps:</span></span>

1. <span data-ttu-id="8bb0c-114">**ソフトウェア配置可能パッケージ** セクションにある自身のプロジェクトの **アセット ライブラリ** で、 **インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-114">In your project's **Asset Library**, in the **Software deployable packages** section, select **Import**.</span></span>
2. <span data-ttu-id="8bb0c-115">共用資産の一覧から、 **環境再プロビジョニング ツール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-115">From the list of shared assets, select the **Environment Reprovisioning Tool**.</span></span>
3. <span data-ttu-id="8bb0c-116">移行先環境の **環境の詳細** ページで、 **管理** > **更新プログラムを適用** を順に選択します。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-116">On the **Environment details** page for your destination environment, select **Maintain** > **Apply updates**.</span></span>
4. <span data-ttu-id="8bb0c-117">先ほどアップロードした **環境再プロビジョニング** ツールを選択し、 **適用** を選択してパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-117">Select the **Environment Reprovisioning** tool that you uploaded earlier, and then select **Apply** to apply the package.</span></span>
5. <span data-ttu-id="8bb0c-118">パッケージの配置の進捗を監視します。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-118">Monitor the progress of the package deployment.</span></span>

<span data-ttu-id="8bb0c-119">配置可能なパッケージの適用方法についての詳細は、 [配置可能なパッケージを作成する](../deployment/create-apply-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-119">For more information about how to apply a deployable package, see [Create deployable packages of models](../deployment/create-apply-deployable-package.md).</span></span> <span data-ttu-id="8bb0c-120">配置可能パッケージを手動で適用する方法の詳細については、 [配置可能 な パッケージ を コマンド ライン から インストール する](../deployment/install-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-120">For more information about how to manually apply a deployable package, see [Install deployable packages from the command line](../deployment/install-deployable-package.md).</span></span>

### <a name="re-activate-pos-devices"></a><span data-ttu-id="8bb0c-121">POS デバイスの再アクティブ化</span><span class="sxs-lookup"><span data-stu-id="8bb0c-121">Re-activate POS devices</span></span>

<span data-ttu-id="8bb0c-122">販売時点管理 (POS) デバイスを使用する場合は、データベースをインポートした後に、POS デバイスを再度アクティブ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-122">If you use point of sale (POS) devices, after you import a database you must activate the POS devices again.</span></span> <span data-ttu-id="8bb0c-123">移行先環境で以前にアクティブ化されたデバイスは、機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-123">Previously activated devices in the destination environment will no longer function.</span></span> <span data-ttu-id="8bb0c-124">詳細については、[販売時点管理 (POS) デバイスのライセンス認証](../../../commerce/dev-itpro/retail-device-activation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bb0c-124">For more information, see [Point of sale device activation](../../../commerce/dev-itpro/retail-device-activation.md).</span></span>
---
ms.openlocfilehash: 4f954e14541c0a55ad1c77d1997b9515ab983ccc
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646121"
---
<span data-ttu-id="949df-101">サンドボックス **環境詳細** ページで、 **管理** メニューをクリックし、 **データベースの移動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="949df-101">From your sandbox **Environment Details** page, click the **Maintain** menu, and then select **Move database**.</span></span>

![データベース メニューの移動](../database/media/DBMovement_Menu.png)

<span data-ttu-id="949df-103">**エクスポート データベース** アクションが使用できるページでスライダー ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="949df-103">A slider pane will open on the page where you can use the **Export database** action.</span></span>

![データベース メニューのエクスポート](../database/media/Export_Menu.png)

<span data-ttu-id="949df-105">サンドボックスの更新やパッケージの展開などの他のサービス操作は、この間実行できません。</span><span class="sxs-lookup"><span data-stu-id="949df-105">The environment will be unavailable for other servicing operations, such as Sandbox refresh or package deployment during this time.</span></span> <span data-ttu-id="949df-106">ソース環境は Dynamics ユーザーの観点から使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="949df-106">The source environment will be usable from a Dynamics user perspective.</span></span>  

<span data-ttu-id="949df-107">エクスポートが正常に完了した後に、**環境の詳細** ページのサービス操作からサインアウトします。</span><span class="sxs-lookup"><span data-stu-id="949df-107">After the export operation completes successfully, sign out of the servicing operation on your **Environment details** page.</span></span> <span data-ttu-id="949df-108">**データベースのバックアップ** セクションの **資産ライブラリ** で資産を確認できます。</span><span class="sxs-lookup"><span data-stu-id="949df-108">You can then see the asset in your **Asset Library** in the **Database backups** section.</span></span>

![資産ライブラリのバックアップ ファイル](../database/media/AssetLibrary_Backups.png)

<span data-ttu-id="949df-110">**.bacpac** ファイルはここに格納され、インポート用 Tier 1 開発者環境に手動でダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="949df-110">The **.bacpac** files are stored here and can be manually downloaded to your Tier 1 developer environments for import.</span></span> <span data-ttu-id="949df-111">今後、Microsoft は、エクスポート アクションをトリガーし、資産ライブラリで使用可能なバックアップ ファイルを一覧表示するための API を提供します。</span><span class="sxs-lookup"><span data-stu-id="949df-111">In the future, Microsoft will provide APIs to trigger the export action, as well as list the available backup files in your asset library.</span></span> <span data-ttu-id="949df-112">これには、バックアップ資産ファイルを自動でダウンロードするための、または Microsoft Azure Storage SDK を使用して、セキュリティで保護された BLOB ストレージに直接コピーするための、セキュリティで保護された URL が含まれます。</span><span class="sxs-lookup"><span data-stu-id="949df-112">This includes the secured URL for automatically downloading a backup asset file or copying it directly to your secure blob storage using Microsoft Azure Storage SDKs.</span></span>

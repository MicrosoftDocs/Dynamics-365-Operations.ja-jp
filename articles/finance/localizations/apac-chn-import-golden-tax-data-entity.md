---
title: 中国金税データ エンティティのインポート
description: このトピックでは、中国金税データ エンティティを Microsoft Dynamics 365 Finance にインポートする方法について説明します。
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr
audience: IT Pro
ms.reviewer: kfend
ms.custom: 261394
ms.search.region: China (PRC)
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a3697caf1a75b327c84133cbd3cd41d22e0d5211
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894791"
---
# <a name="import-the-chinese-golden-tax-data-entity"></a><span data-ttu-id="10d5e-103">中国金税データ エンティティのインポート</span><span class="sxs-lookup"><span data-stu-id="10d5e-103">Import the Chinese Golden Tax data entity</span></span>

[!include [banner](../includes/banner.md)]
  
<span data-ttu-id="10d5e-104">このトピックでは、中国金税データ エンティティを Dynamics 365 Finance にインポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="10d5e-104">This topic explains how to import the Chinese Golden Tax data entity into Dynamics 365 Finance.</span></span>

> [!NOTE] 
> <span data-ttu-id="10d5e-105">Dynamics 365 Finance の10.0 以降のバージョンでは、中国金税データ エンティティをインポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="10d5e-105">You don't need to import the Chinese Golden Tax data entity for Dynamics 365 Finance version 10.0 and later.</span></span> 

<span data-ttu-id="10d5e-106">中国金税データ エンティティをインポートするには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="10d5e-106">To import the Chinese Golden Tax data entity, complete the following steps.</span></span>

1.  <span data-ttu-id="10d5e-107">**システム管理** &gt; **データ管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="10d5e-107">Go to **System administration** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="10d5e-108">**インポート** タイルをクリックして新しいインポート プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="10d5e-108">Click the **Import** tile to create a new import project.</span></span>
3.  <span data-ttu-id="10d5e-109">プロジェクトの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="10d5e-109">Enter a name for the project.</span></span>
4.  <span data-ttu-id="10d5e-110">ソース データ形式 **XML-Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="10d5e-110">Select the source data format **XML-Element**.</span></span>
5.  <span data-ttu-id="10d5e-111">**エンティティ名** フィールドで、**税の統合されたインポート** エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="10d5e-111">In the **Entity name** field, select **Tax integration import** entity.</span></span>
6.  <span data-ttu-id="10d5e-112">アップロードをクリックしてから、金税データ ファイルの場所を参照します。</span><span class="sxs-lookup"><span data-stu-id="10d5e-112">Click upload and then browse to the location of your golden tax data file.</span></span>
7.  <span data-ttu-id="10d5e-113">**マップの表示** を **税の統合されたインポート** タイルでクリックします。</span><span class="sxs-lookup"><span data-stu-id="10d5e-113">Click **View map** on the **Tax integration import** tile.</span></span>
8.  <span data-ttu-id="10d5e-114">**変換** タブで、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10d5e-114">On the **Transformations** tab, click **New**.</span></span>
9.  <span data-ttu-id="10d5e-115">**ファイルのアップロード** をクリックして .xlst ファイルの場所を参照します。</span><span class="sxs-lookup"><span data-stu-id="10d5e-115">Click **Upload file** and browse to the location of the .xlst file.</span></span>

<span data-ttu-id="10d5e-116">データ エンティティのインポート方法を示す特定の手順については、[エンティティを使用したデータのインポート](../../fin-ops-core/dev-itpro/data-entities/build-consuming-data-entities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="10d5e-116">For specific steps that show how to import a data entity, refer to [Importing data by using entities](../../fin-ops-core/dev-itpro/data-entities/build-consuming-data-entities.md).</span></span> <span data-ttu-id="10d5e-117">デモ データ会社 CNMF を使用して中国金税データ エンティティのインポートを実行するには、以下のファイルを [CustomerSource](/dynamics/s-e/) からダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="10d5e-117">To practice the Chinese Golden Tax data entity import using the demo data company CNMF, download the following files from [CustomerSource](/dynamics/s-e/).</span></span>

-   <span data-ttu-id="10d5e-118">**ImportSampleFile.xml** - このファイルは中国金税データ エンティティ複合です。</span><span class="sxs-lookup"><span data-stu-id="10d5e-118">**ImportSampleFile.xml** - This file is the Chinese Golden Tax data entity composite.</span></span>
-   <span data-ttu-id="10d5e-119">**Tax-Import-to-XML.xslt** - このファイルは変換ファイル マッピングとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="10d5e-119">**Tax-Import-to-XML.xslt** - This file is used as the transformational file mapping.</span></span>

<span data-ttu-id="10d5e-120">次のスクリーン ショットは、中国金税データ エンティティのマッピングのビジュアル化例を示します。</span><span class="sxs-lookup"><span data-stu-id="10d5e-120">The following screenshot shows an example mapping visualization for the Chinese Golden Tax data entity.</span></span> <span data-ttu-id="10d5e-121">[![この画像は中国金税データ エンティティのマッチングのビジュアル化例を示します。](./media/goldentaximportmappingvisualization.png)](./media/goldentaximportmappingvisualization.png)</span><span class="sxs-lookup"><span data-stu-id="10d5e-121">[![This image shows a sample mapping visualization for the Chinese Golden Tax data entity.](./media/goldentaximportmappingvisualization.png)](./media/goldentaximportmappingvisualization.png)</span></span>      

<span data-ttu-id="10d5e-122">詳細については、[金税統合エクスポートの設定](./tasks/golden-tax-integration-export-setup.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="10d5e-122">For more information, see [Golden tax integration export setup](./tasks/golden-tax-integration-export-setup.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
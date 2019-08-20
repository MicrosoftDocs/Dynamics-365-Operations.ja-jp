---
title: 中国金税データ エンティティのインポート
description: このトピックでは、中国金税データ エンティティを Microsoft Dynamics 365 for Finance and Operations にインポートする方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 261394
ms.search.region: China (PRC)
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dfde4faf1eea9356c482e6be4eaa4e353f4c8717
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850732"
---
# <a name="import-the-chinese-golden-tax-data-entity"></a><span data-ttu-id="aeb36-103">中国金税データ エンティティのインポート</span><span class="sxs-lookup"><span data-stu-id="aeb36-103">Import the Chinese Golden Tax data entity</span></span>

[!include [banner](../includes/banner.md)]
  
<span data-ttu-id="aeb36-104">このトピックでは、中国金税データ エンティティを Microsoft Dynamics 365 for Finance and Operations にインポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="aeb36-104">This topic explains how to import the Chinese Golden Tax data entity into Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="aeb36-105">Dynamics 365 for Finance and Operations の10.0以降のバージョンでは、中国で使用されている金税システムのデータ エンティティをインポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="aeb36-105">You don't need to import the Chiness Golden Tax data entity for Dynamics 365 for Finance and Operations version 10.0 and later.</span></span> 

<span data-ttu-id="aeb36-106">中国金税データ エンティティをインポートするには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="aeb36-106">To import the Chinese Golden Tax data entity, complete the following steps.</span></span>

1.  <span data-ttu-id="aeb36-107">**システム管理** &gt; **データ管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="aeb36-107">Go to **System administration** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="aeb36-108">**インポート** タイルをクリックして新しいインポート プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="aeb36-108">Click the **Import** tile to create a new import project.</span></span>
3.  <span data-ttu-id="aeb36-109">プロジェクトの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="aeb36-109">Enter a name for the project.</span></span>
4.  <span data-ttu-id="aeb36-110">ソース データ形式 **XML-Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="aeb36-110">Select the source data format **XML-Element**.</span></span>
5.  <span data-ttu-id="aeb36-111">**エンティティ名** フィールドで、**税の統合されたインポート** エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="aeb36-111">In the **Entity name** field, select **Tax integration import** entity.</span></span>
6.  <span data-ttu-id="aeb36-112">アップロードをクリックしてから、金税データ ファイルの場所を参照します。</span><span class="sxs-lookup"><span data-stu-id="aeb36-112">Click upload and then browse to the location of your golden tax data file.</span></span>
7.  <span data-ttu-id="aeb36-113">**マップの表示** を **税の統合されたインポート** タイルでクリックします。</span><span class="sxs-lookup"><span data-stu-id="aeb36-113">Click **View map** on the **Tax integration import** tile.</span></span>
8.  <span data-ttu-id="aeb36-114">**変換** タブで、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aeb36-114">On the **Transformations** tab, click **New**.</span></span>
9.  <span data-ttu-id="aeb36-115">**ファイルのアップロード** をクリックして .xlst ファイルの場所を参照します。</span><span class="sxs-lookup"><span data-stu-id="aeb36-115">Click **Upload file** and browse to the location of the .xlst file.</span></span>

<span data-ttu-id="aeb36-116">データ エンティティのインポート方法を示す特定の手順については、[エンティティを使用したデータのインポート](../../dev-itpro/data-entities/build-consuming-data-entities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aeb36-116">For specific steps that show how to import a data entity, refer to [Importing data by using entities](../../dev-itpro/data-entities/build-consuming-data-entities.md).</span></span> <span data-ttu-id="aeb36-117">デモ データ会社 CNMF を使用して中国金税データ エンティティのインポートを実行するには、以下のファイルを [CustomerSource](https://mbs.microsoft.com/customersource/global/ax/learning/samplefilestaximportchina) からダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="aeb36-117">To practice the Chinese Golden Tax data entity import using the demo data company CNMF, download the following files from [CustomerSource](https://mbs.microsoft.com/customersource/global/ax/learning/samplefilestaximportchina).</span></span>

-   <span data-ttu-id="aeb36-118">**ImportSampleFile.xml** - このファイルは中国金税データ エンティティ複合です。</span><span class="sxs-lookup"><span data-stu-id="aeb36-118">**ImportSampleFile.xml** - This file is the Chinese Golden Tax data entity composite.</span></span>
-   <span data-ttu-id="aeb36-119">**Tax-Import-to-XML.xslt** - このファイルは変換ファイル マッピングとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="aeb36-119">**Tax-Import-to-XML.xslt** - This file is used as the transformational file mapping.</span></span>

<span data-ttu-id="aeb36-120">次のスクリーン ショットは、中国金税データ エンティティのマッピングのビジュアル化例を示します。</span><span class="sxs-lookup"><span data-stu-id="aeb36-120">The following screenshot shows an example mapping visualization for the Chinese Golden Tax data entity.</span></span> <span data-ttu-id="aeb36-121">[![この画像は中国金税データ エンティティのマッチングのビジュアル化例を示します。](./media/goldentaximportmappingvisualization.png)](./media/goldentaximportmappingvisualization.png)</span><span class="sxs-lookup"><span data-stu-id="aeb36-121">[![This image shows a sample mapping visualization for the Chinese Golden Tax data entity.](./media/goldentaximportmappingvisualization.png)](./media/goldentaximportmappingvisualization.png)</span></span>      

<span data-ttu-id="aeb36-122">詳細については、[金税統合エクスポートの設定](./tasks/golden-tax-integration-export-setup.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aeb36-122">For more information, see [Golden tax integration export setup](./tasks/golden-tax-integration-export-setup.md).</span></span>


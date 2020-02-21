---
title: Application update 7.3 での ER フレームワーク API の変更
description: このトピックでは、Dynamics 365 for Finance and Operations、Enterprise Edition のアプリケーション更新プログラム 7.3 での電子申告 (ER) フレームワークの API における変更について説明します。
author: NickSelin
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 7b5e9223281c276a8228238de5ab455dcb626fcd
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025868"
---
# <a name="er-framework-api-changes-for-application-update-73"></a><span data-ttu-id="d092c-103">Application update 7.3 での ER フレームワーク API の変更</span><span class="sxs-lookup"><span data-stu-id="d092c-103">ER framework API changes for Application update 7.3</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d092c-104">このトピックでは、Dynamics 365 for Finance and Operations、Enterprise Edition のアプリケーション更新プログラム 7.3 での電子申告 (ER) フレームワークの API における変更について説明します。</span><span class="sxs-lookup"><span data-stu-id="d092c-104">This topic describes how the API of the Electronic reporting (ER) framework has been changed in the Dynamics 365 for Finance and Operations, Enterprise edition Application update 7.3.</span></span>

<span data-ttu-id="d092c-105">ER API には 2 つのタイプの変更があります。</span><span class="sxs-lookup"><span data-stu-id="d092c-105">There are two types of changes to the ER APIs:</span></span>

- <span data-ttu-id="d092c-106">いくつかの X++ クラスが外部アセンブリに X++ から移行されました。</span><span class="sxs-lookup"><span data-stu-id="d092c-106">Several X++ classes were moved from X++ to an external assembly.</span></span>
- <span data-ttu-id="d092c-107">X++ クラスの残りの部分は、内部としてマークされています。</span><span class="sxs-lookup"><span data-stu-id="d092c-107">The rest of X++ classes were marked as internal.</span></span>

## <a name="how-to-access-classes-that-were-moved-from-x-to-an-external-assembly"></a><span data-ttu-id="d092c-108">外部アセンブリに X++ から移行されたクラスへのアクセス方法</span><span class="sxs-lookup"><span data-stu-id="d092c-108">How to access classes that were moved from X++ to an external assembly</span></span>

<span data-ttu-id="d092c-109">外部クラスにアクセスするには、ファイルの先頭に **using** ディレクティブを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d092c-109">To access external classes, you need to add the **using** directive to the beginning of your file.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
```

<span data-ttu-id="d092c-110">たとえば、追加の変更をせずに外部クラスにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="d092c-110">You can then access an external class without any additional changes, for example.</span></span>

```xpp
var destination = new ERFileDestinationMemory();
```

<span data-ttu-id="d092c-111">名前空間のエイリアスを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="d092c-111">You can also create an alias for your namespace.</span></span>

```xpp
using LF = Microsoft.Dynamics365.LocalizationFramework;
```

<span data-ttu-id="d092c-112">作成した名前空間のエイリアスを使用して、外部のクラスを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="d092c-112">You can then refer to an external class by using the namespace alias that you created.</span></span>

```xpp
var destination = new LF.ERFileDestinationMemory();
```

## <a name="how-to-access-internal-x-objects-by-using-erobjectsfactory"></a><span data-ttu-id="d092c-113">ERObjectsFactory を使用して内部 X++ オブジェクトにアクセスする方法</span><span class="sxs-lookup"><span data-stu-id="d092c-113">How to access internal X++ objects by using ERObjectsFactory</span></span>

<span data-ttu-id="d092c-114">アプリケーションの更新プログラム 7.3 以降では、呼び出し元のコードは **ERObjectsFactory** クラスのメソッドを使用して ER オブジェクトにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d092c-114">In Application update 7.3 and later updates, the calling code must access the ER objects by using the methods of the **ERObjectsFactory** class.</span></span> <span data-ttu-id="d092c-115">これらの変更の例をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="d092c-115">Several examples of these changes are shown.</span></span>

### <a name="code-to-display-a-format-mapping-lookup"></a><span data-ttu-id="d092c-116">フォーマット マッピング ルックアップを表示するコード</span><span class="sxs-lookup"><span data-stu-id="d092c-116">Code to display a format mapping lookup</span></span>

<span data-ttu-id="d092c-117">アプリケーション 更新 7.3 より前</span><span class="sxs-lookup"><span data-stu-id="d092c-117">Before Application update 7.3</span></span>

```xpp
// pattern
ERFormatMappingTableLookup::lookupFormatMapping(<form control>, <model name>[, <data container name>]);
// sample code
ERFormatMappingTableLookup::lookupFormatMapping(_referenceGroupControl, bankLCMiscChargeReportERModelName);
```

<span data-ttu-id="d092c-118">アプリケーション更新プログラム 7.3 以降</span><span class="sxs-lookup"><span data-stu-id="d092c-118">Application update 7.3 and later</span></span>

```xpp
// pattern
ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(<form control>, <model name>[, <data container name>]).performFormLookup();
// sample code
ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(_referenceGroupControl, bankLCMiscChargeReportERModelName).performFormLookup();
```

### <a name="code-to-run-a-format-mapping-for-data-export"></a><span data-ttu-id="d092c-119">データ エクスポート用のフォーマット マッピングを実行するためのコード</span><span class="sxs-lookup"><span data-stu-id="d092c-119">Code to run a format mapping for data export</span></span>

<span data-ttu-id="d092c-120">アプリケーション 更新 7.3 より前</span><span class="sxs-lookup"><span data-stu-id="d092c-120">Before Application update 7.3</span></span>

```xpp
// pattern
ERFormatMappingRun::constructByFormatMappingId(<format mapping id>, <file name>, <show prompt dialog>).run();
// sample code
ERFormatMappingRun::constructByFormatMappingId(erBinding, '', true).run();
```

<span data-ttu-id="d092c-121">アプリケーション更新プログラム 7.3 以降</span><span class="sxs-lookup"><span data-stu-id="d092c-121">Application update 7.3 and later</span></span>

```xpp
// pattern
ERObjectsFactory::createFormatMappingRunByFormatMappingId(<format mapping id>, <file name>, <show prompt dialog>).run();
// sample code
ERObjectsFactory::createFormatMappingRunByFormatMappingId(erBinding, '', true).run();
```

### <a name="code-to-run-a-format-mapping-for-data-import"></a><span data-ttu-id="d092c-122">データ インポート用の形式マッピングを実行するためのコード</span><span class="sxs-lookup"><span data-stu-id="d092c-122">Code to run a format mapping for data import</span></span>

<span data-ttu-id="d092c-123">アプリケーション 更新 7.3 より前</span><span class="sxs-lookup"><span data-stu-id="d092c-123">Before Application update 7.3</span></span>

```xpp
// pattern
ERModelMappingDestinationRun::constructByImportFormatMappingId(<mapping id>, <integration point>).run();
// sample code
ERModelMappingDestinationRun::constructByImportFormatMappingId(custPaymModeTable.ERModelMappingTable, CustVendOutPaymConstants::IntegrationPoint).run();
```

<span data-ttu-id="d092c-124">アプリケーション更新プログラム 7.3 以降</span><span class="sxs-lookup"><span data-stu-id="d092c-124">Application update 7.3 and later</span></span>

```xpp
// pattern
ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId(<mapping id>, <integration point>).run();
// sample code
ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId(custPaymModeTable.ERModelMappingTable, CustVendOutPaymConstants::IntegrationPoint).run();
```

### <a name="code-to-create-a-browser-file-destination"></a><span data-ttu-id="d092c-125">ブラウザー ファイルの宛先を作成するためのコード</span><span class="sxs-lookup"><span data-stu-id="d092c-125">Code to create a browser file destination</span></span>

<span data-ttu-id="d092c-126">アプリケーション 更新 7.3 より前</span><span class="sxs-lookup"><span data-stu-id="d092c-126">Before Application update 7.3</span></span>

```xpp
// sample code
new ERFileDestinationBrowser();
```

<span data-ttu-id="d092c-127">アプリケーション更新プログラム 7.3 以降</span><span class="sxs-lookup"><span data-stu-id="d092c-127">Application update 7.3 and later</span></span>

```xpp
// sample code
ERObjectsFactory::createFileDestinationBrowser();
```

### <a name="code-to-create-an-attachment-file-destination"></a><span data-ttu-id="d092c-128">添付ファイルの宛先を作成するためのコード</span><span class="sxs-lookup"><span data-stu-id="d092c-128">Code to create an attachment file destination</span></span>

<span data-ttu-id="d092c-129">アプリケーション 更新 7.3 より前</span><span class="sxs-lookup"><span data-stu-id="d092c-129">Before Application update 7.3</span></span>

```xpp
// pattern
ERFileDestinationAttachment::construct(<record>, ERDocuManagement::instance().otherDocuType());
// sample code
ERFileDestinationAttachment::construct(_cashRegisterFiscalTrans_W, ERDocuManagement::instance().otherDocuType());
```

<span data-ttu-id="d092c-130">アプリケーション更新プログラム 7.3 以降</span><span class="sxs-lookup"><span data-stu-id="d092c-130">Application update 7.3 and later</span></span>

```xpp
// pattern
ERObjectsFactory::createFileDestinationAttachmentWithOtherDocuType(<record>);
// sample code
ERObjectsFactory::createFileDestinationAttachmentWithOtherDocuType(_cashRegisterFiscalTrans_W);
```

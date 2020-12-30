---
title: Power Apps および Power Automate を使用した Talent の拡張
description: この記事では、Microsoft Power Apps および Microsoft Power Automate を使用する Microsoft Dynamics 365 Human Resources の拡張性シナリオのいくつかの例を説明します。
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2e89347829ccd6569d568db42c79b5fea2316ba3
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527029"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="3b372-103">Power Apps および Power Automate を使用した拡張</span><span class="sxs-lookup"><span data-stu-id="3b372-103">Extend with Power Apps and Power Automate</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3b372-104">この記事では、Microsoft Power Apps および Microsoft Power Automate を使用する Microsoft Dynamics 365 Human Resources の拡張性シナリオのいくつかの例を説明します。</span><span class="sxs-lookup"><span data-stu-id="3b372-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="3b372-105">各例に関連付けられているソリューション パッケージを Power Apps 環境にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="3b372-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="3b372-106">次に、そのパッケージをガイダンスもしくは組織に適用できるシナリオを実装するための開始点として使用できます。</span><span class="sxs-lookup"><span data-stu-id="3b372-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b372-107">このトピックで説明されているテンプレートおよびアプリを「そのまま」使用する場合は、それらをテストして、実装に固有のすべてのシナリオをカバーしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="3b372-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3b372-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="3b372-108">Prerequisites</span></span>

- <span data-ttu-id="3b372-109">パッケージをインポートするには、ユーザーは **環境メーカー** のアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="3b372-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="3b372-110">アプリをエクスポートまたはインポートするには、Power Apps プラン 2 ライセンスもしくは Power Apps プラン 2 試用版ライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="3b372-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="3b372-111">Microsoft 365, Power Automate との統合</span><span class="sxs-lookup"><span data-stu-id="3b372-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="3b372-112">**Microsoft 365 との統合** アプリを使用すると、Microsoft 365 からサインイン ユーザーのチーム情報を抽出できます。</span><span class="sxs-lookup"><span data-stu-id="3b372-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="3b372-113">従業員 ID タイプを抽出するために、人事管理の従業員が照会されます。</span><span class="sxs-lookup"><span data-stu-id="3b372-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="3b372-114">マネージャーは従業員 ID タイプの有効期限を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="3b372-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="3b372-115">またマネージャーは、従業員 ID タイプが期限切れになる場合に電子メールの通知を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="3b372-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="3b372-116">Power Automate と Power Apps 統合し、このアラームを送信します。</span><span class="sxs-lookup"><span data-stu-id="3b372-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="3b372-117">アラームが送信されると、Power Automate から Power Apps に確認が送り返されます。</span><span class="sxs-lookup"><span data-stu-id="3b372-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="3b372-118">ID タイプには、運転免許証、パスポート、およびその他受け入れ可能な ID の形式が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3b372-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="3b372-119">このアプリは他のシナリオのために拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="3b372-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="3b372-120">たとえば、チームの休暇情報、カレンダーのイベント、およびそのチーム固有のイベントを表示するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="3b372-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="3b372-121">**Microsoft 365, Power Automate との統合** アプリをダウンロードするには、Microsoft ダウンロード センターの [Microsoft 365 との統合](https://go.microsoft.com/fwlink/?linkid=2081787) に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b372-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="3b372-122">Power Automate – SQL 接続と実行</span><span class="sxs-lookup"><span data-stu-id="3b372-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="3b372-123">**Power Automate – SQL 接続と実行** テンプレートを Microsoft SQL Server に接続し、SQL クエリを実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="3b372-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="3b372-124">このテンプレートは SQL テーブルを読み取り更新しますが、それを拡張して他のシナリオに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="3b372-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="3b372-125">たとえば、Common Data Service のステージング テーブルに SQL Server のレコードを入力したり、SQL Server からの増分プッシュを使用してステージング テーブルを定期的に同期するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="3b372-125">For example, you can use it to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="3b372-126">データ変換と増分プッシュを有効化するために、高度なクエリがフローに統合されています。</span><span class="sxs-lookup"><span data-stu-id="3b372-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="3b372-127">**Power Automate – SQL 接続と実行** テンプレートをダウンロードするには、Microsoft ダウンロード センターの [Power Automate – SQL 接続と実行](https://go.microsoft.com/fwlink/?linkid=2081789) に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b372-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b372-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3b372-128">Additional resources</span></span>

[<span data-ttu-id="3b372-129">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="3b372-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
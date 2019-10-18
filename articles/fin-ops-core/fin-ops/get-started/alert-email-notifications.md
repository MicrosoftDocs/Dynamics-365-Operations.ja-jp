---
title: 電子メールによるクライアント警告通知
description: このトピックでは、定義済のイベントが発生する電子メール通知を送信するルールを設定する方法について説明します。
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: ba92c3dc1debed7e98210168d1a135e2cf567aec
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191296"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="c6b96-103">電子メールによるクライアント警告通知</span><span class="sxs-lookup"><span data-stu-id="c6b96-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c6b96-104">データのフィルター処理されたビューを監視し、定義済のイベントが発生した場合に、電子メール通知を自動的に送信するカスタム警告ルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="c6b96-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="c6b96-105">電子メール通知を送信するオプションは、サポートされているすべての警告タイプで使用可能であり、既存の警告ルールでも有効にできます。</span><span class="sxs-lookup"><span data-stu-id="c6b96-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="c6b96-106">組み込みのコントロールを使用して、システム バッチ ジョブのフィルタ処理されたビューを監視する警告ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c6b96-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="c6b96-107">**ステータス**フィールドの値を監視することで、バッチ ジョブが失敗したときに電子メールを送信する警告ルールも設定できます。</span><span class="sxs-lookup"><span data-stu-id="c6b96-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="c6b96-108">これらの警告ルールを作成した後は、ビジネス データへの変更についてレポートを確認する必要はなくなりました。</span><span class="sxs-lookup"><span data-stu-id="c6b96-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="c6b96-109">代わりに、インテリジェントな変更検出サービスに監視させることができます。</span><span class="sxs-lookup"><span data-stu-id="c6b96-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="c6b96-110">クライアントの警告は、Microsoft Office との統合を通じて提供される電子メール サブシステムによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c6b96-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="c6b96-111">電子メールの配信がローカル メール クライアントに依存する必要がないように、Simple Mail Transfer Protocol (SMTP) プロバイダーを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c6b96-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="c6b96-112">電子メールで通知を送信するには、顧客が統合電子メール サービスをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6b96-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="c6b96-113">電子メール通知は、警告の所有者に代わって受信者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="c6b96-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="c6b96-114">電子メールをコンフィギュレーションする方法の詳細については、[電子メールのコンフィギュレーションと送信](../organization-administration/configure-email.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="c6b96-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="c6b96-115">次の図は、**電子メールの送信**オプションを含む**警告ルールの作成**ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="c6b96-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="c6b96-116">[![ 電子メールの送信オプションがはいに設定されている警告ルールの作成ダイアログ ボックス](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="c6b96-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="c6b96-117">**電子メールの送信**オプションが**はい**に設定されている場合、警告通知はアクション センターから配信され続けます。</span><span class="sxs-lookup"><span data-stu-id="c6b96-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="c6b96-118">警告通知用電子メール テンプレート</span><span class="sxs-lookup"><span data-stu-id="c6b96-118">Alert notification email templates</span></span>

<span data-ttu-id="c6b96-119">このサービスは、警告通知の基本詳細情報を配信する定義済の電子メール テンプレートを使用して、電子メール通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="c6b96-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="c6b96-120">次の図は、電子メールで受信された時の警告通知の構造を表示します。</span><span class="sxs-lookup"><span data-stu-id="c6b96-120">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="c6b96-121">[![レコードの作成、フィールドの変更、およびテンプレート削除のためのテンプレートに基づく警告通知](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="c6b96-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>

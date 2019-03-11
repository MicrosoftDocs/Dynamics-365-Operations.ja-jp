---
title: ビジネス イベントのトラブルシューティング
description: このトピックでは、ビジネス イベントのトラブルシューティングについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 02/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: Platform update 24
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: 968a1a36f04a59b4cbfe4a157e320955e746e82f
ms.sourcegitcommit: 7e0097bdd835e04521bffbce2fd802e6381dde0d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2019
ms.locfileid: "376931"
---
# <a name="troubleshoot-business-events"></a><span data-ttu-id="86f18-103">ビジネス イベントのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="86f18-103">Troubleshoot business events</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="86f18-104">このトピックでは、ビジネス イベントに関する問題を解決するためのヒントをいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="86f18-104">This topic provides some tips for troubleshooting issues that involve business events.</span></span>

<span data-ttu-id="86f18-105">**エラー: エンドポイントを作成できません。例外メッセージ: キー コンテナー「https://[KeyVaultName].vault.azure.net/」からのシークレット「[KeyValueSecretName]」を取得中にエラーが発生しました。AADSTS700016: 識別子を持つアプリケーション「7e28cb03-dc28-43b5-b129-e13dcfb4b1fb」は、ディレクトリ 「ee3fe5c6-26af-42b1-9acf-5ee38e6ead6e」で見つかりませんでした。**</span><span class="sxs-lookup"><span data-stu-id="86f18-105">**Error: Unable to construct endpoint. Exception message: Error retrieving secret '[KeyValueSecretName]' from key vault 'https://[KeyVaultName].vault.azure.net/': AADSTS700016: Application with identifier '7e28cb03-dc28-43b5-b129-e13dcfb4b1fb' was not found in the directory 'ee3fe5c6-26af-42b1-9acf-5ee38e6ead6e'.**</span></span> 

<span data-ttu-id="86f18-106">これは、アプリケーションがテナントの管理者によってインストールされていないか、テナントのユーザーによって同意されていない場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="86f18-106">This can happen if the application has not been installed by the administrator of the tenant or consented to by any user in the tenant.</span></span> <span data-ttu-id="86f18-107">認証要求を間違ったテナントに送信した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="86f18-107">It's likely that you may have sent your authentication request to the wrong tenant.</span></span>

<span data-ttu-id="86f18-108">**エラー: 追跡 ID: 19dc9946-45b6-4335-9676-6a133dbf4000 相関関係 ID: ecbc8a80-f9d0-41ec-9c8f-d334d050bd64 タイムスタンプ : 2019-02-06 23:27:06Z**</span><span class="sxs-lookup"><span data-stu-id="86f18-108">**Error: Trace ID: 19dc9946-45b6-4335-9676-6a133dbf4000 Correlation ID: ecbc8a80-f9d0-41ec-9c8f-d334d050bd64 Timestamp: 2019-02-06 23:27:06Z**</span></span>

<span data-ttu-id="86f18-109">このエラーは、**Azure Active Directory アプリケーション ID** フィールドの値が正しくないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="86f18-109">This error typically means that the value in the **Azure Active Directory Application ID** field is incorrect.</span></span> <span data-ttu-id="86f18-110">顧客の Azure ポータルの **Azure Active Directory アプリケーション ID** の値を **Azure Active Directory > アプリケーションの登録**で確認します。</span><span class="sxs-lookup"><span data-stu-id="86f18-110">Check the **Azure Active Directory Application ID** value in the customers Azure portal in **Azure Active Directory > App Registration**.</span></span>

<span data-ttu-id="86f18-111">**エラー: エンドポイントを作成できません。例外メッセージ: キー コンテナー「https://[KeyVaultName].vault.azure.net/」からシークレット「[KeyValueSecretName]」を取得中にエラーが発生しました。要求の送信中にエラーが発生しました。**</span><span class="sxs-lookup"><span data-stu-id="86f18-111">**Error: Unable to construct endpoint. Exception message: Error retrieving secret '[KeyValueSecretName]' from key vault 'https://[KeyVaultName].vault.azure.net/': An error occurred while sending the request.**</span></span>

<span data-ttu-id="86f18-112">このエラーは、**Key Vault DNS Name** フィールドの値が正しくないことが原因です。</span><span class="sxs-lookup"><span data-stu-id="86f18-112">This error is likely due to an incorrect value in the **Key Vault DNS Name** field.</span></span> <span data-ttu-id="86f18-113">これを解決するには、顧客の Azure ポータルに移動して、キー コンテナーのオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="86f18-113">To resolve this, go to the customer's Azure portal and open the key vault object.</span></span> <span data-ttu-id="86f18-114">**概要**セクションで、**Key Vault DNS 名**値を確認します。</span><span class="sxs-lookup"><span data-stu-id="86f18-114">In the **Overview** section, check the **Key Vault DNS Name** value.</span></span>

<span data-ttu-id="86f18-115">**エラー: テスト イベントをエンドポイントに送信することができません。例外メッセージ: 40103: 無効な認証トークンの署名、リソース: sb://[ServiceBusName]. servicebus.windows.net/[QueueName]。TrackingId:cd0eccaa-1717-4f97-b837-4cd7eda99af4_G13、SystemTracker:[ServiceBusName]. servicebus.windows.net:[QueueName]、Timestamp:2019-02-06T23:36:54**</span><span class="sxs-lookup"><span data-stu-id="86f18-115">**Error: Unable to send test event to endpoint. Exception message: 40103: Invalid authorization token signature, Resource:sb://[ServiceBusName].servicebus.windows.net/[QueueName]. TrackingId:cd0eccaa-1717-4f97-b837-4cd7eda99af4_G13, SystemTracker:[ServiceBusName].servicebus.windows.net:[QueueName], Timestamp:2019-02-06T23:36:54**</span></span>

<span data-ttu-id="86f18-116">顧客の Key Vault シークレットの値が予想が正しくない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="86f18-116">The value in the customer’s Key Vault Secret is likely incorrect.</span></span> <span data-ttu-id="86f18-117">**Key Vault シークレット**の値を確認し、エンドポイントのタイプが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="86f18-117">Check the **Key Vault Secret** value and make sure that it is correct for the endpoint type.</span></span>

<span data-ttu-id="86f18-118">**エラー: エンドポイントを作成できません。例外メッセージ: key vault 「https://[KeyVaultName].vault.azure.net/」からシークレット「[KeyValueSecretName]」を取得中にエラーが発生しました。アクセスが拒否されました。**</span><span class="sxs-lookup"><span data-stu-id="86f18-118">**Error:Unable to construct endpoint. Exception message: Error retrieving secret '[KeyValueSecretName]' from key vault 'https://[KeyVaultName].vault.azure.net/': Access denied**</span></span>

<span data-ttu-id="86f18-119">**Azure Active Directory アプリケーション ID** に Key Vault での適切なアクセス許可がない可能性あります。</span><span class="sxs-lookup"><span data-stu-id="86f18-119">This is likely due to the **Azure Active Directory Application ID** not having the appropriate permissions in the Key Vault.</span></span> <span data-ttu-id="86f18-120">これを解決するには、Azure ポータルに移動して、**Key Vault** のオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="86f18-120">To resolve this, go to the Azure portal and open the **Key Vault** object.</span></span> <span data-ttu-id="86f18-121">**アクセス ポリシー**に移動し、キー、シークレット、および証明書の管理テンプレートを使用して、AAD アプリケーションを追加します。</span><span class="sxs-lookup"><span data-stu-id="86f18-121">Go to **Access Policies** and add the AAD application with Key, Secret, and Certificate Management template.</span></span>

<span data-ttu-id="86f18-122">**エラー: テスト イベントをエンドポイントに送信することができません。例外メッセージ: 40400: エンドポイントが見つかりません。リソース: sb://[ServiceBusName].servicebus.windows.net/[QueueName].**</span><span class="sxs-lookup"><span data-stu-id="86f18-122">**Error: Unable to send test event to endpoint. Exception message: 40400: Endpoint not found., Resource:sb://[ServiceBusName].servicebus.windows.net/[QueueName].**</span></span>

<span data-ttu-id="86f18-123">この問題は、キュー/トピック/ハブ名が正しくないことが原因です。</span><span class="sxs-lookup"><span data-stu-id="86f18-123">This issue is likely a result of the queue/topic/hub name being incorrect.</span></span> <span data-ttu-id="86f18-124">Azure ポータルのサービス バスにアクセスし、**名**フィールドを確認し、**トピック**または**キュー**名を確認します。</span><span class="sxs-lookup"><span data-stu-id="86f18-124">Check the **Name** field by going to service bus in the Azure portal and reviewing the **Topic** or **Queue** name.</span></span> <span data-ttu-id="86f18-125">イベント ハブである場合、Azure の**イベント ハブ**オブジェクトに移動し、**ハブ**名を検証します。</span><span class="sxs-lookup"><span data-stu-id="86f18-125">If it is an Event Hub, go to the **Event Hub** object in Azure and validate the **Hub** name.</span></span>

<span data-ttu-id="86f18-126">**エラー: テスト イベントをエンドポイントに送信することができません。例外メッセージ: 要求の送信中にエラーが発生しました。**</span><span class="sxs-lookup"><span data-stu-id="86f18-126">**Error: Unable to send test event to endpoint. Exception message: An error occurred while sending the request.**</span></span>

<span data-ttu-id="86f18-127">**エンドポイント URL** フィールドのエンドポイントの指定された値が正しくない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="86f18-127">This is likely due to an incorrect endpoint value specified in the **Endpoint URL** field.</span></span> <span data-ttu-id="86f18-128">Azure ポータルの**イベント グリッド**オブジェクトに移動し、**イベント グリッド**を開きます。</span><span class="sxs-lookup"><span data-stu-id="86f18-128">Go to the **Event Grid** object in the Azure portal and open the **Event Grid**.</span></span> <span data-ttu-id="86f18-129">**概要**セクションで、この値が**トピック エンドポイント**になります。</span><span class="sxs-lookup"><span data-stu-id="86f18-129">In the **Overview** section, this value will be the **Topic Endpoint**.</span></span>

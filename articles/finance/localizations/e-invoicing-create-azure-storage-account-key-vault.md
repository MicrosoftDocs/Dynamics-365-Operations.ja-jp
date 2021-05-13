---
title: Azure ストレージ アカウントとキー コンテナーの作成
description: このトピックでは、Azure ストレージ アカウントとキー コンテナーを作成する方法について説明します。
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 5c2ddad10f9cbedd77a04fe0f42bdc217fd43344
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963242"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="f78e9-103">Azure ストレージ アカウントとキー コンテナーの作成</span><span class="sxs-lookup"><span data-stu-id="f78e9-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="f78e9-104">必要条件</span><span class="sxs-lookup"><span data-stu-id="f78e9-104">Prerequisites</span></span>

<span data-ttu-id="f78e9-105">このトピックのタスクを完了する前に、以下の前提条件を完了していることを確認してください :</span><span class="sxs-lookup"><span data-stu-id="f78e9-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="f78e9-106">Azure でのキー コンテナーのリソースの作成。</span><span class="sxs-lookup"><span data-stu-id="f78e9-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="f78e9-107">詳細については、[Azure のキー コンテナー](/azure/key-vault/general/overview)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f78e9-107">For more information, see [About Azure Key Vault](/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="f78e9-108">Azure ストレージ アカウント (Blob ストレージ) の作成。</span><span class="sxs-lookup"><span data-stu-id="f78e9-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="f78e9-109">詳細については、[Azure ストレージ アカウントを管理する](/azure/storage/blobs/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f78e9-109">For more information, see [Maintaining Azure Storage Account](/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="f78e9-110">概要</span><span class="sxs-lookup"><span data-stu-id="f78e9-110">Overview</span></span>

<span data-ttu-id="f78e9-111">このトピックでは、2 つの主要な手順について説明します :</span><span class="sxs-lookup"><span data-stu-id="f78e9-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="f78e9-112">Azure のストレージ アカウントを設定してストレージ アカウントの URI を取得します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="f78e9-113">キーコンテナーを設定し、ストレージ アカウントの URI を格納します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="f78e9-114">Azure のストレージ アカウントを設定してストレージ アカウントの URI を取得する</span><span class="sxs-lookup"><span data-stu-id="f78e9-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="f78e9-115">電子請求に使用する予定のストレージ アカウントを開きます。</span><span class="sxs-lookup"><span data-stu-id="f78e9-115">Open the storage account that you plan to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="f78e9-116">**Blob サービス** \> **コンテナー** に移動 し、新しいコンテナーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="f78e9-117">コンテナーの名前を入力し、**パブリック アクセス レベル** フィールドを **プライベート (匿名アクセスなし)** に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="f78e9-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="f78e9-118">コンテナーを開き、 **設定 \> アクセス ポリシー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="f78e9-119">**ポリシーの追加** を選択して、保存されているアクセス ポリシーを追加します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="f78e9-120">必要に応じて、 **識別子** フィールドと **アクセス許可** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="f78e9-121">**キーのアクセス許可** フィールドで、すべてのアクセス許可を選択します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Blob ストレージのアクセス許可を付与する](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="f78e9-123">開始日と有効期限を入力します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="f78e9-124">有効期限は未来の日付にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f78e9-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="f78e9-125">**OK** をクリックしてポリシーを保存し、変更をコンテナーに保存します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="f78e9-126">ストレージ アカウントに戻り、**記憶域エクスプローラー (プレビュー)** を開きます。</span><span class="sxs-lookup"><span data-stu-id="f78e9-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="f78e9-127">コンテナーを右クリックし、**共有アクセス署名の取得** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="f78e9-128">**共有アクセス署名** ダイアログ ボックスで、**URI** フィールドに値をコピーして格納します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="f78e9-129">この値は、次の手順で使用され、*共有アクセス署名 URI* として参照されます。</span><span class="sxs-lookup"><span data-stu-id="f78e9-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![URI 値の選択とコピー](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="f78e9-131">キー コンテナーを設定し、ストレージ アカウントの URI を格納する</span><span class="sxs-lookup"><span data-stu-id="f78e9-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="f78e9-132">電子請求に使用する Key Vault を開きます。</span><span class="sxs-lookup"><span data-stu-id="f78e9-132">Open the key vault that you intend to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="f78e9-133">**設定** \> **秘密** に移動し、**生成/インポート** を選択して 新しい秘密を作成します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="f78e9-134">**シークレットを作成** ページの **アップロード オプション** フィールドで、**手動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="f78e9-135">秘密の名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-135">Enter the name of the secret.</span></span> <span data-ttu-id="f78e9-136">この名前は、Regulatory Configuration Services (RCS) のサービス設定時に使用され、*キー コンテナーの秘密名称* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="f78e9-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="f78e9-137">**値** フィールドで、**共有アクセス署名 URI** を選択し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="f78e9-138">アクセス ポリシーを設定して、作成したシークレットへの正しいレベルのセキュアなアクセスを電子請求に付与します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-138">Set up the access policy to grant Electronic invoicing the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="f78e9-139">**設定 \>アクセス ポリシー** に移動し 、**アクセス ポリシーの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="f78e9-140">**取得** と **一覧** の操作に、秘密のアクセス許可を設定します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![サービス アクセスの付与](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="f78e9-142">**取得** と **一覧** の操作に、証明書のアクセス許可を設定します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![証明書のアクセス許可の付与](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="f78e9-144">**プリンシパルの選択** フィールドで、**選択なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="f78e9-145">**プリンシパル** ダイアログ ボックスで、**電子請求書サービス** を追加してプリンシパルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="f78e9-146">**追加** を選択し、**キー コンテナーの変更を保存する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="f78e9-147">**概要** ページで、 キー コンテナーの **DNS 名** の値をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="f78e9-148">この値は、RCS におけるサービスの設定時に使用され、*キー コンテナーの URI* として参照されます。</span><span class="sxs-lookup"><span data-stu-id="f78e9-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>

> [!NOTE]
> <span data-ttu-id="f78e9-149">ストレージ アカウントのセキュリティを追加するには、Azure Defender For Storage を構成します。</span><span class="sxs-lookup"><span data-stu-id="f78e9-149">For additional security on the storage account, configure the Azure Defender for Storage.</span></span>
> 
> <span data-ttu-id="f78e9-150">詳細については、[Azure Defender for Storage の概要](/azure/security-center/defender-for-storage-introduction) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f78e9-150">For more information, see [Introduction to Azure Defender for Storage](/azure/security-center/defender-for-storage-introduction).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

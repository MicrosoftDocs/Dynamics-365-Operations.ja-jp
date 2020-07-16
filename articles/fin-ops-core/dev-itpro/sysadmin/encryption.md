---
title: Finance and Operations アプリにおける暗号化処理
description: このトピックでは、環境の SQL Server データベースと Azure ストレージに格納されている、休眠している顧客データの保護に使用される暗号化技術について説明します。
author: nedb
manager: ''
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21631
ms.search.region: Global
ms.author: nedb
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 536c1b5c5c31e44c293c347dc5118b39227ba74a
ms.sourcegitcommit: 497e07d7e42541f9e707495ab334cf2185b70e4e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454947"
---
# <a name="encryption-in-finance-and-operations-apps"></a><span data-ttu-id="4f090-103">Finance and Operations アプリにおける暗号化処理</span><span class="sxs-lookup"><span data-stu-id="4f090-103">Encryption in Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

## <a name="encryption-at-rest"></a><span data-ttu-id="4f090-104">休眠データの暗号化</span><span class="sxs-lookup"><span data-stu-id="4f090-104">Encryption at rest</span></span>

<span data-ttu-id="4f090-105">Microsoft は、環境の SQL Server データベースと Azure ストレージに格納されている、休眠している顧客データを保護する目的で暗号化技術を使用しています。</span><span class="sxs-lookup"><span data-stu-id="4f090-105">Microsoft uses encryption technology to protect customer data while at rest in an environment's SQL Server database and Azure Storage.</span></span>

<span data-ttu-id="4f090-106">すべてのインスタンスは、[Microsoft SQL Server Transparent Data Encryption (TDE) ](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption)と [Azure ストレージ暗号化](https://docs.microsoft.com/azure/storage/common/storage-service-encryption) を使用して、ディスクに書き込まれる休眠データをリアルタイムで暗号化しています。</span><span class="sxs-lookup"><span data-stu-id="4f090-106">All instances utilize [Microsoft SQL Server Transparent Data Encryption (TDE)](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption) and [Azure Storage encryption](https://docs.microsoft.com/azure/storage/common/storage-service-encryption) to perform real-time encryption of data when written to the disk at rest.</span></span> 

<span data-ttu-id="4f090-107">Finance and Operations アプリでは、サービス管理キーを使用してサーバーサイドの暗号化を使用します。</span><span class="sxs-lookup"><span data-stu-id="4f090-107">Finance and Operations apps use server-side encryption using service-managed keys.</span></span> <span data-ttu-id="4f090-108">キーの発行、ローテーション、バックアップなどのキーに関する管理は、Microsoft が処理します。</span><span class="sxs-lookup"><span data-stu-id="4f090-108">All key management aspects such as key issuance, rotation, and backup are handled by Microsoft.</span></span>

<span data-ttu-id="4f090-109">上記の既定の暗号化に加えて、**グローバル** X + + クラスで使用可能な暗号化APIを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f090-109">In addition to the default encryption at rest provided above, you can use the encryption API available in the **Global** X++ class.</span></span> <span data-ttu-id="4f090-110">**グローバル ::editencryptedfield ()** メソッド と **global ::editencryptedfield ()** メソッドは、環境固有のデータ暗号化証明書を使用して、データの暗号化と復号化を行います。</span><span class="sxs-lookup"><span data-stu-id="4f090-110">The methods **Global::editEncryptedField()** and **Global::editEncryptedStringField()** use the environment-specific data encryption certificate to perform data encryption and decryption.</span></span> <span data-ttu-id="4f090-111">これらの方法は、データ ストレージに使用される既定の暗号化技術を超える、追加の保護層として使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f090-111">You can use these methods as an additional layer of protection beyond the default encryption at rest technology used for data storage.</span></span>

## <a name="encryption-in-transit"></a><span data-ttu-id="4f090-112">転送時の暗号化</span><span class="sxs-lookup"><span data-stu-id="4f090-112">Encryption in transit</span></span>

<span data-ttu-id="4f090-113">顧客と Microsoft データセンターの間で確立される接続は暗号化されており、業界標準のトランスポート層セキュリティ (TLS) 1.2 を使用して、すべてのパブリック エンドポイントが保護されます。</span><span class="sxs-lookup"><span data-stu-id="4f090-113">Connections established between customers and Microsoft datacenters are encrypted, and all public endpoints are secured using industry-standard Transport Layer Security (TLS) 1.2.</span></span> <span data-ttu-id="4f090-114">TLSは、セキュリティを強化したブラウザとサーバー間の接続を効果的に確立し、デスクトップとデータセンター間のデータの機密性と完全性を効果的に確保します。</span><span class="sxs-lookup"><span data-stu-id="4f090-114">TLS effectively establishes a security-enhanced browser-to-server connection to help ensure data confidentiality and integrity between desktops and datacenters.</span></span> 

### <a name="supported-tls-versions"></a><span data-ttu-id="4f090-115">対応している TLS のバージョン</span><span class="sxs-lookup"><span data-stu-id="4f090-115">Supported TLS versions</span></span>

<span data-ttu-id="4f090-116">Finance and Operations アプリは TLS 1.2 のみに対応しています。</span><span class="sxs-lookup"><span data-stu-id="4f090-116">Finance and Operations apps support TLS 1.2 only.</span></span> <span data-ttu-id="4f090-117">TLS の古いバージョンである 1.0 と 1.1 には対応していません。</span><span class="sxs-lookup"><span data-stu-id="4f090-117">Earlier TLS versions, 1.0 and 1.1, are not supported.</span></span>

### <a name="supported-cipher-suites"></a><span data-ttu-id="4f090-118">対応している暗号スイート</span><span class="sxs-lookup"><span data-stu-id="4f090-118">Supported cipher suites</span></span>

<span data-ttu-id="4f090-119">Finance and Operations アプリは以下の暗号スイートにのに対応しています。</span><span class="sxs-lookup"><span data-stu-id="4f090-119">Finance and Operations apps only support the following cipher suites:</span></span>

* <span data-ttu-id="4f090-120">TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384</span><span class="sxs-lookup"><span data-stu-id="4f090-120">TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384</span></span>
* <span data-ttu-id="4f090-121">TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256</span><span class="sxs-lookup"><span data-stu-id="4f090-121">TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256</span></span>
* <span data-ttu-id="4f090-122">TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384</span><span class="sxs-lookup"><span data-stu-id="4f090-122">TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384</span></span>
* <span data-ttu-id="4f090-123">TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256</span><span class="sxs-lookup"><span data-stu-id="4f090-123">TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256</span></span>
* <span data-ttu-id="4f090-124">TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384</span><span class="sxs-lookup"><span data-stu-id="4f090-124">TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384</span></span>
* <span data-ttu-id="4f090-125">TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256</span><span class="sxs-lookup"><span data-stu-id="4f090-125">TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256</span></span>
* <span data-ttu-id="4f090-126">TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384</span><span class="sxs-lookup"><span data-stu-id="4f090-126">TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384</span></span>
* <span data-ttu-id="4f090-127">TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256</span><span class="sxs-lookup"><span data-stu-id="4f090-127">TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f090-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4f090-128">Additional resources</span></span>

* [<span data-ttu-id="4f090-129">Azure 休眠データの暗号化</span><span class="sxs-lookup"><span data-stu-id="4f090-129">Azure Data Encryption-at-Rest</span></span>](https://docs.microsoft.com/azure/security/fundamentals/encryption-atrest)
* [<span data-ttu-id="4f090-130">Microsoft SQL Server透過データの暗号化 (TDE)</span><span class="sxs-lookup"><span data-stu-id="4f090-130">Microsoft SQL Server Transparent Data Encryption (TDE)</span></span>](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption)
* [<span data-ttu-id="4f090-131">Azure ストレージの暗号化</span><span class="sxs-lookup"><span data-stu-id="4f090-131">Azure Storage encryption</span></span>](https://docs.microsoft.com/azure/storage/common/storage-service-encryption)
* [<span data-ttu-id="4f090-132">開発のための内部者向けヒント</span><span class="sxs-lookup"><span data-stu-id="4f090-132">Insider tips on development</span></span>](https://community.dynamics.com/ax/b/newdynamicsax)
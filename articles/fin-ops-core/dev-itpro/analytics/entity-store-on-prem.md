---
title: PowerBI.comとオンプレミス環境との統合
description: このトピックでは、 オンプレミス配置にてエンティティストアを有効にする方法を提供します。
author: MilindaV
manager: AnnBe
ms.date: 06/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EntityStoreOnPrem
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27661
ms.assetid: 861cfa94-c6f3-4c84-89ac-22c78bf6b7a4
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2019-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 00e5ae5c07c25fbf4cb8e79a4875bf5a2e710e16
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183396"
---
# <a name="powerbicom-integration-with-on-premises-environments"></a><span data-ttu-id="026da-103">オンプレミス環境との PowerBI.com の統合</span><span class="sxs-lookup"><span data-stu-id="026da-103">PowerBI.com integration with on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="026da-104">クラウド版では、Microsoft Power BI との緊密な統合を可能にするいくつかの機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="026da-104">The cloud version provides several features that allow for deeper integration with Microsoft Power BI.</span></span> <span data-ttu-id="026da-105">いくつかの機能は、オンプレミスの配置用にはまだ実装されていません。</span><span class="sxs-lookup"><span data-stu-id="026da-105">Some of these features haven't yet been implemented for on-premises deployments.</span></span> <span data-ttu-id="026da-106">ただし、オンプレミス配置でのエンティティ格納を利用することで、PowerBI.com を使って Finance and Operations のデータのレポートや分析ができるようになっています。</span><span class="sxs-lookup"><span data-stu-id="026da-106">However, the availability of Entity Store in on-premises deployments lets customers use PowerBI.com to report on and analyze data.</span></span> 

<span data-ttu-id="026da-107">このトピックでは、 Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム26 (2019年5月)以降にて動作する、オンプレミス配置で使用できる分析機能について概説します。</span><span class="sxs-lookup"><span data-stu-id="026da-107">This topic outlines the analytical capabilities that are available in on-premises deployments that run Microsoft Dynamics 365 for Finance and Operations platform update 26 (May 2019) and later.</span></span>

| <span data-ttu-id="026da-108">特性/機能</span><span class="sxs-lookup"><span data-stu-id="026da-108">Feature/capability</span></span>                                                           | <span data-ttu-id="026da-109">クラウド</span><span class="sxs-lookup"><span data-stu-id="026da-109">Cloud</span></span>     | <span data-ttu-id="026da-110">オンプレミス (プラットフォーム更新プログラム 26 またはそれ以降)</span><span class="sxs-lookup"><span data-stu-id="026da-110">On-premises (Platform update 26 or later)</span></span> |
|------------------------------------------------------------------------------|-----------|-------------------------------------------|
| <span data-ttu-id="026da-111">分析ワークスペース</span><span class="sxs-lookup"><span data-stu-id="026da-111">Analytical workspaces</span></span>                                                        | <span data-ttu-id="026da-112">利用可</span><span class="sxs-lookup"><span data-stu-id="026da-112">Available</span></span> | <span data-ttu-id="026da-113">**まだ実装されていません**</span><span class="sxs-lookup"><span data-stu-id="026da-113">**Not yet implemented**</span></span><p><span data-ttu-id="026da-114">Entity Store上で構築されたレポートは、PowerBI.comと一緒に使うことができます。</span><span class="sxs-lookup"><span data-stu-id="026da-114">Customers can use the reports that are built on Entity Store together with PowerBI.com.</span></span></p> |
| <span data-ttu-id="026da-115">PowerBI.com からレポート、タイル、およびダッシュボードをクライアントに固定することができます。</span><span class="sxs-lookup"><span data-stu-id="026da-115">Pin reports, tiles, and dashboards from PowerBI.com into the client.</span></span>         | <span data-ttu-id="026da-116">利用可</span><span class="sxs-lookup"><span data-stu-id="026da-116">Available</span></span> | <span data-ttu-id="026da-117">**まだ実装されていません**</span><span class="sxs-lookup"><span data-stu-id="026da-117">**Not yet implemented**</span></span> |
| <span data-ttu-id="026da-118">アプリケーションのデータを使用した Power BI のレポートを作成および配布します。</span><span class="sxs-lookup"><span data-stu-id="026da-118">Author and distribute Power BI reports that use application data.</span></span> | <span data-ttu-id="026da-119">使用可能</span><span class="sxs-lookup"><span data-stu-id="026da-119">Available</span></span> | <span data-ttu-id="026da-120">**使用可能**</span><span class="sxs-lookup"><span data-stu-id="026da-120">**Available**</span></span><p><span data-ttu-id="026da-121">オンプレミスでエンティティストアを使用することで、既製のレポートを変更したり、新しいレポートを作成をすることができます。</span><span class="sxs-lookup"><span data-stu-id="026da-121">Customers can modify ready-made reports and create new reports by using Entity Store on-premises.</span></span></p> |
| <span data-ttu-id="026da-122">アプリケーション データをデータ ウェアハウスに抽出します。</span><span class="sxs-lookup"><span data-stu-id="026da-122">Extract application data into data warehouses.</span></span>                    | <span data-ttu-id="026da-123">使用可能</span><span class="sxs-lookup"><span data-stu-id="026da-123">Available</span></span> | <span data-ttu-id="026da-124">**使用可能**</span><span class="sxs-lookup"><span data-stu-id="026da-124">**Available**</span></span> |

## <a name="enable-entity-store-on-premises"></a><span data-ttu-id="026da-125">エンティティストアをオンプレミスにて有効化する</span><span class="sxs-lookup"><span data-stu-id="026da-125">Enable Entity Store on-premises</span></span>

<span data-ttu-id="026da-126">このトピックでは [、オンプレミス環境の設定および配置](../deployment/setup-deploy-on-premises-pu12.md) についてのトピックを補足します。</span><span class="sxs-lookup"><span data-stu-id="026da-126">This topic supplements the [Set up and deploy on-premises environments](../deployment/setup-deploy-on-premises-pu12.md) topic.</span></span> <span data-ttu-id="026da-127">以下のセクション番号は、該当するトピックのセクション番号に対応しています。</span><span class="sxs-lookup"><span data-stu-id="026da-127">The section numbers that follow correspond to the section numbers in that topic.</span></span>

### <a name="3-plan-your-users-and-service-accountsdeploymentsetup-deploy-on-premises-pu12mdplansvcacct"></a>[<span data-ttu-id="026da-128">3. ユーザーとサービスのアカウントを準備する</span><span class="sxs-lookup"><span data-stu-id="026da-128">3. Plan your users and service accounts</span></span>](../deployment/setup-deploy-on-premises-pu12.md#plansvcacct)

| <span data-ttu-id="026da-129">ユーザー アカウント</span><span class="sxs-lookup"><span data-stu-id="026da-129">User account</span></span>               | <span data-ttu-id="026da-130">型</span><span class="sxs-lookup"><span data-stu-id="026da-130">Type</span></span>     | <span data-ttu-id="026da-131">目的</span><span class="sxs-lookup"><span data-stu-id="026da-131">Purpose</span></span> | <span data-ttu-id="026da-132">ユーザー名</span><span class="sxs-lookup"><span data-stu-id="026da-132">User name</span></span> |
|----------------------------|----------|---------|-----------|
| <span data-ttu-id="026da-133">AOS SQL AXDW DB 管理者 ユーザー</span><span class="sxs-lookup"><span data-stu-id="026da-133">AOS SQL AXDW DB Admin user</span></span> | <span data-ttu-id="026da-134">SQL ユーザー</span><span class="sxs-lookup"><span data-stu-id="026da-134">SQL user</span></span> | <span data-ttu-id="026da-135">アプリケーションは、このユーザーを使用して AXDW データベースに情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="026da-135">The application uses this user to enter information in the AXDW database.</span></span> <span data-ttu-id="026da-136">このユーザーは任意であり、エンティティストアに対応する必要がある場合にのみ作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="026da-136">This user is optional and must be created only if you want Entity Store support.</span></span> | <span data-ttu-id="026da-137">axdwadmin</span><span class="sxs-lookup"><span data-stu-id="026da-137">axdwadmin</span></span> |
| <span data-ttu-id="026da-138">AOS SQL AXDW FB 管理者 ユーザー</span><span class="sxs-lookup"><span data-stu-id="026da-138">AOS SQL AXDW FB Admin user</span></span> | <span data-ttu-id="026da-139">SQL ユーザー</span><span class="sxs-lookup"><span data-stu-id="026da-139">SQL user</span></span> | <span data-ttu-id="026da-140">アプリケーションは、このユーザーを使用して AXDW データベースに情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="026da-140">The application uses this user to enter information in the AXDW database.</span></span> <span data-ttu-id="026da-141">このユーザーは任意であり、エンティティストアに対応する必要がある場合にのみ作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="026da-141">This user is optional and must be created only if you want Entity Store support.</span></span> | <span data-ttu-id="026da-142">axdwruntimeuser</span><span class="sxs-lookup"><span data-stu-id="026da-142">axdwruntimeuser</span></span> |

### <a name="14-configure-the-databasesdeploymentsetup-deploy-on-premises-pu12mdconfiguredb"></a>[<span data-ttu-id="026da-143">14. データベースの環境設定</span><span class="sxs-lookup"><span data-stu-id="026da-143">14. Configure the databases</span></span>](../deployment/setup-deploy-on-premises-pu12.md#configuredb)

<span data-ttu-id="026da-144">本セクションの以下手順は任意の設定です。</span><span class="sxs-lookup"><span data-stu-id="026da-144">The steps in this section are optional.</span></span>

<span data-ttu-id="026da-145">エンティティストアに使用するデータベースを作成する場合は、最初に ConfigTemplate .xml ファイルを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="026da-145">If you want to create a database that can be used for Entity Store, you must first modify the ConfigTemplate.xml file.</span></span>

1. <span data-ttu-id="026da-146">**DbServer - セキュリティ**で、 **axdwadmin** および **axdwruntimeuser** の **generateuser** フラグを **True**に設定します。</span><span class="sxs-lookup"><span data-stu-id="026da-146">Under **DbServer – Security**, set the **generateUser** flags for **axdwadmin** and **axdwruntimeuser** to **True**.</span></span> <span data-ttu-id="026da-147">次の手順のスクリプトを実行すると、2つのユーザーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="026da-147">The scripts that you run in the next step will then create those two users.</span></span> <span data-ttu-id="026da-148">ユーザーのパスワードを設定するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="026da-148">You will be prompted to set passwords for the users.</span></span>
2. <span data-ttu-id="026da-149">次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="026da-149">Run the following scripts.</span></span>

        .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EntityStore
        .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EntityStore

    <span data-ttu-id="026da-150">Initialize-Database.ps1 スクリプトは、以下の処理を行います:</span><span class="sxs-lookup"><span data-stu-id="026da-150">The Initialize-Database.ps1 script performs the following actions:</span></span>

    - <span data-ttu-id="026da-151">**AXDW** という名前の空のデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="026da-151">Create an empty database that is named **AXDW**.</span></span> <span data-ttu-id="026da-152">このデータベースは、エンティティストアに使用されます。</span><span class="sxs-lookup"><span data-stu-id="026da-152">This database is used for Entity Store.</span></span>
    - <span data-ttu-id="026da-153">SQL認証が有効となった **Axdwadmin** という名前の新規ユーザーが作成され、パスワードの設定が求められます。</span><span class="sxs-lookup"><span data-stu-id="026da-153">Create a new user that is named **axdwadmin** and that has SQL authentication enabled, and prompt you for the user's password.</span></span>
    - <span data-ttu-id="026da-154">SQL認証が有効となった **axdwruntimeuser** という名前の新規ユーザーが作成され、パスワードの設定が求められます。</span><span class="sxs-lookup"><span data-stu-id="026da-154">Create a new user that is named **axdwruntimeuser** and that has SQL authentication enabled, and prompt you for the user's password.</span></span>
    - <span data-ttu-id="026da-155">axdwadmin と axdwruntimeuser に対して、データベースへの **データベース\_所有者** 権限を付与します。</span><span class="sxs-lookup"><span data-stu-id="026da-155">Grant the axdwadmin and axdwruntimeuser users **db\_owner** permissions on the database.</span></span>

    <span data-ttu-id="026da-156">Configure-Database.ps1 スクリプトは、以下の処理を行います:</span><span class="sxs-lookup"><span data-stu-id="026da-156">The Configure-Database.ps1 script performs the following actions:</span></span>

    - <span data-ttu-id="026da-157">指定したデータベースファイル と ログの設定を行います。</span><span class="sxs-lookup"><span data-stu-id="026da-157">Set the specified database file and log settings.</span></span>
    - <span data-ttu-id="026da-158">VIEW SERVER STATE 権限を axdbadmin に付与します。</span><span class="sxs-lookup"><span data-stu-id="026da-158">GRANT VIEW SERVER STATE TO axdwadmin.</span></span>
    - <span data-ttu-id="026da-159">VIEW SERVER STATE 権限を axdwruntimeuser に付与します。</span><span class="sxs-lookup"><span data-stu-id="026da-159">GRANT VIEW SERVER STATE TO axdwruntimeuser.</span></span>

### <a name="15-encrypt-credentialsdeploymentsetup-deploy-on-premises-pu12mdencryptcred"></a>[<span data-ttu-id="026da-160">15. 資格情報の暗号化</span><span class="sxs-lookup"><span data-stu-id="026da-160">15. Encrypt credentials</span></span>](../deployment/setup-deploy-on-premises-pu12.md#encryptcred)

<span data-ttu-id="026da-161">以下のように、Credentials.json ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="026da-161">Create a Credentials.json file as shown here.</span></span> <span data-ttu-id="026da-162">**AosDWAuth** カテゴリは任意であり、エンティティストアが有効な場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="026da-162">The **AosDWAuth** category is optional and is used only if Entity Store is enabled.</span></span>

    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        },
        "AosDWAuth": {
            "DWUser": "<encryptedDWUser>",
            "DWPwd": "<encryptedDWPassword>",
            "DWRuntimeUser": "<encryptedDWRuntimeUser>",
            "DWRuntimePwd": "<encryptedDWRuntimePassword>"
        }
    }

<span data-ttu-id="026da-163">上記のコマンドの内容について説明します:</span><span class="sxs-lookup"><span data-stu-id="026da-163">Here is an explanation of the preceding code lines:</span></span>

- <span data-ttu-id="026da-164">**AccountPassword** は、Application Object Server (AOS) ドメインユーザー (contoso\\axserviceuser) 用の暗号化されたドメイン ユーザー パスワードです。</span><span class="sxs-lookup"><span data-stu-id="026da-164">**AccountPassword** is the encrypted domain user password for the Application Object Server (AOS) domain user (contoso\\axserviceuser).</span></span>
- <span data-ttu-id="026da-165">**SqlUser** は、アプリケーション データベース (AXDB) にアクセス権限が付与されている暗号化された SQL ユーザー (axdbadmin) です。</span><span class="sxs-lookup"><span data-stu-id="026da-165">**SqlUser** is the encrypted SQL user (axdbadmin) that has access to the application database (AXDB).</span></span> <span data-ttu-id="026da-166">**SqlPwd** は暗号化されたSQLパスワードです。</span><span class="sxs-lookup"><span data-stu-id="026da-166">**SqlPwd** is the encrypted SQL password.</span></span>
- <span data-ttu-id="026da-167">**DWUser** は、エンティティストア データベース (axdw) へのアクセス権限が付与されている、暗号化されたSQLユーザー (axdwadmin) です。</span><span class="sxs-lookup"><span data-stu-id="026da-167">**DWUser** is the encrypted SQL user (axdwadmin) that has access to the Entity Store database (AXDW).</span></span> <span data-ttu-id="026da-168">**DWPwd** は、Initialize-Database.ps1 スクリプトの実行時に入力される暗号化されたSQLパスワードです。</span><span class="sxs-lookup"><span data-stu-id="026da-168">**DWPwd** is the encrypted SQL password that is entered when the Initialize-Database.ps1 script is run.</span></span>
- <span data-ttu-id="026da-169">**DWRuntimeUser** は、エンティティストア データベース (AXDW) へのアクセス権限が付与されている、暗号化されたSQLユーザー (axdwruntimeuser) です。</span><span class="sxs-lookup"><span data-stu-id="026da-169">**DWRuntimeUser** is the encrypted SQL user (axdwruntimeuser) that has access to the Entity Store database (AXDW).</span></span> <span data-ttu-id="026da-170">**DWRuntimePwd** は、Initialize-Database.ps1 スクリプトの実行時に入力される暗号化されたSQLパスワードです。</span><span class="sxs-lookup"><span data-stu-id="026da-170">**DWRuntimePwd** is the encrypted SQL password that is entered when the Initialize-Database.ps1 script is run.</span></span>

## <a name="more-information"></a><span data-ttu-id="026da-171">詳細情報</span><span class="sxs-lookup"><span data-stu-id="026da-171">More information</span></span>

<span data-ttu-id="026da-172">エンティティストアは、プラットフォーム更新プログラム 26で有効となっています。</span><span class="sxs-lookup"><span data-stu-id="026da-172">Entity Store was enabled in Platform update 26.</span></span>

<span data-ttu-id="026da-173">エンティティストアを行うデータベースとユーザーの作成は任意です。</span><span class="sxs-lookup"><span data-stu-id="026da-173">Creation of the Entity Store database and users is optional.</span></span> <span data-ttu-id="026da-174">Microsoft Dynamics Lifecycle Services (LCS)で配置の構成を行う際には、エンティティストアのカスタマイズを空白のままにしておくことができます。</span><span class="sxs-lookup"><span data-stu-id="026da-174">When you configure a deployment in Microsoft Dynamics Lifecycle Services (LCS), you can leave the Entity Store customizations blank.</span></span>

<span data-ttu-id="026da-175">エンティティストアを環境内で有効にする必要がある場合は、以下のタスクを完了する必要があります:</span><span class="sxs-lookup"><span data-stu-id="026da-175">If Entity Store should be enabled in an environment, the following tasks must be completed:</span></span>

- <span data-ttu-id="026da-176">手順14に記載のスクリプトを使用することで、 **AXDW** データベースを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="026da-176">Create an **AXDW** database by using the scripts that are described in step 14.</span></span>
- <span data-ttu-id="026da-177">手順14に記載のスクリプトを使用することで、適切な権限を持つ **axdwadmin** と **axdwruntimeuser** ユーザーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="026da-177">Create **axdwadmin** and **axdwruntimeuser** users that have appropriate privileges, by using the scripts in that are described step 14.</span></span> <span data-ttu-id="026da-178">ユーザーは次のファイルで定義されています: ConfigTemplate.xml、DatabaseTopologyDefinition.xml</span><span class="sxs-lookup"><span data-stu-id="026da-178">Users are defined in the following files: ConfigTemplate.xml and DatabaseTopologyDefinition.xml.</span></span>
- <span data-ttu-id="026da-179">手順15に記載の **Credentials.json** ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="026da-179">Create a **Credentials.json** file as described in step 15.</span></span> <span data-ttu-id="026da-180">手順14に記載されているように、ユーザー名とパスワードは、axdwadminおよびaxdwruntimeuserに対して定義する必要があり、暗号化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="026da-180">User names and passwords should be defined for axdwadmin and axdwruntimeuser as described in step 14, and they should be encrypted.</span></span>
- <span data-ttu-id="026da-181">エンティティストアを行うSQL Serverの名称および、データベースの名称は、LCSへの配置差処理中に設定される必要があります。</span><span class="sxs-lookup"><span data-stu-id="026da-181">The Entity Store SQL Server name and Entity Store database name must be filled in during deployment in LCS.</span></span>

    - <span data-ttu-id="026da-182">データベースの名称は手順14で作成され、DatabaseTopologyDefinitionファイルにて定義されています。</span><span class="sxs-lookup"><span data-stu-id="026da-182">The database name is created in step 14 and is defined in the DatabaseTopologyDefinition.xml file.</span></span> <span data-ttu-id="026da-183">既定の名称は **AXDW** です。</span><span class="sxs-lookup"><span data-stu-id="026da-183">The default name is **AXDW**.</span></span>
    - <span data-ttu-id="026da-184">SQL Serverの名称は、 Microsoft SQL Server またはAlwaysOnリスナー の完全修飾ドメイン名 (FQDN) となります。</span><span class="sxs-lookup"><span data-stu-id="026da-184">The SQL Server name is the fully qualified domain name (FQDN) of the Microsoft SQL Server or Always on listener.</span></span> <span data-ttu-id="026da-185">このFQDNの例としては、 **sqlinstance.onprem.contoso.com** があります。</span><span class="sxs-lookup"><span data-stu-id="026da-185">An example of this FQDN is **sqlinstance.onprem.contoso.com**.</span></span> <span data-ttu-id="026da-186">これはAXDWデータベースが作成されたサーバーです。</span><span class="sxs-lookup"><span data-stu-id="026da-186">It's the server that the AXDW database is created on.</span></span>

<span data-ttu-id="026da-187">現在のところ、エンティティストアの有効化は最初の配置処理中にのみ行うことができます。</span><span class="sxs-lookup"><span data-stu-id="026da-187">Currently, you can enable Entity Store only during initial deployment.</span></span> <span data-ttu-id="026da-188">既存の環境で有効にする必要がある場合は、エンティティストアに対応しているプラットフォームの更新を使用して、当該環境を削除したのちに再度配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="026da-188">If it must be enabled in an existing environment, that environment must be deleted and then deployed again by using a platform update that supports Entity Store.</span></span>

## <a name="authoring-and-distributing-reports-by-using-entity-store-on-premises"></a><span data-ttu-id="026da-189">エンティティストア オンプレミスを使用したレポートの作成および配布</span><span class="sxs-lookup"><span data-stu-id="026da-189">Authoring and distributing reports by using Entity Store on-premises</span></span>

<span data-ttu-id="026da-190">エンティティ格納は、含まれている運用データ ウェアハウスです。</span><span class="sxs-lookup"><span data-stu-id="026da-190">Entity Store is an operational data warehouse that is included.</span></span> <span data-ttu-id="026da-191">これにより、パワー ユーザーやビジネス アナリストは、シンプルで豊富なデータを使用したレポートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="026da-191">It lets power users and business analysts author reports that use simplified and enriched data.</span></span> <span data-ttu-id="026da-192">エンティティストアには集計測定値が含まれており、単純化されたスタースキーマを使用できます。</span><span class="sxs-lookup"><span data-stu-id="026da-192">Entity Store contains aggregate measurements, which are simplified star schemas.</span></span> <span data-ttu-id="026da-193">エンティティストアを使用してレポートを作成する方法の詳細については、 [ Power BI Desktopを使用して分析レポートを作成する](author-distribute-power-bi-reports.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="026da-193">For more information about how to author reports by using Entity Store, see [Create analytical reports by using Power BI Desktop](author-distribute-power-bi-reports.md).</span></span>

<span data-ttu-id="026da-194">オンプレミスの配置に固有となる、以下の手順についても注意してください。</span><span class="sxs-lookup"><span data-stu-id="026da-194">Note the following additional steps that are specific to on-premises deployments:</span></span>

- <span data-ttu-id="026da-195">オンプレミス環境においては、実運用環境またはサンドボックス環境に Power BI レポートを配置するにあたってLCSを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="026da-195">For on-premises environments, you don't have to use LCS to deploy Power BI reports to production or sandbox environments.</span></span> <span data-ttu-id="026da-196">オンプレミス環境では、管理者はPowerBI.comデータセットを特定のエンティティー ストアデータベースに指定することができるため、LCSが提供する機能を使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="026da-196">Because admins can point PowerBI.com datasets to specific Entity Store databases in on-premises environments, you don't have to use the functionality that LCS offers.</span></span> <span data-ttu-id="026da-197">ただし、オンプレミスのゲートウェイを設定して、オンプレミスのデータにPowerBI.comがアクセスできるようにする必要となる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="026da-197">However, you might have to configure the on-premises gateway to enable PowerBI.com to access data on-premises.</span></span> <span data-ttu-id="026da-198">ゲートウェイの詳細については、 [Power BI ゲートウェイのドキュメント](https://powerbi.microsoft.com/gateway/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="026da-198">For more information about the gateway, see [Power BI gateway documentation](https://powerbi.microsoft.com/gateway/).</span></span>
- <span data-ttu-id="026da-199">クラウドベースのアプリケーション環境は、DirectQuery オプションを使用して作成されたレポートにのみ対応していますが、オンプレミスのエンティティ格納は、DirectQuery レポートとインポート モード レポートの両方に対応しています。</span><span class="sxs-lookup"><span data-stu-id="026da-199">Although cloud-based application environments support only reports that are authored by using the DirectQuery option, on-premises Entity Store supports both DirectQuery reports and Import mode reports.</span></span>
- <span data-ttu-id="026da-200">分析ワークスペースは、オンプレミス配置はに実装されていません。</span><span class="sxs-lookup"><span data-stu-id="026da-200">Analytical workspaces aren't yet implemented in on-premises deployments.</span></span> <span data-ttu-id="026da-201">分析ワークスペースでレポートを表示することはできませんが、PowerBI.com の環境にレポートを配置することができます。</span><span class="sxs-lookup"><span data-stu-id="026da-201">Instead of viewing reports in analytical workspaces, you can deploy them to PowerBI.com environments.</span></span> <span data-ttu-id="026da-202">そうすることで、PowerBI.com へのアクセス権限を持つユーザーがレポートを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="026da-202">The reports can then be used by users who have access to PowerBI.com.</span></span> <span data-ttu-id="026da-203">PowerBI.comのレポートへのアクセスには、ユーザーが適切なライセンスを要求する場合があります。</span><span class="sxs-lookup"><span data-stu-id="026da-203">Your users might require appropriate licenses to access reports on PowerBI.com.</span></span>

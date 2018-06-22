---
title: "AX 2012 のデータのインポート/エクスポート フレームワークで使用される SSIS のバージョンをコンフィギュレーションする"
description: "このトピックでは、Dynamics AX 2012 のデータ インポート/エクスポート フレームワークで使用されている SSIS を構成する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 51562
ms.assetid: 02188740-e0d9-4b25-9512-dfd15e68020f
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8d8528cb15c17149eea134acaa5c84576f2a2431
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="configure-the-version-of-ssis-used-by-the-ax-2012-data-importexport-framework"></a><span data-ttu-id="dde56-103">AX 2012 のデータのインポート/エクスポート フレームワークで使用される SSIS のバージョンをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="dde56-103">Configure the version of SSIS used by the AX 2012 Data import/export framework</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dde56-104">このトピックは、[KB 3018235](https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235) をインストールした Microsoft Dynamics AX 2012 R2 を実行している環境にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="dde56-104">This topic only applies to environments that are running Microsoft Dynamics AX 2012 R2 with [KB 3018235](https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235) installed.</span></span> <span data-ttu-id="dde56-105">KB 3018235 は、SQL Server 2014 Integration Services で AX 2012 R2 CU7 用のデータのインポート/エクスポート フレームワークを使用するために必要です。</span><span class="sxs-lookup"><span data-stu-id="dde56-105">KB 3018235 is required to use Data Import/Export Framework for AX 2012 R2 CU7 with SQL Server 2014 Integration Services.</span></span> <span data-ttu-id="dde56-106">同じコンピューターに 2 つのバージョンの Microsoft SQL Server Integration Service がインストールされている環境にいる場合、既定では、データのインポート/エクスポート フレームワーク Windows サービスは、検索できる統合サービスの最も古いバージョンを添付します。</span><span class="sxs-lookup"><span data-stu-id="dde56-106">If you are in an environment in which two versions of Microsoft SQL Server Integration Services are installed on the same computer, by default, the Data Import/Export Framework Windows service will attach to the oldest version of Integration Services that it can find.</span></span> <span data-ttu-id="dde56-107">SQL Server 2008 Integration Services は、最も古いサポートされているバージョンです。</span><span class="sxs-lookup"><span data-stu-id="dde56-107">SQL Server 2008 Integration Services is the oldest supported version.</span></span> <span data-ttu-id="dde56-108">アセンブリ バージョンのリダイレクトを使用して、データのインポート/エクスポート フレームワークが、Integration Services の他のバージョンを使用することを強制することができます。</span><span class="sxs-lookup"><span data-stu-id="dde56-108">You can force the Data Import/Export Framework to use another version of Integration Services by using redirecting assembly versions.</span></span> <span data-ttu-id="dde56-109">SQL Server Integration Services の 1 つのバーションだけがインストールされている環境でデータのインポート/エクスポート フレームワークを使用することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="dde56-109">We strongly recommend that you use Data Import/Export Framework in an environment with only one version of SQL Server Integration Services installed.</span></span> <span data-ttu-id="dde56-110">データのインポート/エクスポート フレームワークでサポートされる統合サービスのバージョンを確認するには、[[Microsoft Dynamics AX 2012 のシステム要件](http://go.microsoft.com/fwlink/?LinkId=165377)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dde56-110">To see which versions of Integration Services are supported with the Data Import/Export Framework, see the [Microsoft Dynamics AX 2012 System Requirements](http://go.microsoft.com/fwlink/?LinkId=165377).</span></span>

## <a name="force-the-data-importexport-framework-to-use-a-version-of-integration-services-other-than-the-default"></a><span data-ttu-id="dde56-111">データのインポート/エクスポート フレームワークが既定以外の Integration Services のバージョンを使用することを強制します</span><span class="sxs-lookup"><span data-stu-id="dde56-111">Force the Data import/export framework to use a version of Integration Services other than the default</span></span>
<span data-ttu-id="dde56-112">[アセンブリ バージョンのリダイレクト](https://msdn.microsoft.com/en-us/library/7wd6ex19(v=vs.110).aspx) の既定ではなく、データのインポート/エクスポート フレームワークが Integration Services のバージョンを使用することを強制することができます。</span><span class="sxs-lookup"><span data-stu-id="dde56-112">You can force the Data Import/Export Framework to use a version of Integration Services other than the default by [redirecting assembly versions](https://msdn.microsoft.com/en-us/library/7wd6ex19(v=vs.110).aspx).</span></span>

| <span data-ttu-id="dde56-113">注意 :</span><span class="sxs-lookup"><span data-stu-id="dde56-113">Caution:</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dde56-114">たとえば、インストールされていない Integration Services のバージョンにリダイレクトするなど、アセンブリのバージョン リダイレクトが正しく設定されていない場合、データ インポート/エクスポート フレームワークは正しく機能しません。</span><span class="sxs-lookup"><span data-stu-id="dde56-114">If the assembly version redirection is setup incorrectly, for example, by redirecting to a version of Integration Services that is not installed, the Data Import/Export Framework will not work correctly.</span></span> |

1.  <span data-ttu-id="dde56-115">データのインポート/エクスポート フレームワーク サービス コンポーネントのインストール ディレクトリを指定します。</span><span class="sxs-lookup"><span data-stu-id="dde56-115">Locate the installation directory of the Data Import/Export Framework service component.</span></span>
2.  <span data-ttu-id="dde56-116">テキスト エディタで **Microsoft.Dynamics.AX.DMF.SSISHelperService.exe.config** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="dde56-116">Open the file **Microsoft.Dynamics.AX.DMF.SSISHelperService.exe.config** in a text editor.</span></span>
3.  <span data-ttu-id="dde56-117">ファイルで **&lt;ランタイム&gt;** 要素を検索します。</span><span class="sxs-lookup"><span data-stu-id="dde56-117">Locate the **&lt;runtime&gt;** element in the file.</span></span> <span data-ttu-id="dde56-118">この要素内に、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="dde56-118">Inside this element, add the following code.</span></span>
    -   <span data-ttu-id="dde56-119">SQL Server 2012 Integration Services にリダイレクトするコード     <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1"> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.DTSPipelineWrap"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.DTSRuntimeWrap"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.ManagedDTS"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.PipelineHost"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.SQLTask"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.XmlSrc"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> </assemblyBinding></span><span class="sxs-lookup"><span data-stu-id="dde56-119">Code to redirect to SQL Server 2012 Integration Services     <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1"> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.DTSPipelineWrap"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.DTSRuntimeWrap"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.ManagedDTS"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.PipelineHost"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.SQLTask"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.XmlSrc"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> </assemblyBinding></span></span>

    -   <span data-ttu-id="dde56-120">SQL Server 2014 Integration Services にリダイレクトするコード         <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1"> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.DTSPipelineWrap"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.DTSRuntimeWrap"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.ManagedDTS"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.PipelineHost"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.SQLTask"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.XmlSrc"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> </assemblyBinding></span><span class="sxs-lookup"><span data-stu-id="dde56-120">Code to redirect to SQL Server 2014 Integration Services         <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1"> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.DTSPipelineWrap"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.DTSRuntimeWrap"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.ManagedDTS"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.PipelineHost"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.SQLTask"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.XmlSrc"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> </assemblyBinding></span></span>

4.  <span data-ttu-id="dde56-121">ファイル保存します。</span><span class="sxs-lookup"><span data-stu-id="dde56-121">Save the file.</span></span>
5.  <span data-ttu-id="dde56-122">データのインポート/エクスポート フレームワーク サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="dde56-122">Restart the Data Import/Export Framework service.</span></span>
6.  <span data-ttu-id="dde56-123">変更内容が正常に機能することをテストします。</span><span class="sxs-lookup"><span data-stu-id="dde56-123">Test that your changes are working as expected.</span></span>







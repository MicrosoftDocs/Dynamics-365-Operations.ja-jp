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
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 6d0854ac64a09e5837c0d350da14f47e290491df
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="configure-the-version-of-ssis-used-by-the-ax-2012-data-importexport-framework"></a>AX 2012 のデータのインポート/エクスポート フレームワークで使用される SSIS のバージョンをコンフィギュレーションする

[!include [banner](../../includes/banner.md)]

このトピックは、[KB 3018235](https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235) をインストールした Microsoft Dynamics AX 2012 R2 を実行している環境にのみ適用されます。 KB 3018235 は、SQL Server 2014 Integration Services で AX 2012 R2 CU7 用のデータのインポート/エクスポート フレームワークを使用するために必要です。 同じコンピューターに 2 つのバージョンの Microsoft SQL Server Integration Service がインストールされている環境にいる場合、既定では、データのインポート/エクスポート フレームワーク Windows サービスは、検索できる統合サービスの最も古いバージョンを添付します。 SQL Server 2008 Integration Services は、最も古いサポートされているバージョンです。 アセンブリ バージョンのリダイレクトを使用して、データのインポート/エクスポート フレームワークが、Integration Services の他のバージョンを使用することを強制することができます。 SQL Server Integration Services の 1 つのバーションだけがインストールされている環境でデータのインポート/エクスポート フレームワークを使用することを強くお勧めします。 データのインポート/エクスポート フレームワークでサポートされる統合サービスのバージョンを確認するには、[[Microsoft Dynamics AX 2012 のシステム要件](http://go.microsoft.com/fwlink/?LinkId=165377)] を参照してください。

## <a name="force-the-data-importexport-framework-to-use-a-version-of-integration-services-other-than-the-default"></a>データのインポート/エクスポート フレームワークが既定以外の Integration Services のバージョンを使用することを強制します
[アセンブリ バージョンのリダイレクト](https://msdn.microsoft.com/en-us/library/7wd6ex19(v=vs.110).aspx) の既定ではなく、データのインポート/エクスポート フレームワークが Integration Services のバージョンを使用することを強制することができます。

| 注意 :                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| たとえば、インストールされていない Integration Services のバージョンにリダイレクトするなど、アセンブリのバージョン リダイレクトが正しく設定されていない場合、データ インポート/エクスポート フレームワークは正しく機能しません。 |

1.  データのインポート/エクスポート フレームワーク サービス コンポーネントのインストール ディレクトリを指定します。
2.  テキスト エディタで **Microsoft.Dynamics.AX.DMF.SSISHelperService.exe.config** ファイルを開きます。
3.  ファイルで **&lt;ランタイム&gt;** 要素を検索します。 この要素内に、次のコードを追加します。
    -   SQL Server 2012 Integration Services にリダイレクトするコード     <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1"> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.DTSPipelineWrap"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.DTSRuntimeWrap"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.ManagedDTS"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.PipelineHost"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.SQLTask"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.XmlSrc"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="11.0.0.0" /> </dependentAssembly> </assemblyBinding>

    -   SQL Server 2014 Integration Services にリダイレクトするコード         <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1"> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.DTSPipelineWrap"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.DTSRuntimeWrap"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.ManagedDTS"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.PipelineHost"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.SQLTask"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> <dependentAssembly> <assemblyIdentity name="Microsoft.SqlServer.XmlSrc"
                      publicKeyToken="89845dcd8080cc91" /> <bindingRedirect oldVersion="10.0.0.0" newVersion="12.0.0.0" /> </dependentAssembly> </assemblyBinding>

4.  ファイル保存します。
5.  データのインポート/エクスポート フレームワーク サービスを再起動します。
6.  変更内容が正常に機能することをテストします。







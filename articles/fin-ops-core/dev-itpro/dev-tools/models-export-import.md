---
title: モデルのエクスポートとインポート
description: この記事では、モデルをモデル ファイルにエクスポートし、モデル ファイルをインストールし、開発環境でモデルを削除する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 20451
ms.assetid: 9eb3be56-6382-43df-a247-eae0dcaf46b8
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: afadebba3ebd75136b6281982a02b41eb9b597cb
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093461"
---
# <a name="export-and-import-models"></a>モデルのエクスポートとインポート

[!include [banner](../includes/banner.md)]

モデル ファイルは顧客およびパートナーにモデルを配布して、開発環境にインストールすることができます。 これらは Lifecycle Services (LCS) ソリューションの主要なコンポーネントです。 モデル ファイルには、モデル記述子ファイル、メタデータ、ソース コード、および参照先の .NET アセンブリ (ある場合) が含まれます。 この記事では、モデルをモデル ファイルにエクスポートし、モデル ファイルをインストールし、開発環境でモデルを削除する方法について説明します。


<a name="export-a-model-into-a-model-file-for-distribution"></a>モデルを配布用のモデル ファイルにエクスポート
-------------------------------------------------

既存のモデルをモデル ファイルにエクスポートするには、ModelUtil.exe ツールと **-export** ディレクティブを使用します。 このツールは、パッケージの bin フォルダー (通常は、c:\\packages\\bin または i:\\AosService\\PackagesLocalDirectory\\bin) に配置されています。

```Console
ModelUtil.exe -export -metadatastorepath=[path of the metadata store] -modelname=[name of the model to export] -outputpath=[path of the folder where the model file should be saved]
```

**例**

```Console
ModelUtil.exe -export -metadatastorepath=c:\packages -modelname="FleetManagement" -outputpath=c:\temp
```

上記の例は、c:\\temp に .axmodel ファイルを作成します。通常、次に、顧客プロジェクトや Microsoft Dynamics Lifecycle Services (LCS) ソリューション プロジェクトの資産ライブラリにモデル ファイルをアップロードします。

## <a name="install-a-model-in-a-development-environment"></a>開発環境でのモデルのインストール
開発環境でモデル ファイルをインストールするには、ModelUtil.exe ツールと **-import** ディレクティブを使用します。

```Console
ModelUtil.exe -import -metadatastorepath=[path of the metadata store where model should be imported] -file=[full path of the file to import]
```

モデルが開発環境で既に存在する場合、**-削除** 指令を使用し、それを最初に削除する必要があります。

```Console
ModelUtil.exe -delete -metadatastorepath=[path of the metadata store] -modelname=[name of the model to delete]
```
    
> [!NOTE]
> 以前のバージョンを使用している場合、-replace パラメーターを使用して、オーバーレイヤー用の標準モデル (Foundation など) を置き換えることができます。    

## <a name="resolve-conflicts"></a>競合を解決
モデルを開発環境にインストールするときに、環境開発にそのモデルへのカスタマイズが含まれている場合、コードまたはメタデータの競合を解決する必要がある場合があります。 開発ツールを使用すると、競合しているすべての品目をグループ化するプロジェクトを作成することができます。

1. <strong>Dynamics 365 &gt; AddIns</strong> で、<strong>コンフリクトからプロジェクトを作成する</strong>をクリックします。
2. ダイアログ ボックスで、モデルを選択して競合を確認します。 これは、新しくインストールされたベースライン モデルの要素に対するカスタマイズを含まれるモデルです。
3. **プロジェクトの作成** をクリックします。 競合するモデルの要素のみを含むプロジェクトが生成されます。 

    [![AddUpdate\_MetaHotfix](./media/addupdate_metahotfix.png)](./media/addupdate_metahotfix.png)

4. 競合する要素のデザイナーを開いて、表示されたツールを使って競合を表示し、解決します。 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: "Lifecycle Services (LCS) から更新プログラムをダウンロード"
description: "このチュートリアルを使用して、Lifecycle Services (LCS) から Microsoft Dynamics 365 for Finance and Operations の 修正プログラムをダウンロードします。"
author: AngelMarshall
manager: AnnBe
ms.date: 02/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 56171
ms.assetid: 61069cf2-6c3f-4ebc-bbee-b21b1c99626a
ms.search.region: Global
ms.author: amarshall
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 0c0ec9dd9f45eb6c534215105113f03b15797db2
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="download-updates-from-lifecycle-services-lcs"></a>Lifecycle Services (LCS) から更新プログラムをダウンロード

[!include [banner](../includes/banner.md)]

このチュートリアルを使用して、Microsoft Dynamics Lifecycle Services (LCS) から更新プログラムをダウンロードします。

## <a name="types-of-updates"></a>更新のタイプ

- **バイナリ更新プログラム**は、コンパイル済みで累積されています。 その後のバイナリ更新には、これまでのすべての更新が含まれます。 これらの更新は、開発環境でコンパイルする必要はなく、LCS から非開発環境に直接適用することもできます。
        
    小売機能とカスタマイズされた販売時点管理 (POS) のインスタンスを持つ環境を実行している場合は、Retail SDK のパッケージに記載されている追加手順を完了する必要があります。 Microsoft Dynamics 365 for Retail で、すべての更新プログラムは、アプリケーション モデルの更新プログラムでさえ、バイナリ更新プログラムとしてリリースされます。
    
    > [!NOTE]
    > 環境がプラットフォーム更新プログラム 4 以上である場合、**すべてのバイナリ更新プログラム**および**プラットフォーム バイナリ更新プログラム**を LCS **環境**ページからダウンロードするオプションがあります。  
    > - **すべてのバイナリ更新プログラム** タイルには、アプリケーションとプラットフォームのバイナリ アップデートのパッケージの一覧が含まれています。  
    > - **プラットフォーム バイナリの更新プログラム** タイルには、最新のプラットフォーム専用の更新プログラムまたは修正プログラムが含まれます。 
    

- **X++ 更新プログラム**には、アプリケーション モデルの特定のアプリケーション機能への更新が含まれます。 これらの更新は、個別にダウンロードして適用することができます。 環境に適用する特定の X++ 更新プログラムを選択することができます。  依存 X++ 更新は自動的に選択され、ダウンロードされます。  X++ の更新はソース コードの更新であり、非開発環境に適用する前に、開発環境でコンパイルして任意のカスタマイズとマージする必要があります。 X++ の更新プログラムは Microsoft Dynamics 365 for Finance and Operations に対してのみ適用されます。 

    > [!NOTE]
    > オンライン環境では、**すべての X++ 更新プログラム**タイルおよび**重要な X++ 更新プログラム**タイルの両方を表示します。 重要な X++ 更新プログラムは、**実稼働環境**のテレメトリ データに基づく推奨 KB です。  
    >
    > X++ 更新プログラムをテストして適用するには、X++ 更新プログラムをダウンロードした後で開発環境に適用して展開可能パッケージを作成し、展開可能パッケージをサンドボックスに適用してから実稼働環境に適用します。 
    >
    > 更新の展開に関する詳細については、[クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md) を参照してください  

## <a name="download-updates"></a>更新プログラムのダウンロード

利用可能な更新プログラムを表示するには、次のようにします。
1. 資格情報を使用して LCS にサインインします。
2. LCS プロジェクトで、環境を選択します。
3. **環境**ページで、**監視**セクションには更新タイルが含まれています。 

   >[!NOTE]
   > Retail で、バイナリ更新プログラムのみに対するタイルを表示します。 Finance and Operations で、X++ 更新およびバイナリ更新の両方に対するタイルを表示します。 これらの 2 種類の更新は、個別にダウンロードして適用することができます。 ただし、一部の X++ 更新プログラムはバイナリ更新プログラムに依存し、別のバイナリ更新プログラムは X++ 更新プログラムに依存しています。 すべての依存関係は、更新の説明に含まています。
   
## <a name="download-binary-updates"></a>ダウンロード Binary 更新プログラム

1. **すべてのバイナリ更新プログラム** タイルをクリックすると、アプリケーションおよびプラットフォームのバイナリ アップデートの組み合わせリスト、またはプラットフォームのみのバイナリ アップデートのための**プラットフォーム バイナリ更新プログラム** タイルが表示されます。 

   ![バイナリ タイル](./media/BinaryUpdateTiles.jpg)

2. **バイナリ更新プログラム**ページで、**パッケージの保存**を選択します。

   ![バイナリ パッケージの保存](./media/ReviewAndSaveBinaryPackage.jpg)

3. **更新プログラムの確認と保存**ページで、**パッケージの保存**を選択します。

![更新プログラムの確認と保存](./media/ReviewBinaryPackage.jpg)

4. **資産ライブラリへのパッケージの保存**スライダーから、**名前**および**説明**を入力し、**パッケージの保存**をクリックします。

   ![資産ライブラリへのパッケージの保存](./media/SaveBinaryPackage.jpg)

5. **完了**をクリックし、環境ページに戻ります。

   ![DoneSavingBinaryPackage](./media/DoneSavingBinaryPackage.jpg)
 
6. 資産ライブラリに保存されているバイナリ パッケージが表示されます。 

   ![ViewSavedBinaryPackageInAssetLibrary](./media/ViewSavedBinaryPackageInAssetLibrary.jpg)

## <a name="download-x-updates"></a>ダウンロード X++ 更新プログラム

1. **すべての X++ 更新プログラム** タイルをクリックすると、使用可能なアプリケーションの更新の一覧を環境に表示、または実稼働環境への推奨アプリケーションの更新プログラムの**重要な X++ 更新プログラム**を表示します。 

   ![アプリケーション X++ 更新タイル](./media/X++UpdateTiles.jpg)   
  
2. **更新プログラムの追加**ページで、該当するナレッジサポート技術情報 (KB) 番号を選択し、**追加**をクリックし、選択した KB を**ダウンロード パッケージ**に追加します。

    ![X++ の更新プログラムの追加](./media/AddX++Updates.jpg)

    > [!NOTE]
    > X++ の更新プログラムで、この時点で利用可能なすべての更新プログラムをダウンロードすることができます。 **すべて選択** を選択して **追加** をクリックし、すべての KB を **ダウンロード パッケージ** に追加します。

3. **ダウンロード パッケージ** を選択します。

    ![ダウンロード X++ パッケージ](./media/DownloadX++UpdatePackage.jpg)

4. **修正プログラムの確認とダウンロード**ページで、選択した修正プログラムを確認したり、パッケージを破棄して、修正プログラムの選択に戻ったり、または最終修正プログラムのパッケージをダウンロードしたりすることができます。

    ![X++ 更新プログラムの確認とダウンロード](media/ReviewAndDownloadX++Package.jpg)
    
5. パッケージをダウンロードして**完了**をクリックします。
    
    ![downloaded](media/X++UpdatesDownloadBegin.jpg)


## <a name="also-see"></a>参照してください。
- [クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md)
- [メタデータ修正プログラムのインストール](./install-metadata-hotfix-package.md) 


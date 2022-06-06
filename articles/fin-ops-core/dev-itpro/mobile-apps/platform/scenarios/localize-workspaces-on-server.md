---
title: モバイル ワークスペースのローカライズ
description: このトピックでは、ワークスペース クラスを使用して、ワークスペースにローカライゼーション サポートを提供する方法について説明します。
author: tonyafehr
ms.date: 05/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 48efe161aad4873cc5ece6d43b4d4d39ef07db34
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811440"
---
# <a name="localize-mobile-workspaces"></a>モバイル ワークスペースのローカライズ

[!include [banner](../../../includes/banner.md)]
[!include [mobile app deprecated](../../../includes/mobile-app-deprecation-banner.md)]

いくつかの方法でワークスペース クラスを使用すると、ワークスペースにローカライゼーション サポートを提供することができます。

## <a name="use-config-objects-to-pass-localized-labels"></a>Config オブジェクトを使用して、ローカライズされたラベルを渡す
コンフィギュレーション オブジェクトは、モバイル アプリケーションから要求されたときに、ワークスペース メタデータに追加できます。 後で、config オブジェクトは、ローカライズ サポートを提供するために使用できます。 

たとえば、次のワークスペースは、ビジネス ロジックを通して追加された **pageLink** コントロールの、ローカライズされたラベルを必要とします。

 ![レンタル リンクのテキストがローカライズされていない顧客の詳細ワークスペース。](media/workspace-api/ConfigObjectsPage.png)

アプリケーションのビジネス ロジックには、次の図に示すように、**addLink** メソッドの呼び出しが含まれています。 この **addLink** メソッドは、現在のお客様の **レンタル** ページへリンクを追加します。 この場合、リンクのラベルは **レンタル** です。 ただし、リンクのローカライズされたラベルがないため、リンクは常に **レンタル** として表示されます。

![metadataService.addLink を呼び出します。](media/workspace-api/ConfigObjectsBusinessLogicOriginal.png)

構成オブジェクトを使用してローカライズされたラベルを提供するには、次の手順を実行します。

1. ラベルのフィールドを含む config クラスを作成します。 1 つのフィールド、**rentalLinkLabel** が、**pageLink** コントロールのラベルを含むクラスに追加されます。 コンフィギュレーション クラスは、データ契約クラスでなければなりません。

    ![コンフィギュレーション クラス コード。](media/workspace-api/ConfigClass.png)

2. コンフィギュレーション クラスは、ワークスペースのワークスペース クラスで使用されます。 ワークスペース クラスには、ワークスペースの **appId** 値が必要です。 次の図に示すように、アプリ デザイナーでアプリの ID を検索することができます。

    ![ワークスペース概要のアプリ ID。](media/workspace-api/ConfigWorkspaceSummary.png)

    次の図は、**appId** 値が属性に設定されているときのワークスペース クラスの外観を示しています。 このクラスには、ラベルの値を含む設定オブジェクトを設定するメソッド、**addConfig** も含まれています。

    ![ワークスペース クラス。](media/workspace-api/ConfigWorkspace.png)

    次の図は、モバイル アプリの **appInit** コールの config オブジェクトを示しています。

    ![モバイル アプリのコンフィギュレーション オブジェクト。](media/workspace-api/ConfigClientSide.png)

3. これで、コンフィギュレーション オブジェクトを使用し、ハードコーディングされたラベルの代わりに **addLink** メソッドに渡すことができます。

    ![config オブジェクトの呼び出しによる metadataService.addLink。](media/workspace-api/ConfigObjectsBusinessLogicFinal.png)

## <a name="use-a-workspace-class-to-update-the-workspace-title-and-description"></a>ワークスペース クラスを使用して、ワークスペースのタイトルと説明を更新する
ワークスペース クラスは、ワークスペースのタイトルと説明のローカライズされた文字列を提供するために使用することができます。 タイトルと説明をローカライズしていない場合、それらを実装した言語がフィールドの言語になります。 この例では、**MyWorkspace** がタイトルで、**サンプル ワークスペース** が説明となっているワークスペースをローカライズします。

![ワークスペースのリスト。](media/workspace-api/LocalizeWorkspaceTitle.png) 

![選択されたワークスペース。](media/workspace-api/LocalizeWorkspaceOriginal.png)

1. ワークスペースのワークスペース クラスを持っていない場合、ワークスペースのクラスを作成します。
2. **getWorkspaceMetadata** メソッドをオーバーライドし、ワークスペース メタデータを取得します。 ワークスペースのタイトルおよび説明フィールドのラベルにするワークスペース メタデータが必要です。
3. ワークスペースのタイトルと説明をラベルから設定するには、**workspaceTitle** および **workspaceDescription** プロパティを使用します。 次の図では、プレースホルダーが **workspaceTitle** および **workspaceDescription** プロパティに割り当てられています。

    ![ワークスペース クラスのタイトルと説明を提供。](media/workspace-api/LocalizeWorkspaceClass.png)

4. ワークスペース クラスをビルドします。
5. モバイル クライアントのアプリ リストを更新します。

次の図は、英語とデンマーク語を使用する電話機のタイトルと説明を示しています。

![最終ワークスペース。](media/workspace-api/LocalizeWorkspaceFinal.png)


[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]

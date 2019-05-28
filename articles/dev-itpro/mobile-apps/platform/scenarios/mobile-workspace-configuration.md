---
title: SysAppWorkspace クラスを使用してワークスペースを構成する
description: このトピックでは、SysAppWorkspace クラスを使用してサーバー上のワークスペースを構成および公開する方法について説明します。
author: makhabaz
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 9b0e6ae43d082dff8c62fbd39e385b3c9835b788
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537437"
---
# <a name="configure-workspaces-by-using-the-sysappworkspace-class"></a>SysAppWorkspace クラスを使用してワークスペースを構成する

[!include [banner](../../../includes/banner.md)]

ワークスペース クラス **SysAppWorkspace** は、サーバー上でワークスペースを作成、構成および公開する開始点です。 sysAppWorkspace で使用できる API には、次の 2 つのカテゴリがあります。

+ **ワークスペースの属性**; はモバイルワークスペースを構築するために、ページ、タスク、エンティティ、ルックアップ、リレーションシップの作成に使用されます。 

    [フリート管理のモバイル アプリのサンプル プロジェクトをダウンロードする](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) (.axpp ファイル)。
    *ファイルをダウンロードした後、オペレーション開発環境で Visual Studio を開き、Dynamics 365 > プロジェクトのインポートをクリックし、ダウンロードしたプロジェクト ファイルを閲覧します。同じダイアログで、上書きにチェックを入れ、新しいソリューションの作成にチェックを入れます。インポートが完了した後、ソリューションを構築 (またはフリート管理モデルを構築) します。例を確認するには、まず、ワークスペースに含まれるすべてのページとアクションを見るために、'FMReservationManagementWorkspace' クラスを確認します。ソリューション エクスプローラを使用して、ページおよびタスク クラスを検索し、それぞれに含まれるすべての資産を検索してください。各 API の詳細については、API リファレンスを使用してください。*
    
    **X++ モバイル ワークスペースは、デザイナー ウィンドウで、X++ 属性 API またはその両方の組み合わせを使用して作成できます。 デザイナーから AOT へのモバイル アプリ メタデータのインポートの詳細については、以下の「ワークスペース クラスを使用して AOT リソースのワークスペースを公開する」を参照してください。上記のサンプルは、X++ 属性 API を使用して構築された完全なモバイル アプリです。**

+ **ワークスペース メタデータ クラス**; はモバイル ワークスペースのためのメタデータへのサーバー側のビジネス ロジックを調査し、適用するために使用します。 

[サーバー側の APIs の完全な一覧を参照してください。](../mobile-workspace-server-apis.md)



## <a name="create-a-new-workspace-class"></a>新しいワークスペース クラスを作成する
ワークスペースに **SysAppWorkspace** クラスを使用するには、 **SysAppWorkspace** クラスを拡張してワークスペース用に新しいクラスを作成する必要があります。 新しいクラスを使用してワークスペース メタデータを変更することができます。 新しいクラスは、モバイル アプリのライフ サイクル管理のフックも提供します。

ワークスペース用の新しいワークスペース クラスを作成するには、これらの手順に従います。

1. ワークスペース用の新しいクラスを作成し、それを **SysAppWorkspace** クラスから拡張します。

    ![ワークスペース クラス](media/workspace-api/WorkspaceClass.png)

2. 新しいクラスに **SysAppWorkspaceAttribute** 属性を追加し、ワークスペースの **AppID** 値を指定します。 アプリ用アプリ ID はモバイル アプリ デザイナー内の **概要** ページで見つけることができます。

    ![ワークスペース概要のアプリ ID](media/workspace-api/workspaceSummary.png)

    ![ワークスペース クラスの AppID 値](media/workspace-api/WorkspaceClassWithAppId.png)

3. オプション: ワークスペースがアプリケーション オブジェクト ツリー (AOT) リソースの場合、AOT リソースの名前を **SysAppWorkspaceAttribute** コンストラクターの 2 番目のパラメーターとして指定します。

    ![ワークスペース クラスの AOT リソース名。](media/workspace-api/WorkspaceClassWithAOTResource.png)

## <a name="use-the-workspace-class-to-publish-workspaces-from-aot-resources"></a>AOT リソースからワークスペースを発行するには、workspace クラスを使用します。
ワークスペースはデータベース内に配置することができます。 リソースとして AOT に常駐することもできます。 AOT リソースに格納されているワークスペースを可視化するには、ワークスペース・クラスを作成し、そのワークスペースを含む AOT リソースの名前をポイントする必要があります。 AOT リソースとして保管されているワークスペースは、モバイル アプリ デザイナーを使用して編集または削除することはできません。 これらのワークスペースはエクスポートのみ可能です。

AOT リソースとして存在するワークスペースを公開するには、これらの手順に従います。

1. データベースに格納されるワークスペースを作成するとき、AOT リソースとして保存できるように、それをモバイル アプリ デザイナーからエクスポートする必要があります。 ワークスペースは XML ファイル形式でエクスポートされます。

    ![ワークスペースをエクスポート](media/workspace-api/ExportWorkspace.png)

2. モバイル アプリのデザイナーからワークスペースを削除します。 それを後で AOT リソースから読み込みます。

    ![ワークスペースの削除](media/workspace-api/DeleteWorkspace.png)

3. 新しい AOT リソースを作成し、リソースのエクスポートされたワークスペースを選択します。

    ![リソースとしてのワークスペース](media/workspace-api/WorkspaceAsResource.png)

4. ワークスペース用の新しいクラスを作成します。 このクラスは、**SysAppWorkspace** を拡張する必要があります。 **SysAppWorkspaceAttribute** 属性をクラスに適用し、リソースを含むアプリ ID と AOT リソース名を指定します。

    ![新しいワークスペース クラス](media/workspace-api/NewWorkspaceClass.png)

5. クラスをビルドして、モバイル アプリ デザイナーを再オープンします。

    ワークスペースが公開されました。 これはデザイナーに表示されますが、編集または削除できません。 ワークスペースがメタデータから読み込まれることに注意してください。

    ![メタデータ内のワークスペース](media/workspace-api/WorkspaceInMetadata.png)

## <a name="update-a-workspace-that-has-already-been-published"></a>発行済みワークスペースの更新
ワークスペースが AOT リソースの一部である場合、モバイル アプリ デザイナーを使用して編集することはできません。 次の例では、**MyWorkspace** というワークスペースが AOT に存在し、そこには **WorkspaceInAOT** というバッキング クラスがあります。

![AOT 内のワークスペース](media/workspace-api/UpdateWorkspaceInAOT.png)

![AOT 内にある公開済みのワークスペース](media/workspace-api/UpdateWorkspaceInAOTAndPublished.png)

ワークスペースを編集するには、これらの手順に従います。

1. モバイル アプリ デザイナーを使用して、ワークスペースをエキスポートします。 デザイナーは、AOT に保存されているワークスペースの新しいアプリ ID を自動的に作成します。
2. モバイル アプリ デザイナーを使用して、新しくエクスポートされたワークスペースをインポートします。

   1. オプション: 名前を変更します。新たに追加されたワークスペースを他のワークスペースと区別できるようにします。
   2. 新しく作成したワークスペースのアプリ ID をコピーします。

      ![データベースの新しいワークスペース](media/workspace-api/UpdateWorkspaceNewWorkspace.png)

      ![新しいワークスペースの詳細](media/workspace-api/UpdateWorkspaceNewWorkspaceDetails.png)

3. バッキング クラスを拡張し、**SysAppWorkspaceAttribute** 属性を適用し、新しいアプリ ID を指定する新しいクラスを作成します。

    ![メタデータ内のワークスペース](media/workspace-api/UpdateWorkspaceNewWorkspaceClass.png)

新しいワークスペースおよびバッキング クラスでの作業を続行することができるようになりました。 変更を行なった後、AOT ベース ワークスペースとそれらをマージできます。

## <a name="delete-a-workspace-that-is-an-aot-resource"></a>AOT リソースであるワークスペースの削除
モバイル ワークスペースが AOT リソースとして格納されている場合は、それをモバイル アプリ デザイナーを使用して削除することはできません。 AOT リソースとして存在するワークスペースを削除するには、これらの手順に従います。

1. ワークスペースを含む AOT リソースを削除します。

    ![削除するワークスペース](media/workspace-api/WorkspaceAsResourceToBeDeleted.png)

2. ワークスペース用に作成されたワークスペース クラスを削除します。

    ![削除するワークスペース クラス](media/workspace-api/WorkspaceClassToBeDeleted.png)

3. AOT リソースおよびクラスを含む完全なモデル ビルドを実行します。 次の図は、アプリケーション基準モデルの完全なビルドを示しています。 アプリケーション基盤モデルには、AOT リソースとワークスペース クラスも含まれます。 フルビルドをスピードアップするには、**オプション** タブですべての選択をクリアします。

    ![完全なビルド メニュー項目](media/workspace-api/FullBuildMenuItem.png)

    ![完全なビルド](media/workspace-api/FullBuild.png)

4. ビルドが完了したら、モバイル アプリ デザイナーを再オープンして、ワークスペースが存在しないことを確認します。


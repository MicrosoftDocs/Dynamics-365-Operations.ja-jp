---
title: SysAppWorkspace クラスを使用してワークスペースを構成する
description: この記事では、SysAppWorkspace クラスを使用してサーバー上にワークスペースを構成および公開する方法について説明します。
author: jasongre
ms.date: 05/26/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: b016eee73597059fe889efe51d36a35b50a2fe00
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288665"
---
# <a name="configure-workspaces-by-using-the-sysappworkspace-class"></a>SysAppWorkspace クラスを使用してワークスペースを構成する

[!include [banner](../../../includes/banner.md)]
[!include [mobile app deprecated](../../../includes/mobile-app-deprecation-banner.md)]

ワークスペース クラス **SysAppWorkspace** は、サーバー上でワークスペースを作成、構成および公開する開始点です。 sysAppWorkspace で使用できる API には、次のカテゴリがあります。

- **ワークスペースの属性** - これはモバイルワークスペースを構築するために、ページ、タスク、エンティティ、ルックアップ、リレーションシップの作成に使用されます。 
    - フリート管理のモバイル アプリのサンプル プロジェクトをダウンロードします。 これは、[Dynamics365-for-Operations-mobile-FleetManagementSamples](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) で発見された .axpp ファイルです。
    - ファイルをダウンロードした後、運用開発環境で Visual Studio を開き、**Dynamics 365 > Import Project** を選び、ダウンロードされたプロジェクト ファイルを参照します。 同じダイアログ ボックスで、**上書き** を選び、**新しいソリューションの作成** を選択します。 インポートが完了したら、ソリューションをビルドします (または、フリート管理 モデルをビルドします)。 
    - 例を確認するには、まず FMReservationManagementWorkspace クラスを確認し、ワークスペースに含まれるすべてのページとアクションを表示します。 ソリューション エクスプローラーを使用して、ページとタスク クラス、およびそれらに含まれるすべての資産を検索します。 各 API の詳細については、API リファレンスを参照してください。
    - モバイル ワークスペースは、X + + 属性 APIs またはその両方の組み合わせを使用して、デザイナー ウィンドウから作成できます。 デザイナーから AOT にモバイル アプリのメタデータをインポートする方法については、この後の「ワークスペース クラスを使用して AOT リソースからワークスペースを発行」を参照してください。 サンプル プロジェクトのフリート管理モバイル アプリは、X + + 属性 APIs を使用して作成された完全なモバイル アプリです。

- **ワークスペース メタデータ クラス** - これはモバイル ワークスペースのためのメタデータへのサーバー側のビジネス ロジックを調査し、適用するために使用します。 

サーバー側の APIs の完全一覧については、[サーバー側の開発 (ワークスペース X++ APIs)](../mobile-workspace-server-apis.md) を参照してください。


## <a name="create-a-new-workspace-class"></a>新しいワークスペース クラスを作成する
ワークスペースに **SysAppWorkspace** クラスを使用するには、 **SysAppWorkspace** クラスを拡張してワークスペース用に新しいクラスを作成する必要があります。 新しいクラスを使用してワークスペース メタデータを変更することができます。 新しいクラスは、モバイル アプリのライフ サイクル管理のフックも提供します。

ワークスペース用の新しいワークスペース クラスを作成するには、これらの手順に従います。

1. ワークスペース用の新しいクラスを作成し、それを **SysAppWorkspace** クラスから拡張します。

    ![ワークスペース クラス。](media/workspace-api/WorkspaceClass.png)

2. 新しいクラスに **SysAppWorkspaceAttribute** 属性を追加し、ワークスペースの **AppID** 値を指定します。 アプリ用アプリ ID はモバイル アプリ デザイナー内の **概要** ページで見つけることができます。

    ![ワークスペース概要のアプリ ID。](media/workspace-api/workspaceSummary.png)

    ![ワークスペース クラスの AppID 値。](media/workspace-api/WorkspaceClassWithAppId.png)

3. オプション: ワークスペースがアプリケーション オブジェクト ツリー (AOT) リソースの場合、AOT リソースの名前を **SysAppWorkspaceAttribute** コンストラクターの 2 番目のパラメーターとして指定します。

    ![ワークスペース クラスの AOT リソース名。](media/workspace-api/WorkspaceClassWithAOTResource.png)

## <a name="use-the-workspace-class-to-publish-workspaces-from-aot-resources"></a>AOT リソースからワークスペースを発行するには、workspace クラスを使用します。
ワークスペースはデータベース内に配置することができます。 リソースとして AOT に常駐することもできます。 AOT リソースに格納されているワークスペースを可視化するには、ワークスペース・クラスを作成し、そのワークスペースを含む AOT リソースの名前をポイントする必要があります。 AOT リソースとして保管されているワークスペースは、モバイル アプリ デザイナーを使用して編集または削除することはできません。 これらのワークスペースはエクスポートのみ可能です。

AOT リソースとして存在するワークスペースを公開するには、これらの手順に従います。

1. データベースに格納されるワークスペースを作成するとき、AOT リソースとして保存できるように、それをモバイル アプリ デザイナーからエクスポートする必要があります。 ワークスペースは XML ファイル形式でエクスポートされます。

    ![ワークスペースをエクスポートします。](media/workspace-api/ExportWorkspace.png)

2. モバイル アプリのデザイナーからワークスペースを削除します。 それを後で AOT リソースから読み込みます。

    ![ワークスペースを削除します。](media/workspace-api/DeleteWorkspace.png)

3. 新しい AOT リソースを作成し、リソースのエクスポートされたワークスペースを選択します。

    ![リソースとしてのワークスペース。](media/workspace-api/WorkspaceAsResource.png)

4. ワークスペース用の新しいクラスを作成します。 このクラスは、**SysAppWorkspace** を拡張する必要があります。 **SysAppWorkspaceAttribute** 属性をクラスに適用し、リソースを含むアプリ ID と AOT リソース名を指定します。

    ![新しいワークスペース クラス。](media/workspace-api/NewWorkspaceClass.png)

5. クラスをビルドして、モバイル アプリ デザイナーを再オープンします。

    ワークスペースが公開されました。 これはデザイナーに表示されますが、編集または削除できません。 ワークスペースがメタデータから読み込まれることに注意してください。

    ![メタデータ内のワークスペース。](media/workspace-api/WorkspaceInMetadata.png)

## <a name="update-a-workspace-that-has-already-been-published"></a>発行済みワークスペースの更新
ワークスペースが AOT リソースの一部である場合、モバイル アプリ デザイナーを使用して編集することはできません。 次の例では、**MyWorkspace** というワークスペースが AOT に存在し、そこには **WorkspaceInAOT** というバッキング クラスがあります。

![AOT 内のワークスペース。](media/workspace-api/UpdateWorkspaceInAOT.png)

![AOT 内にある公開済みのワークスペース。](media/workspace-api/UpdateWorkspaceInAOTAndPublished.png)

ワークスペースを編集するには、これらの手順に従います。

1. モバイル アプリ デザイナーを使用して、ワークスペースをエキスポートします。 デザイナーは、AOT に保存されているワークスペースの新しいアプリ ID を自動的に作成します。
2. モバイル アプリ デザイナーを使用して、新しくエクスポートされたワークスペースをインポートします。

   1. オプション: 名前を変更します。新たに追加されたワークスペースを他のワークスペースと区別できるようにします。
   2. 新しく作成したワークスペースのアプリ ID をコピーします。

      ![データベースの新しいワークスペース。](media/workspace-api/UpdateWorkspaceNewWorkspace.png)

      ![新しいワークスペースの詳細。](media/workspace-api/UpdateWorkspaceNewWorkspaceDetails.png)

3. バッキング クラスを拡張し、**SysAppWorkspaceAttribute** 属性を適用し、新しいアプリ ID を指定する新しいクラスを作成します。

    ![SysAppWorkspaceAttribute を使用したコード エディター。](media/workspace-api/UpdateWorkspaceNewWorkspaceClass.png)

新しいワークスペースおよびバッキング クラスでの作業を続行することができるようになりました。 変更を行なった後、AOT ベース ワークスペースとそれらをマージできます。

## <a name="delete-a-workspace-that-is-an-aot-resource"></a>AOT リソースであるワークスペースの削除
モバイル ワークスペースが AOT リソースとして格納されている場合は、それをモバイル アプリ デザイナーを使用して削除することはできません。 AOT リソースとして存在するワークスペースを削除するには、これらの手順に従います。

1. ワークスペースを含む AOT リソースを削除します。

    ![削除するワークスペース。](media/workspace-api/WorkspaceAsResourceToBeDeleted.png)

2. ワークスペース用に作成されたワークスペース クラスを削除します。

    ![削除するワークスペース クラス。](media/workspace-api/WorkspaceClassToBeDeleted.png)

3. AOT リソースおよびクラスを含む完全なモデル ビルドを実行します。 次の図は、アプリケーション基準モデルの完全なビルドを示しています。 アプリケーション基盤モデルには、AOT リソースとワークスペース クラスも含まれます。 フルビルドをスピードアップするには、**オプション** タブですべての選択をクリアします。

    ![完全なビルド メニュー項目。](media/workspace-api/FullBuildMenuItem.png)

    ![完全なビルド。](media/workspace-api/FullBuild.png)

4. ビルドが完了したら、モバイル アプリ デザイナーを再オープンして、ワークスペースが存在しないことを確認します。



[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]

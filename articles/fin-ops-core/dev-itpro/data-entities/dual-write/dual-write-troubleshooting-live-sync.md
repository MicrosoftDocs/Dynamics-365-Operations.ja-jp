---
title: ライブ同期に関する問題のトラブルシューティング
description: このトピックでは、ライブ同期の問題修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d45b19c1e88e6a27bde4335d4a356f2173bdfcd3
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275420"
---
# <a name="troubleshoot-live-synchronization-issues"></a>ライブ同期に関する問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]



このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。 このトピックでは、ライブ同期の問題修正に役立つトラブルシューティングに特化した情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Finance and Operations アプリでレコードを作成すると、ライブ同期で 403 権限がありません エラーが発生する

Finance and Operations アプリでレコードを作成した際に、次のエラー メッセージが表示される場合があります。

*\[{\\"エラー\\"：{\\"コード\\"：\\"0x 80072560\\"、\\"メッセージ\\"：\\"ユーザーは組織のメンバではありません。\\}}\]、リモートサーバーからエラーが返されました：（403）権限がありません。"}}"*

この問題を修正するには、[システム要件と前提条件](requirements-and-prerequisites.md) に記載されている手順を実行してください。 これらの手順を完了するには、Common Data Service で作成したデュアル書き込みアプリケーションのユーザーにシステム管理者ロールが割り当てられている必要があります。 また、既定の所有チームにシステム管理者ロールが割り当てられている必要があります。

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Finance and Operations アプリでレコードを作成時に、エンティティに対するライブ同期を行うと同様のエラーが発生する

**問題の修正に必要な役割：** システム管理者

エンティティ データを Finance and Operations アプリに保存するたびに、次のようなエラーメッセージが表示される場合があります：

*データベースへの変更を保存できません。作業単位で取引をコミットすることはできません。エンティティ uoms にデータを書き込むことができません。UnitOfMeasureEntity への書き込みが失敗し、次のエラーメッセージが表示されました。エンティティ uoms と同期することはできません。*

問題を修正するには、前提条件となる参照データが Finance and Operations アプリと Common Data Service の両方に存在していることを確認する必要があります。 たとえば、Finance and Operations アプリで作業している顧客が特定の顧客グループに属している場合は、その顧客グループが Common Data Service に存在することを確認します。

データが両面に存在し、問題がデータに起因するものではないことが分かった場合は、次の手順を実行してください。

1. 関連するエンティティを停止します。
2. Finance and Operations アプリにログインし、失敗したエンティティのレコードが DualWriteProjectConfiguration テーブルと DualWriteProjectFieldConfiguration テーブルに存在することを確認します。 たとえば、**顧客**エンティティに障害が発生した場合、クエリは次のようになります。

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. エンティティのマッピングを停止しても、失敗したエンティティのレコードが存在する場合は、失敗したエンティティに関連するレコードを削除してください。 DualWriteProjectConfiguration テーブルの **projectname** 列をメモし、プロジェクト名を使用してレコードを削除することで、DualWriteProjectFieldConfiguration テーブル内のレコードをフェッチします。
4. エンティティのマッピングを開始します。 データが問題なく同期されていることを検証してください。

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Finance and Operations アプリにデータを作成する際の、読み取り、書き込み権限に関するエラーを処理する

Finance and Operationsアプリでデータを作成する際に、次のような "要求が不正です" というエラー メッセージが表示される場合があります。

![不正な要求のエラー メッセージの例](media/error_record_id_source.png)

この問題を修正するには、マッピングされた Dynamics 365 Sales または Dynamics 365 Customer Service の部署のチームに適切なセキュリティロールを割り当てて、不足している権限を有効にする必要があります。

1. Finance and Operations アプリで、データ統合の接続セットにマッピングされている事業単位を検索します。

    ![組織のマッピング](media/mapped_business_unit.png)

2. Dynamics 365 のモデル駆動型アプリケーションの環境にログインし、**設定 \> セキュリティ** に移動し、マッピングされた事業単位のチームを検索します。

    ![マッピングされた事業単位のチーム](media/setting_security_page.png)

3. 編集をするチームのページを開き、 **ロールの管理** を選択して、**チームロールの管理** ダイアログ ボックスを開きます。

    ![ロールの管理ボタン](media/manage_team_roles.png)

4. 関連するエンティティに対する読み取り/書き込み権限を持つロールの割り当てを行い、 **OK** を選択します。

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a>最近変更された Common Data Service 環境の存在する環境にて、同期の問題を修正する

**問題の修正に必要な役割：** システム管理者

Finance and Operations アプリでデータを作成した際に、次のエラー メッセージが表示される場合があります。

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**エンティティ CustCustomerV3Entity のペイロードを生成できません。**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":" ペイロードの作成に失敗しました。エラー 無効な URI です：URI が入力されていません。}\],"isErrorCountUpdated":true}*

Dynamics 365 のモデル駆動アプリでは、次のようにエラーが表示されます：

*ISV コードに起因する予期しないエラーが発生しました。（ErrorType = ClientError）プラグイン（実行）に起因する予期しない例外が発生しました。Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: エンティティ アカウントの処理に失敗しました ―（接続先が一定期間応答しなかったために接続に失敗したか、接続ホストが応答しなかったために確立された接続が失敗しました*

このエラーは、Finance and Operations アプリでのデータ作成時に、Common Data Service 環境が正しくリセットされていない場合に発生します。

問題を解決するには、次の手順に従います。

1. Finance and Operations 仮想マシン（VM）にログインし、SQL Server Management Studio（SSMS）を起動し、DUALWRITEPROJECTCONFIGURATIONENTITY テーブルにて、**internalentityname** が **Customers V3** 、かつ **externalentityname** が **アカウント** となっているレコードを探してください。 以下にクエリの例を示します。

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. 前のクエリの結果からプロジェクト名を使用して、次のクエリを実行してください。

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. **externalenvironmentURL** の列に、正しい Common Data Service またはアプリの URL が設定されていることを確認してください。 誤った Common Data Service の URL を指している重複レコードを削除します。 DUALWRITEPROJECTFIELDCONFIGURATION テーブルと DUALWRITEPROJECTCONFIGURATION テーブルにて該当するレコードを削除します。
4. エンティティのマッピングを停止して、再起動してください。

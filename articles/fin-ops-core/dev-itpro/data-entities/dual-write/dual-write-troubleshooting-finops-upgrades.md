---
title: Finance and Operations アプリのアップグレードに関する問題のトラブルシューティング
description: このトピックでは、Finance and Operations アプリの更新に関する問題の修正に役立つトラブルシューティング情報を提供します。
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
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172880"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>Finance and Operations アプリのアップグレードに関する問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]



このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。 このトピックでは、Finance and Operations アプリの更新に関する問題の修正に役立つトラブルシューティングに特化した情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="database-synchronization-errors"></a>データベース同期のエラー

**問題の修正に必要な役割：** システム管理者

**DualWriteProjectConfiguration**エンティティを使用して、プラットフォーム更新プログラム 30 を Finance and Operations アプリに更新すると、次のようなエラーメッセージが表示される場合があります。

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

問題を解決するには、次の手順に従います。

1. Finance and Operations アプリの仮想マシン（VM）にサイン インします。
2. Visual Studio を管理者で起動し、アプリケーション オブジェクト ツリー（AOT）を開きます。
3. **DualWriteProjectConfiguration** を検索します。
4. AOT で、**DualWriteProjectConfiguration** を右クリックし、**新しいプロジェクトに追加する**を選択します。 **OK** を選択すると、既定のオプションを使用した新たなプロジェクトが作成されます。
5. ソリューション エクスプローラーで、 **プロジェクトのプロパティ** を右クリックし、 **ビルド時にデータベースを同期する** を **True** に設定します。
6. プロジェクトをビルドし、ビルドが成功したことを確認します。
7. **Dynamics 365** メニューで、**データベースの同期** を選択します。
8. データベース全体の同期を実行するには、**同期** を選択します。
9. データベース全体の同期処理が正常に完了した後で、Microsoft Dynamics Lifecycle Services（LCS）でデータベースの同期を再実行し、必要に応じて手動アップグレードスクリプトを使用して、更新を進めることができます。

## <a name="missing-entity-fields-issue-on-maps"></a>マッピングに存在しないエンティティ フィールドの問題

**問題の修正に必要な役割：** システム管理者

**デュアル書き込み**ページでは、次のようなエラーメッセージが表示される場合があります。

*スキーマ内の 存在しないソース フィールド\<フィールド 名\>。*

![存在しないソース フィールドを示すエラー メッセージの例](media/error_missing_field.png)

この問題を解決するには、まず次の手順に従って、フィールドがエンティティに含まれていることを確認します。

1. Finance and Operations アプリの VM にログインします。
2. **ワークスペース \> データ管理** に移動して、**フレームワーク パラメータ** のタイルを選択し、**エンティティの設定** タブにて、 **エンティティ リストを更新する**を選択してエンティティを更新します。
3. **ワークスペース \> データ管理** に移動し、**データエンティティ** タブを選択して、エンティティが一覧表示されていることを確認します。 エンティティが一覧に表示されない場合は、当該 Finance and Operations アプリの VM にログインして、エンティティが使用可能となっていることを確認してください。
4. Finance and Operations アプリにて **デュアル書き込み** ページの **エンティティ マッピング** ページを開きます。
5. **エンティティ リストの更新** を選択すると、エンティティ マッピングのフィールドが自動的に入力されます。

問題が解決しない場合は、次の手順を実行してください。

> [!IMPORTANT]
> 次の手順に従い、エンティティを削除してから再度追加するプロセスを実行します。 問題を回避するには、手順を正確に守ってください。

1. Finance and Operations アプリで、**ワークスペース  \> データ管理** に移動し **、データ エンティティ** タイルを選択します。
2. フィールドが欠落しているエンティティを検索します。 対象のエンティティ、ステージング テーブル、ステージング エンティティ、およびその他の列の値をメモしておきます。
3. 処理グループがこのエンティティに依存している場合は、エンティティを削除する前に、処理グループに対して適切な処理を行ってください。
4. フィールドが欠落しているエンティティを削除します。
5. **新規** を選択し、エンティティを再度追加します。 手順 2 でメモした値を指定します。
6. Finance and Operations アプリにて **デュアル書き込み** ページの **エンティティ マッピング** ページを開きます。
7. **エンティティ リストの更新** を選択すると、エンティティ マッピングのフィールドが自動的に入力されます。

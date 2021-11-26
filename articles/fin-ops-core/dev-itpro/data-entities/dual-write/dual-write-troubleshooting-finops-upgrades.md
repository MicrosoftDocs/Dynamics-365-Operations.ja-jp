---
title: Finance and Operations アプリのアップグレードで生じる問題のトラブルシューティング
description: このトピックでは、Finance and Operations アプリの更新に関する問題の修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: db1602c2edaa2e6b6310cce04639ef7a8e43df15
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782784"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Finance and Operations アプリのアップグレードで生じる問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。 このトピックでは、Finance and Operations アプリの更新に関する問題の修正に役立つトラブルシューティングに特化した情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="database-synchronization-errors"></a>データベース同期のエラー

**問題の修正に必要な役割：** システム管理者

**DualWriteProjectConfiguration** テーブルを使用して、Platform update 30 に Finance and Operations アプリを更新すると、次の例のようなエラー メッセージが表示される場合があります。

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

問題を解決するには、次の手順に従います。

1. Finance and Operations アプリの仮想マシン（VM）にサイン インします。
2. Visual Studio を管理者で起動し、アプリケーション オブジェクト ツリー（AOT）を開きます。
3. **DualWriteProjectConfiguration** を検索します。
4. AOT で、**DualWriteProjectConfiguration** を右クリックし、**新しいプロジェクトに追加する** を選択します。 **OK** を選択すると、既定のオプションを使用した新たなプロジェクトが作成されます。
5. ソリューション エクスプローラーで、 **プロジェクトのプロパティ** を右クリックし、 **ビルド時にデータベースを同期する** を **True** に設定します。
6. プロジェクトをビルドし、ビルドが成功したことを確認します。
7. **Dynamics 365** メニューで、**データベースの同期** を選択します。
8. データベース全体の同期を実行するには、**同期** を選択します。
9. データベース全体の同期処理が正常に完了した後で、Microsoft Dynamics Lifecycle Services（LCS）でデータベースの同期を再実行し、必要に応じて手動アップグレードスクリプトを使用して、更新を進めることができます。

## <a name="missing-table-columns-issue-on-maps"></a>マップに存在しないテーブル列の問題

**問題の修正に必要な役割：** システム管理者

**デュアル書き込み** ページでは、次のようなエラーメッセージが表示される場合があります。

*スキーマ内の存在しないソース フィールド \<field name\>。*

![存在しないソース列のエラー メッセージの例。](media/error_missing_field.png)

この問題を解決するには、まず次の手順に従って、列がテーブルに含まれていることを確認します。

1. Finance and Operations アプリの VM にログインします。
2. **ワークスペース \> データ管理** に移動して、**フレームワーク パラメーター** タイルを選択し、**テーブルの設定** タブにて、**テーブル リストの更新** を選択してテーブルを更新します。
3. **ワークスペース \> データ管理** に移動し、**データ テーブル** タブを選択して、テーブルが一覧表示されていることを確認します。 テーブルが一覧に表示されない場合は、Finance and Operations アプリの VM にサインインして、テーブルが使用可能となっていることを確認してください。
4. Finance and Operations アプリにて **デュアル書き込み** ページの **テーブル マッピング** ページを開きます。
5. **テーブル リストの更新** を選択すると、テーブル マッピングの列が自動的に入力されます。

問題が解決しない場合は、次の手順を実行してください。

> [!IMPORTANT]
> これらの手順では、テーブルを削除してから再度追加するプロセスを示します。 問題を回避するには、手順を正確に守ってください。

1. Finance and Operations アプリで、**ワークスペース \> データ管理** に移動し、**データ テーブル** タイルを選択します。
2. 属性が欠落しているテーブルを検索します。 ツールバーの **ターゲット マッピングの変更** をクリックします。
3. **ステージングをターゲットにマッピング** ウィンドウで、**マッピングの生成** をクリックします。
4. Finance and Operations アプリにて **デュアル書き込み** ページの **テーブル マッピング** ページを開きます。
5. マッピング上で属性が自動設定されていない場合は、**属性の追加** ボタンをクリックして手動で追加し、**保存** をクリックします。 
6. マッピングを選択し、**実行** をクリックします。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
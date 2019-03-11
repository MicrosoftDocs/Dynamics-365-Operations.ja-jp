---
title: データベース移動操作
description: このトピックでは、Lifecycle Services のデータベース移動機能の一部として使用可能な操作について説明します。
author: laneswenka
manager: AnnBe
ms.date: 10/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 103674f8eefce840e3c6064d4b922b1ae69d4012
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369150"
---
# <a name="database-movement-operations"></a>データベース移動操作

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/private-preview-banner.md)]

このトピックでは、Lifecycle Services (LCS) のデータベース移動機能の一部として使用可能な操作について説明します。  

## <a name="sandbox-refresh"></a>サンドボックスの更新
実稼働環境をサンドボックス環境に、またはサンドボックス環境を別のサンドボックス環境に更新するときは、ターゲット環境にコピーされない特定のデータベース要素があります。  これらの要素として次のものがあります。
* LogisticsElectronicAddress テーブル内の電子メール アドレス。
* BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴。
* SysEmailSMTPPassword テーブルの SMTP パスワード。
* SysEmailParameters テーブルの SMTP 中継サーバー。
* PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定。
* SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード。
* DocuValue テーブル内のドキュメント添付ファイル。
* 管理者を除くすべてのユーザーが無効になります。
* すべてのバッチ ジョブは、[保留] 状態に設定されます。

## <a name="import"></a>インポート元
データベース バックアップをサンドボックス環境にインポートするときは、特定のアクティビティを実行する必要があります。  コピーされるフィールドは次のとおりです。
* 要件に従って、電子メール機能が正しく再設定または無効化されることを確認します。
* AOS サーバーが必要なバッチ グループに追加されます。
* システム ヘルプとタスク ガイドに再接続されます。
* バッチ ジョブは、[待機中] 状態に設定されます。
* ユーザーは再度有効になります。

## <a name="export"></a>輸出
環境からデータベース バックアップをエクスポートするときは、バックアップ ファイルにエクスポートされない特定のデータベース要素があります。  これらの要素として次のものがあります。
* LogisticsElectronicAddress テーブル内の電子メール アドレス。
* BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴。
* SysEmailSMTPPassword テーブルの SMTP パスワード。
* SysEmailParameters テーブルの SMTP 中継サーバー。
* PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定。
* SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード。
* DocuValue テーブル内のドキュメント添付ファイル。
* 管理者を除くすべてのユーザーが無効になります。
* すべてのバッチ ジョブは、[保留] 状態に設定されます。

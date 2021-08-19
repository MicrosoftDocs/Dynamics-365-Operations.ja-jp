---
title: AX 2012 からのアップグレード - データ アップグレード FAQ
description: このトピックでは、Microsoft Dynamics AX 2012からのアップグレードの際、データ アップグレードについてよく寄せられる質問に回答します。
author: ttreen
ms.date: 07/01/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: ttreen
ms.search.validFrom: 2021-07-01
ms.openlocfilehash: e8fefaa8fe1bbd2c8a69ca50f52c76280ebeb2b4
ms.sourcegitcommit: 41a5d18552bcc94cb1ddbbe3f3278eaf9d05f418
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/15/2021
ms.locfileid: "6617084"
---
# <a name="upgrade-from-ax-2012--data-upgrade-faq"></a>AX 2012 からのアップグレード – データ アップグレード FAQ

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics AX 2012からのアップグレードの際、データ アップグレードについてよく寄せられる質問に回答します。

## <a name="is-the-tier-2-azure-sql-database-sized-enough-for-upgrades-of-large-databases"></a>レベル 2 の Azure SQL データベースは、大規模なデータベースをアップグレードするのに十分なサイズですか?

データベースのサイズが増加した場合は、必要に応じて「エラスティック プール」に配置されるレベル 2 のサンドボックスのサイズが自動的に調整されます。

## <a name="does-the-ax-2012-database-upgrade-toolkit-for-dynamics-365-support-the-microsoft-government-community-cloud"></a>Dynamics 365 の AX 2012 データベース アップグレード ツールキットは、Microsoft Government Community Cloud をサポートしていますか?

いいえ。Dynamics 365 の AX 2012 データベース アップグレード ツールキットは、現在 Government Community Cloud (GCC) をサポートしていません。

## <a name="what-type-of-validation-is-done-as-part-of-the-ax-2012-database-upgrade-toolkit-for-dynamics-365"></a>Dynamics 365 の AX 2012 データベース アップグレード ツールキットの一部として実行される検証は、どのようなタイプですか?

Dynamics 365 の AX 2012 データベース アップグレード ツールキットの一部として実行される検証はほとんど行われません。 たとえば、ツールキットは、AX 2012 で必要な KB (前提条件) をインストールしたかどうかを検証します。 まだインストールしていない場合は、レプリケーション プロセスを開始できます。 レプリケートされたデータに対してレコード カウント チェックを実行するオプションもあります。

## <a name="what-is-the-recommended-approach-if-the-source-ax-2012-database-is-in-a-different-region-than-the-target-database"></a>ソース AX 2012 データベースがターゲット データベースとは別の地域にある場合、推奨される方法は?

レプリケーションのパフォーマンスを最適化するために、ソース AX 2012 データベースとターゲット データベースを同じ地域にすることをお勧めします。 ソースと同じ地域にサンドボックス環境を配置し、データ アップグレードを実行できます。 アップグレードが完了した後、サンドボックス環境を必要な地域に移動できます。

## <a name="are-the-sql-bacpac-and-dacpac-processes-still-supported-for-ax-2012-data-upgrades-in-sandbox-environments"></a>SQL BACPAC および DACPAC プロセスは、引き続きサンドボックス環境の AX 2012 データ アップグレードでもサポートされますか?

いいえ。SQL BACPAC および DACPAC プロセスは、サンドボックス環境の AX 2012 データ アップグレードではサポートされなくなりました。 Dynamics 365 の AX 2012 データベース アップグレード ツールキットを使用して、サンドボックス環境でデータをアップグレードする必要があります。

## <a name="ive-upgraded-an-ax-2012-database-in-a-dev-tier-1-environment-and-uploaded-the-upgraded-bacpac-file-into-lifecycle-services-however-i-receive-an-error-message-when-i-then-try-to-import-the-bacpac-file-into-a-sandbox-environment-how-do-i-fix-the-error"></a>AX 2012 のデータベースを、DEV (レベル 1) 環境にアップグレードし、アップグレードした BACPAC ファイルを Lifecycle Servicesにアップロードしました。 しかし、BACPAC ファイルをサンドボックス環境にインポートしようとすると、エラー メッセージが表示されます。 どのようにエラーを修正できますか?

アップグレードした BACPAC ファイルを Microsoft Dynamics Lifecycle Services (LCS) からサンドボックス環境にインポートしようとする場合、次のエラー メッセージが表示される場合があります。

> インポートされたデータが失われ、環境が失敗状態になるため、Dynamics 365 環境への AX 2012 bacpac ファイルのインポートはサポートされていません。

実行される検証により、プロジェクトの実装タイプが **AX2012 データ アップグレード** の場合、BACPAC ファイルはサンドボックス環境にインポートされなくなります。 データのアップグレードには、Dynamics 365 の AX 2012 データベース アップグレード ツールキットを使用する必要があります。また、データのアップグレードは、サンドボックス環境で行う必要があります。

## <a name="can-i-filter-on-the-table-data-that-will-be-replicated-for-example-to-limit-specific-records-only-for-replication-to-the-target-database"></a>レプリケートされるテーブル データでフィルター処理できますか (例: ターゲット データベースへのレプリケーションのみに特定のレコードを制限するなど)?

いいえ。Dynamics 365 の AX 2012 データベース アップグレード ツールキットは、レプリケートされるテーブル データのフィルター処理をサポートしていません。
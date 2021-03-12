---
title: ER 移行クリーンアップ
description: このトピックでは、ER 移行クリーンアップ機能を使用して ER テンプレートに関する問題を解決する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: edb60f247b2bd6cc4ecd514e3e85bafbb681788d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686371"
---
# <a name="er-migration-cleanup"></a>ER 移行クリーンアップ 

[!include[banner](../includes/banner.md)]

Finance インスタンスを管理する場合、現在のインスタンスを別の場所に移行する必要性が発生する場合があります。 たとえば、本番インスタンスを新しいサンドボックス環境に移行するかもしれません。 テンプレートを Microsoft Azure Blob ストレージに保存するように電子レポート（ER）フレームワークを構成した場合、新しいサンドボックス環境の **DocuValue** テーブルは、本番環境の Blob ストレージのインスタンスを参照します。 ただし、移行プロセスでは、Blob ストレージ内のアーティファクトの移行に対応していないため、このインスタンスにはサンドボックス環境からアクセスすることはできません。 新しいサンドボックス環境では、まだ ER のテンプレートを取得していないサンドボックス環境の Blob ストレージのインスタンスを参照することが予想されます。

したがって、テンプレートを使用して ER 形式を実行してビジネス ドキュメントを生成すると、例外が発生し、テンプレートが欠落していることが通知されます。 また、ER 移行クリーンアップ オプションを使用して、テンプレートを含む ER 形式の構成を削除してから再インポートする方法も紹介しています。

[![ER 形式の実行](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

**構成** ページ（**組織管理の** \> **電子レポートの構成** \> **構成**）に移動し、構成ツリーでテンプレートを使用したER 形式の構成を削除しようとした際には、同様のエラーが発生します。

[![ER 形式の削除](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

アクセスできない ER テンプレートの問題を解決するには、次の手順を実行してください。

1.  **組織管理** \> **定期** \> **移行クリーンアップ** ページに移動します。
2.  実行、削除できない ER 形式の構成を選択します。
3.  **削除** を選択します。
4.  選択したER形式の構成の削除を確認します。
5.  削除された ER 形式の構成を現在の Finance インスタンスを [インポート](download-electronic-reporting-configuration-lcs.md) します。

## <a name="applicability"></a>適合性

> [重要] **移行クリーンアップ** オプションは、 アクセスできない ER テンプレートを含む ER 形式の構成のみを対象としています。 **移行クリーンアップ** オプションを使用して ER 形式の構成を削除すると、ER はアプリケーション データベース内の構成アーティファクトのみに関連しているテンプレートを削除します。 Blob ストレージに適切な物理ファイルが存在するかどうかの検証はされません。 ここではむしろ存在しないことが前提となっています。 したがって、**構成** ページの ER 設定削除オプションの代わりに **移行クリーンアップ** オプション使用しないでください。 **移行クリーンアップ** オプションは、**構成** ページの ER 設定削除オプションが失敗した場合にのみ使用してください。
>
> 参照されたテンプレートが Blob ストレージで利用可能な場合に ER 形式の構成を削除する目的で **移行クリーンアップ**  オプションを使用すると、アプリケーション データベース内の関連する構成アーティファクトのみが削除されます。 Blob ストレージのテンプレートの物理ファイルは残ります。 Blob ストレージにおけるファイルの上書きは許可されなくなりました。 詳細については、[KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217) を参照してください。 また、この環境で移行のクリーンアップを使用して削除した構成を再度インポートすることもできなくなります。 この問題を解決するには、対応するファイルを Blob ストレージで検索し、手動で削除する必要があります。

[![ER 形式のインポート](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

アプリケーション インスタンスを移行対象として複数回使用されている場所に移行した場合で、Blob ストレージに ER のテンプレート ファイルがすでに含まれている場合にも、同様の問題が発生する可能性があります。

ER 形式の構成が複数存在する場合があるため、このプロセスには時間がかかる場合があります。 したがって、[ER テンプレートのバックアップ ストレージ](er-backup-storage-templates.md) 機能を使用して、壊れた参照を含むテンプレートを自動的に回復することを推奨します。

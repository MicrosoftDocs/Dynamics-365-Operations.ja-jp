---
title: Dynamics AX 2012 からのドキュメントの添付ファイルの移行する
description: このトピックでは、Microsoft Dynamics AX 2012 からドキュメントの添付ファイルを移行する方法について説明します。
author: ttreen
ms.date: 04/26/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: ttreen
ms.search.validFrom: ''
ms.search.form: 2022-04-08
ms.openlocfilehash: c7f7bb853e40c95008fc26461bb72a9ca48c32da
ms.sourcegitcommit: 5130446fd5327595b2d67e67cbd1b5661bb2983c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648756"
---
# <a name="migrate-document-attachments-from-dynamics-ax-2012"></a>Dynamics AX 2012 からのドキュメントの添付ファイルの移行する

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics AX 2012 からドキュメントの添付ファイルを移行する方法について説明します。

## <a name="background"></a>背景

Dynamics AX 2012 では、添付ファイルはファイル共有、データベース、またはローカル SharePoint サーバーなど複数の場所に格納されます。 添付ファイルの保存先は、ファイル タイプごとに **ドキュメント タイプ** フォームで設定します。

Dynamics 365 Finance + Operations (on-premises) では、添付ファイルは多くの場合、環境に割り当てられたプライベートの Azure Blob Storage の場所に格納されます。 または、顧客のテナントの下にある SharePoint オンライン サイトにリンクされている場合もあります。

添付ファイルは、アップグレードが行われる前に Dynamics AX 2012 データベースに移行した場合にのみ、Dynamics AX 2012 からのアップグレード後に Dynamics 365 で使用できます。 アップグレード後の手順で、それらを Blob Storage の場所に移行します。

## <a name="migration-options"></a>移行オプション

Dynamics AX 2012 からドキュメントの添付ファイルを移行するには、2 つのオプションがあります。 それらは、データベースの場所またはファイル共有の場所から移行できます。

> [!NOTE]
> 現在、ローカル SharePoint サイトからの添付ファイルの移行はサポートされていません。

### <a name="option-1-migrate-attachments-from-a-database-location"></a>オプション 1: データベースの場所から添付ファイルを移行する

Dynamics AX 2012 データベースの **DocuValue** テーブルに格納するよう既に設定されている添付ファイルにはアクションは必要はありません。

### <a name="option-2-migrate-attachments-from-a-file-share-location"></a>オプション 2: ファイル共有の場所から添付ファイルを移行する

Dynamics AX 2012 環境のファイル共有に格納された添付ファイルは、Dynamics AX 2012 データベースに移行する必要があります。 詳細については、[ドキュメントを共有場所からデータベースに移動する](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/AX2012DataUpgrade/MoveDocumentsToDatabase)を参照してください。

## <a name="post-upgrade-steps"></a>アップグレード後の手順

アップグレードが完了した後、Dynamics AX 2012 データベースに格納されている既存のドキュメントや添付ファイルを Blob Storage に移行する必要があります。

この移行をするには、**ドキュメント管理パラメーター** ページの **ファイルを移行** タブで、**ファイルを移行** を選択します。 ドキュメント管理ではデータベースに格納されているファイルに引き続きアクセスできるため、この操作は重要ではありません。 ただし、ファイルはかなりのデータベース ストレージを消費する可能性があり、データベースからの取得は効率が低下します。 ファイル移行プロセスでは、すべての可能なデータベース ファイルが Blob Storage に移行されます。 エラーが発生した場合は、プロセスは報告されますが移行は続行されます。 エラーが報告された場合は、ファイル移行プロセスを再度実行します。

> [!NOTE]
> 運用フェーズ中は、[セルフサービス データベースのプロセスを最新情報に更新](../database/database-refresh.md#self-service-database-refresh)を完了し、アップグレードされたデータベースをサンドボックス環境から運用環境にコピーするまで添付ファイルを移行しないでください。 そうしない場合、添付ファイルは運用環境ではなくサンドボックス Blob Storage の場所に移行されるため、運用環境では使用できません。

ファイルの移行プロセスが正常に完了しない場合、データベースに保存されているファイルに損傷があることが考えられます。 この場合、Microsoft はファイルを修復できません。 ただし、業務に不可欠とならないサポート案件を開いて、添付ファイルをメモ レコードに変換できるようにすることができます。 これらのメモ レコードには、以前のメモとデータベースに保存されたファイルの名前が保持されます。 ファイル自体を復元することはできません。

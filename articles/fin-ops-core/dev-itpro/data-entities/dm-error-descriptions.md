---
title: データ管理エラーの説明
description: このトピックでは、データ管理で発生する可能性があるエラー メッセージについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 25341
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-09-15
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: de55489d0bc5be9f57b6882211607c1fbf5eb4ba
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685679"
---
# <a name="data-management-error-descriptions"></a>データ管理エラーの説明

[!include [banner](../includes/banner.md)]

このトピックでは、特定のエラーが表示されるときのシナリオを示します。 これらのシナリオは、エラーとシナリオの完全な一覧ではありませんが、このリストは継続的に更新されるため、最新情報をチェックしてください。 特定のエラーが扱われるべきかどうかに関するこのページのフィードバックをお送りください。

このトピックでは、データ管理で発生する可能性があるエラー メッセージについて説明します。

## <a name="import-to-target-failed-due-to-an-update-conflict-as-more-than-one-process-is-trying-to-update-the-same-record-at-the-same-time"></a>複数のプロセスとしての更新競合のために失敗したターゲットへのインポートが、同じレコードを同時に更新しようとしている

定期的なインポート (API をキューに入れる) を使用するとき、頻度の高いのエンドポイントにファイルが送信され、連続したメッセージの処理が有効になっていない場合、データ管理は同時にファイルを処理しようとします。 ファイルが並行で処理され、複数のファイルが同一のレコードを持つ場合、複数のスレッドが同時に同じレコードを更新しようとします。 これがデータの問題である場合、ファイルの間で同じレコードが繰り返さないように、データを更新する必要があります。 これがデータの問題ではなく、エンティティがこのようなケースを処理すると予測される場合は、バグの可能性があります。 不具合の場合、問題を軽減するため、順番にファイルを処理することを選択できます。 これがデータの問題ではなく、エンティティが並行処理することが予想されない場合、このエンティティが並列処理の対象でない可能性があります。 定期的なジョブ内のメッセージの連続した処理を有効にする必要があります。

## <a name="there-are-fields-which-are-not-mapped-to-entity-entityname"></a>エンティティ \<EntityName\> にマップされていないフィールドがあります

一般的には、後でインポートに使用できるエンティティ テンプレート ファイルを生成するためにエクスポート機能を使用します。 ただし、"最初の行ヘッダー" が "いいえ" になっている固定長形式でテンプレートをエクスポートしますが (設定されたソース データ形式で)、エクスポートしたテンプレートには列の名前がありません。 このファイルのインポート時、このエラーが発生します。 

## <a name="data-package-download---error-downloading-data-package-for-job--record-for-id---guid-not-found"></a>データ パッケージ ダウンロード - ジョブ '' のデータ パッケージのダウンロード エラーです。 ID - {GUID} のレコードが見つかりません

このエラーが発生するシナリオの 1 つは、開発環境などの環境が UAT などの別の環境にあるデータベースをポイントしており、エクスポート ジョブがソース環境から実行される場合などです。 この例では、開発です。 エクスポートしたファイルは、ソース環境 (この例では開発) に関連付けられている blob ストレージにアップロードされます。 ただし、データベースが共有されているため、このジョブはターゲット環境 (UAT) にも表れます。 **ファイルのダウンロード** オプションを使用してエクスポートしたファイルをダウンロードしようとする場合、ダウンロード元となるターゲット環境 (UAT) の Blob ストレージにファイルが存在しないために、このエラーが表示されます。

## <a name="xml-is-not-in-correct-format-exception-from-hresult-0xc0010009"></a>XML が正しい形式ではありません-HRESULT: 0xC0010009 からの例外

このメッセージは、ファイルにおける XML 形式のすべての問題をカバーします。 たとえば、データ プロジェクトには、操作に使用されているファイルに存在しない列のマッピングがあります。 このエラーは、ファイルから特定の列が削除され、このファイルが使用される場合に発生する可能性があります。 データ プロジェクトでマッピングを修正するか、すべての列が正常に存在するようにファイルを修正します。

## <a name="error-while-uploading-a-file-during-export"></a>エクスポート時のファイルのアップロード中にエラーが発生する

開発環境でエクスポート処理をした際に、エクスポートファイルのアップロードができない旨のエラーが発生する。 これは、Azure Storage エミュレーターが使用できないか、旧バージョンの エミュレーター が インストール されている場合に発生する可能性があります。 この問題を解決するには、最新のエミュレータをインストールし、仮想マシン (VM) を再起動の上、エクスポート ジョブを再実行してください。 ストレージのエミュレーターは [Azure Storage エミュレーター](https://docs.microsoft.com/azure/storage/common/storage-use-emulator) からインストールすることができます。


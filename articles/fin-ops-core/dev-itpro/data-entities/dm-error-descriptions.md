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
ms.search.scope: Operations
ms.custom: 25341
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-09-15
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 894eb3b19fe26f2b7b5f8f1f9a930f4ddabfc2e7
ms.sourcegitcommit: c237123ad94d9418994ac095fbd8634c05a927b1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943276"
---
# <a name="data-management-error-descriptions"></a>データ管理エラーの説明
このトピックでは、特定のエラーが表示されるときのシナリオを示します。 これはエラーとシナリオの完全な一覧ではありませんが、このリストは継続的に更新されるため、最新情報をチェックしてください。 特定のエラーが扱われるべきかどうかに関するこのページのフィードバックをお送りください。 このトピックが最新の状態になるように、フィードバック依頼を優先するよう努めます。

[!include [banner](../includes/banner.md)]

このトピックでは、データ管理で発生する可能性があるエラー メッセージについて説明します。

## <a name="import-to-target-failed-due-to-an-update-conflict-as-more-than-one-process-is-trying-to-update-the-same-record-at-the-same-time"></a>複数のプロセスとしての更新競合のために失敗したターゲットへのインポートが、同じレコードを同時に更新しようとしている
定期的なインポート (API をキューに入れる) を使用するとき、頻度の高いのエンドポイントにファイルが送信され、連続したメッセージの処理が有効になっていない場合、データ管理は同時にファイルを処理しようとします。 ファイルが並行で処理され、複数のファイルが同一のレコードを持つ場合、複数のスレッドが同時に同じレコードを更新しようとします。 これがデータの問題である場合、ファイルの間で同じレコードが繰り返さないように、データを更新する必要があります。 これがデータの問題ではなく、エンティティがこのようなケースを処理すると予測される場合は、バグの可能性があります。 不具合の場合、問題を軽減するため、順番にファイルを処理することを選択できます。 これがデータの問題ではなく、エンティティが並行処理することが予想されない場合、このエンティティが並列処理の対象でない可能性があります。 定期的なジョブ内のメッセージの連続した処理を有効にする必要があります。 

## <a name="there-are-fields-which-are-not-mapped-to-entity-ltentitynamegt"></a>エンティティ &lt;EntityName&gt; にマップされていないフィールドがあります
後でインポートに使用できるエンティティ テンプレート ファイルを生成するためにエクスポート機能を使用することをお勧めします。 ただし、"最初の行ヘッダー" が "いいえ" になっている固定長形式でテンプレートをエクスポートしますが (設定されたソース データ形式で)、エクスポートしたテンプレートには列の名前がありません。 このファイルのインポート時、このエラーが発生します。 

## <a name="data-package-download---error-downloading-data-package-for-job--record-for-id---guid-not-found"></a>データ パッケージ ダウンロード - ジョブ '' のデータ パッケージのダウンロード エラーです。 ID - {GUID} のレコードが見つかりません
これが発生するシナリオは、開発環境などの環境が UAT などの別の環境にあるデータベースをポイントしており、エクスポート ジョブがソース環境から実行される場合などがあります。 この例では、開発です。 エクスポートしたファイルは、ソース環境 (この例では開発) に関連付けられている blob ストレージにアップロードされます。 ただし、データベースが共有されているため、このジョブはターゲット環境 (UAT) にも表れます。 **ファイルをダウンロード**オプションを使用してエクスポートしたファイルをダウンロードしようとする場合、ダウンロード元となるターゲット環境 (UAT) の blob ストレージにファイルが存在しないために、このエラーが表示されます。

## <a name="xml-is-not-in-correct-format-exception-from-hresult-0xc0010009"></a>XML が正しい形式ではありません-HRESULT: 0xC0010009 からの例外
これは、ファイルにおける XML 形式のすべての問題をカバーする汎用メッセージです。 たとえば、データ プロジェクトには、操作に使用されているファイルに存在しない列のマッピングがあります。 これは、ファイルから特定の列が削除され、このファイルがすぐに使用される場合に発生する可能性があります。 データ プロジェクトでマッピングを修正するか、すべての列が正常に存在するようにファイルを修正します。

## <a name="error-while-uploading-a-file-during-export"></a>エクスポート時のファイルのアップロード中にエラーが発生する
開発環境でエクスポート処理をした際に、エクスポートファイルのアップロードができない旨のエラーが発生する。 これは、Azure のストレージ エミュレータが使用できないか、旧バージョンの エミュレータ が インストール されている場合に発生する可能性があります。 この問題を解決するには、最新のエミュレータをインストールし、仮想マシン (VM) を再起動の上、エクスポートのジョブを再実行してください。 ストレージのエミュレータは [Azure ストレージ エミュレータ](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-emulator) からインストールすることができます。


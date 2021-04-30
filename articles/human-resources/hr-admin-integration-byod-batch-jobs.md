---
title: BYOD でスケジュール設定されたバッチ ジョブを最適化する
description: このトピックでは、Microsoft Dynamics 365 Human Resources でデータベースの持ち込み (BYOD) 機能を使用している場合のパフォーマンスの最適化方法について説明します。
author: andreabichsel
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: a63ff89a6fcbffc57eff14f310a080a35521ef34
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890079"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>BYOD でスケジュール設定されたバッチ ジョブを最適化する

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、データベースの持ち込み (BYOD) 機能を使用している場合のパフォーマンスの最適化方法について説明します。 詳細については、[自分のデータベースの持ち込み (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)を参照してください。

## <a name="performance-considerations-for-data-export"></a>データ エクスポートのパフォーマンスに関する考慮事項

エンティティが宛先データベースに公開された後、**データ管理** ワークスペースのエクスポート機能を使用してデータを移動することができます。 エクスポート関数を使用すると、1 つまたは複数のエンティティが含まれるデータ移動ジョブを定義できます。 データのエクスポートについての詳細情報は、[データのインポート ジョブとエクスポート ジョブの概要](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json) を参照してください。

**エクスポート** ページを使用すると、データをコンマ区切り値 (CSV) ファイルなどの様々なターゲットのデータ書式にエクスポートすることができます。 このページは、別の宛先として SQL データベースもサポートしています。

複数のエンティティを持つデータ プロジェクトを作成し、バッチジョブを使用してそのデータ プロジェクトの実行をスケジュールすることができます。 また、**バッチ処理でエクスポート** オプションを選択することにより、データ エクスポート ジョブを定期的に実行することができます。

BYOD エクスポートの全体的な信頼性を維持するために、エクスポート プロジェクトに複数のエンティティを追加する場合は注意する必要があります。 同じプロジェクトに追加するエンティティの数を決定する際には、以下のパラメーターを考慮してください。

- エンティティの複雑性
- エンティティごとの予想されるデータ量
- ジョブ レベルでエクスポートを完了するにあたって必要となる全体的な時間

最高のパフォーマンスを得るには、1つのプロジェクトにたくさんののエンティティを追加しないでください。 複数のジョブを作成し、各ジョブに含まれるエンティティ数を削減することをお勧めします。

## <a name="scheduling-byod-batch-jobs"></a>BYOD バッチ バッチジョブのスケジュール設定

Microsoft Dynamics 365 Human Resources のユーザーへの影響を軽減するには、夜間または業務時間外に BYOD バッチジョブを実行してください。 これらの定期的なバッチ ジョブを実行するタイム ゾーンを確認してください。 一部のバッチ ジョブは、太平洋標準時 (PST) を使用している場合があります。

パフォーマンスの問題を回避するために、BYOD バッチジョブのスケジューリング頻度を公正する際は、次の要素を考慮してください :

- 各バッチジョブの完了までに必要となる時間
- BYOD のデータに対する業務上のニーズ

各バッチジョブの頻度を設定して、次にスケジュール設定された実行時間よりも前にジョブを完了できるようにしてください。 この方法は、Human Resources のパフォーマンスに悪影響を及ぼす可能性があるため、複数のジョブを並行して実行しないようにしてください。

最高のパフォーマンスを得るためには、**エクスポート** ページの **バッチ処理でエクスポート** オプションを使用して、BYOD バッチジョブをスケジュール設定してください。 **管理 \> 定期データ ジョブの管理** にて定期的なスケジュール設定されたエクスポートを回避します。

## <a name="incremental-export"></a>差分エクスポート

データ エクスポートにエンティティを追加する場合は、増分プッシュ (エクスポート) またはフル プッシュのいずれかを行うことができます。 フル プッシュは、BYOD データベースのエンティティから既存のレコードをすべて削除します。 続いて、Human Resources エンティティから現在のレコードセットを挿入します。

増分プッシュを実行するには、**エンティティ** ページで各エンティティの変更の追跡を有効にする必要があります。 詳細については、 [エンティティへの変更の追跡を有効化する](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)を参照してください。

増分プッシュを選択した場合、最初のプッシュは常に完全なプッシュになります。 SQL は、この最初の完全プッシュからの変更を追跡します。 新しいレコードが挿入される、またはレコードが追加または削除されるたびに、これら変更が宛先エンティティに反映されます。

## <a name="time-outs"></a>タイムアウト

BYOD エクスポートの既定のタイムアウトを示します :

- トランケート処理では 10分間
- 一括挿入処理では 1 時間

ボリュームが多い場合、これらのタイムアウト設定の時間内に処理が完了しない場合があります。 これらを変更するには、**データ管理 \> フレームワークパラメータ \> 独自のデータベース** に移動します。 タイムアウトは会社ごとに固有の設定となるため、それぞれの会社ごとに個別に設定する必要があります。

## <a name="known-limitations"></a>既知の制限

BYOD 機能には、次の制限があります :

- 同期中のデータベースにはアクティブなロックが存在してはいけません。 アクティブなロックが存在すると、Azure SQL database へのデータのエクスポート時に、書き込速度の低下や失敗が発生する場合があります。
- 独自のデータベースには、複合のエンティティをエクスポートすることはできません。 現在、複合エンティティがサポートされていません。 複合エンティティを構成する個々 のエンティティをエクスポートする必要があります。 ただし、同じデータ プロジェクト内では両方のエンティティをエクスポートすることができます。
- 固有のキーを持たないエンティティは、増分プッシュを使用してのエクスポートはできません。 この制限は特に、数個の既製エンティティからレコードを段階的にエクスポートする場合に直面する可能性があります。 これらのエンティティはデータをインポートできるように設計されているため、固有のキーはありません。

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="incremental-push-doesnt-work-correctly"></a>増分プッシュが正常に機能しない

**問題 :** あるエンティティに対してフルプッシュが実行された場合、**セレクト** 文を使用すると BYOD で大量のレコードセットが表示されます。 しかし、増分プッシュを行うと、BYOD では数件のレコードしか表示されません。 増分プッシュですべてのレコードが削除され、BYOD で変更したレコードだけが追加されたように見えます。

**解決策 :** SQLの変更追跡テーブルがしかるべき状態になっていない可能性があります。 このような場合は、エンティティの変更の追跡をオフにしてからオンに戻すことをお勧めします。 詳細については、 [エンティティへの変更の追跡を有効化する](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)を参照してください。

## <a name="see-also"></a>参照

[データ管理の概要](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[自分のデータベースの持ち込み (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[データ インポート/エクスポート ジョブの概要](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[エンティティの変更追跡の有効化](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
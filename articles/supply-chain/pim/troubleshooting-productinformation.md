---
title: 製品情報のトラブルシューティング
description: このトピックでは、製品情報を操作する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4c505ccfd1998acd40dbae715c7fa572e315af2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007519"
---
# <a name="troubleshoot-product-information"></a>製品情報のトラブルシューティング

このトピックでは、製品情報を操作する際に発生する可能性がある問題の修正方法について説明します。

## <a name="i-cant-delete-a-released-product"></a>リリースされた製品を削除できません。

### <a name="issue-description"></a>問題の説明

リリースされた製品およびそのすべてのバリアントは、リリースされた製品に関連するトランザクションが存在しない場合にのみ削除できます。

### <a name="issue-resolution"></a>問題の解決

リリースされた製品または製品マスターを削除するには、次の手順に従います。

1. 品目の未処理トランザクションをすべて閉じます。
1. 在庫を 0 (ゼロ) に減らします。
1. 在庫計算を実行します。
1. 削除する製品マスターのすべての製品バリアントを削除します。

## <a name="can-i-change-the-item-number-of-a-released-product"></a>リリースされた製品の品目番号を変更できますか。

ほとんどの場合、この変更によってデータが破損するため、リリースされた製品の品目番号を編集できません。 この品目番号を編集できるのは、リリースされた製品の主キーを以前名前変更したことにより発生したデータの破損を修復する必要がある場合のみです。これについては、[Platform update 24 により Finance and Operations 10.0.0 で削除または廃止された機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24)の一覧に掲載されています。

リリースされた製品の品目番号を編集できるようにする場合は、[アイデア ポータルでこのアイデアに投票](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25)してください。

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>製品からの既定の部品消費ルールが部品表明細行に入力されていません。

### <a name="issue-description"></a>問題の説明

部品表 (BOM) 明細行に品目を追加しても、その品目に対して設定されている既定の部品消費ルール情報は使用されません。 つまり、品目からの部品消費ルールは **BOM 明細行** ページに表示されません。

### <a name="issue-resolution"></a>問題の解決

BOM 明細行で部品消費ルールを指定した場合、その BOM 明細行に適用されます。 ただし、部品消費ルールが空白の場合、または BOM 明細行で設定されていない場合は、BOM 明細行に表示されなくても、その BOM 明細行には品目に対して設定されている部品消費ルールが適用されます。

通常、Microsoft Dynamics 365 Supply Chain Management のその他の機能の既定のロジックでは、この方法は使用されません。 ただし、現在の動作を変更することはできません。 そうしないと、それに依存する既存のカスタマイズの一部が失われることがあります。

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>システムでは、さまざまな品目または分析コードが異なる同じ品目に対して重複するバーコードを保存できます。

現在は、システムによって固有のバーコードが適用されておらず、この制限の追加は破壊的変更となります。 実際、Microsoft では、この変更によってお客様の既存のインストールが壊れるという証拠を持っています。 ただし、将来この機能を有効にするため、より広範な設計変更を検討する予定です。

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>品目レコード テンプレートを編集すると、エラー メッセージ "品目の在庫がないため、倉庫の場所を作成できません。 品目の在庫を確保するには、関連付けられている品目モデル グループの在庫製品オプションを選択する必要があります" が表示されます。

### <a name="issue-description"></a>問題の説明

この問題は、次の手順に従って、在庫のない品目のテンプレートを作成しようとした場合に発生します。

1. まだ在庫のないリリース済製品を開きます。
1. アクション ペインの **オプション** タブで、**レコード情報** を選択します。
1. **レコード情報** ダイアログ ボックスで、**会社コード テンプレート** を選択します。

この場合、次のエラー メッセージが表示されます。

> 品目の在庫がないため、倉庫の場所を作成できません。 品目の在庫を確保するには、関連付けられている品目モデル グループの在庫製品オプションを選択する必要があります。

### <a name="issue-resolution"></a>問題の解決

製品テンプレートを作成するプロセスには、追加の製品固有のロジックが必要です。 したがって、この目的では、汎用の **会社コード テンプレート** ボタンを使用することはできません。 代わりに、以下の手順を実行します。

1. リリース済製品を開きます。
1. アクション ペインで、**製品** タブの **新規** グループで、**テンプレート \> 共有テンプレートの作成** を選択します。

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>製品属性に追加された既定のヘルプ テキストは、リリース済み製品に入力されません。

製品属性に追加された説明およびヘルプ テキストは、リリース済み製品では既定で表示または入力できません。 この動作は仕様です。

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>入力される既定の数量が、BOM から登録されるときと、BOM バージョンから登録されたときで異なります。

### <a name="issue-description"></a>問題の説明

既定では、BOM に品目を追加すると、数量が、選択された製品の **既定の注文設定** ページの **最小注文数量** フィールドで定義されている数量ではなく、1 に設定されます。 ただし、BOM バージョンから品目を追加する場合で、品目とバリアントが選択されている場合、既定で入力された数量は、特定の分析コードに対する既定の注文設定で設定された最小数量を考慮します。

### <a name="issue-resolution"></a>問題の解決

この動作は予期されています。 ただし、BOM ではロジックが異なり、BOM バージョンは既知の問題であるという事実もあります。 それでも、変更はさまざまな顧客のシナリオに影響する可能性があるため、この動作は変更されません。

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>リリース済み製品の詳細では、製品ドキュメントの添付ファイル データ エンティティからアップロードされた添付画像を変更することはできません。

### <a name="issue-description"></a>問題の説明

この問題は、*製品ドキュメントの添付ファイル* データ エンティティを使用して画像を品目に関連付けた場合に発生することがあります。 この場合、品目の品目画像が表示されます。 ただし、**画像の変更** を選択した場合、アップロードした画像の一覧には何も表示されません。 また、この品目の添付ファイルは表示されません。

### <a name="issue-resolution"></a>問題の解決

*EcoResProductDocumentAttachmentEntity* エンティティ (*製品ドキュメントの添付ファイル*) は、*製品* のドキュメント添付ファイルをインポートしますが、*リリース済製品* の添付ファイルはインポートしません。 (リリース済み製品は *品目* と呼ばれることもあります)。**リリース済み製品の詳細** ページで、品目の添付ファイルを表示するには、代わりに *EcoResReleasedProductDocumentAttachmentEntity* エンティティ (*リリース済み製品ドキュメント添付ファイル*) を使用する必要があります。

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>Microsoft Flow コネクタに、エラーメッセージ "ProductNumber フィールドの更新は許可されていません" が表示されます。

### <a name="issue-description"></a>問題の説明

この問題は、*リリース済み製品* エンティティ V2 と Microsoft Flow を使用して **製品番号** フィールドを更新しようとすると発生します。

### <a name="issue-resolution"></a>問題の解決

この動作は予期されています。 リリース済み製品の製品番号を編集する機能は、データの破損を防ぐため、Dynamics 365 Finance and Operations 10.0.0 プラットフォーム更新プログラム 24 で削除されました。 リリース済み製品の主キーの以前の名前変更によって発生したデータ破損を修復する必要がある例外的なケースでは、Microsoft サポートに対して、この制限を一時的に解除するように依頼することができます。

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>別の法人にリリース済の製品バリアントを作成できません。

### <a name="issue-description"></a>問題の説明

バリアントを指定しないで製品マスターをリリースし、必要に応じて各法人 (会社) にバリアントを作成する場合は、バリアントの提案を使用してバリアントをリリースすることはできません。 バリアントを手動で作成することもできません。

### <a name="issue-resolution"></a>問題の解決

この動作は仕様です。 製品マスターの関係と、マスターで実行できる分析コードは、共有レベルで維持されます。 したがって、これらの分析コードがリリースされた特定の法人で共有の製品マスターに対して使用できる分析コードを作成し、分析コードが必要な各法人にプロセスをレプリケートすることはできません。 代わりに、設計されたプロセスに対応するようにリリース プロセスを変更する必要があります。

製品のリリース プロセスは次のとおりです。

1. 法人にリリースできる共有製品マスターと分析コードを作成します。
1. バリアント提案を使用するか、リリースする必要のある組み合わせを手動で追加することによって、製品を法人にリリースします。

または、リリース済み製品を直接作成することもできます。

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>別の会社でバリアントをリリースすると、エラー メッセージ "指定された分析コードを持つ商品バリエーションは既に作成されています" が表示されます。

### <a name="issue-description"></a>問題の説明

製品バリアントが会社 A で既にリリースされている場合に、**リリース済み製品バリアント** ページの **新規** ボタンを使用して会社 B でそのバリアントをリリースしようとすると 、次のエラー メッセージが表示されます。

> 指定された分析コードを持つ製品バリアントは、既に作成されています。

### <a name="issue-resolution"></a>問題の解決

**リリース済製品バリアント** ページの **新規** ボタンをクリックするとバリアントが作成され、会社コンテキストでリリースされます。 バリアントが既に作成されている場合は、**新規** ボタンを使用して別の会社にリリースすることはできません。

この問題を解決するには、**製品マスター** ページを開き、**製品のリリース** を選択して、目的の会社の既存のバリアントをリリースします。

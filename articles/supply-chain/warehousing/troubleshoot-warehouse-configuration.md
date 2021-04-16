---
title: 倉庫コンフィギュレーションのトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management を構成する際に発生する可能性がある一般的な問題の修正方法について説明します。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814395"
---
# <a name="troubleshoot-warehouse-configuration"></a>倉庫コンフィギュレーションのトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management を構成する際に発生する可能性がある一般的な問題の修正方法について説明します。

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>"ライセンス プレートまたは場所が有効ではありません" というエラー メッセージが表示されます。

### <a name="issue-description"></a>問題の説明

ライセンス プレート ID または場所をスキャンすると、このエラー メッセージが表示されます。

### <a name="issue-resolution"></a>問題の解決

ライセンス プレート ID が別のものによって予約されていないことを確認してください。 この問題は、倉庫管理モバイル アプリでユーザーがスキャンした値が有効な場所と有効なライセンス プレート ID の両方である場合に発生します。 ただし、この問題はバージョン 10.0.11 で解決されました。

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>"この場所にはライセンス プレートを指定する必要があります" というエラー メッセージが表示されます。

### <a name="issue-description"></a>問題の説明

このエラー メッセージは、高度な倉庫管理 (WMS) が有効になっている倉庫を使用して移動オーダーを作成し、作業が完了した後、出荷を確認しようとした場合に表示されます。

### <a name="issue-resolution"></a>問題の解決

"移動元" 倉庫の流通倉庫の **既定の受入場所** フィールドが空白になっています。 この問題を解決するには、流通倉庫の既定の受入場所を指定します。 この場所がライセンス プレートによって制御されていることを確認してください。

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>エラー メッセージ "作業タイプが無効なので、在庫ステータスを変更するための作業テンプレート行を作成できません。 別の作業タイプを選択してください" が表示されます。

### <a name="issue-description"></a>問題の説明

作業テンプレートの場合、**作業テンプレートの詳細** セクションの **作業タイプ** 列で *在庫ステータスの変更* を選択することはできません。

### <a name="issue-resolution"></a>問題の解決

この動作は仕様です。 *在庫ステータス変更* 作業タイプは、システム プロセスでのみ使用されます。 この値は構成できません。 作業タイプのリストは列挙として固定されているため、追加のエントリを **作業タイプ** ドロップダウン メニューからフィルターで除外することはできません。

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>"単位 1% の数量が有効ではありません" というエラー メッセージが表示されます。

### <a name="issue-description"></a>問題の説明

複数のライセンス プレートを含むピッキング作業が 1 つの場所にある場合に、*ea* 単位の数量が無効です。

### <a name="issue-resolution"></a>問題の解決

リリース済み製品または製品バリアントの **単位順序グループ ID** フィールドと **単位換算** フィールドが正しく設定されていることを確認します。

バージョン 10.0.15 では、エラー メッセージが改善されていることに注意してください ([KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531) を参照)。 新しいエラー メッセージは、"数量が無効です。 期待値: %1 %2" です。

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>販売注文のプット作業の場所ディレクティブでは、複数の SKU オプションにより複数の場所ディレクティブのアクションが評価されることはありません。

### <a name="issue-description"></a>問題の説明

**複数 SKU** オプションが選択されているときは、*販売注文* 作業指示タイプおよび *プット* 作業タイプの場所ディレクティブにより、複数の場所ディレクティブ アクションが評価されることはありません。 最初の場所ディレクティブ アクションのみが評価されます。

### <a name="issue-resolution"></a>問題の解決

バージョン 10.0.15 では、新しい機能 *複数の SKU の場所ディレクティブのすべてのアクションを評価する* が追加されています ([KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091) を参照)。 この機能は、複数 SKU の場所ディレクティブのすべてのアクションを評価します。 この機能が必要な場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用してオンにします。

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a>倉庫管理モバイル アプリを使用して部分的なピッキングを実行できません。

### <a name="issue-description"></a>問題の説明

販売注文および移動オーダーの場合は、品目のスキップや部分ピッキングを行うことはできません。

### <a name="issue-resolution"></a>問題の解決

販売注文または移動オーダーを処理するように設定されているメニュー項目ごとに、**モバイル デバイス メニュー項目** ページで、**全般** クイックタブの **作業の分割を許可する** オプション を *はい* に設定します。

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>部分的な数量作業に対して在庫ステータスの変更を行うにはどうすればよいですか。

### <a name="issue-description"></a>問題の説明

バッチの一部の数量の在庫ステータス変更を行おうとしています。

### <a name="issue-resolution"></a>問題の解決

作業者がこの変更を行うことができるようにするには、倉庫管理モバイル アプリのメニュー項目を作成します。 **モバイル デバイスのメニュー項目** ページで、次の設定を持つメニュー項目を作成 (または編集) します。

- **モード:** *作業*
- **既存の作業を使用する :** *いいえ*
- **作業作成プロセス:** *移動*
- **在庫状態の表示:** *はい*

必要に応じて、ページの他のフィールドを設定できます。

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a>場所プロファイルのドック管理プロファイルは、在庫タイプの混合を防ぎません。

### <a name="issue-description"></a>問題の説明

*出荷連結ポリシー* を使用しています。 *場所プロファイル* の *ドック管理プロファイル* を設定しましたが、作業の作成時には、最終的な場所で在庫タイプが混合します。

### <a name="issue-resolution"></a>問題の解決

ドック管理プロファイルでは、事前に作業を分割する必要があります。 つまり、ドック管理プロファイルでは、作業ヘッダーに複数のプット場所がないことを想定しています。

ドック管理プロファイルで在庫の混合を効果的に管理するには、作業ヘッダーの区切りを設定する必要があります。

この例では、ドック管理プロファイルは **混合しない在庫タイプ** を *出荷 ID* に設定されるように構成しています。その場合は、作業ヘッダーの区切りを設定します。

1. **倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。
1. 編集する **作業指示書のタイプ** (*発注書* など) を選択します。
1. 編集するには、作業テンプレートを選択します。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. **並べ替え** タブを開き、次の設定で行を追加します。
    - **テーブル** - *一時的な作業トランザクション*
    - **派生テーブル** - *一時的な作業トランザクション*
    - **フィールド** - *出荷 ID*
1. **OK** を選択します。
1. **作業テンプレート** ページに戻ります。 アクション ウィンドウで、**作業ヘッダーの分割** を選択します。
1. アクション ウィンドウで、**編集** を選択します。
1. **フィールド名***出荷 ID* に関連付けられているチェックボックスをオンにします。
1. アクション ウィンドウで、**保存** を選択します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

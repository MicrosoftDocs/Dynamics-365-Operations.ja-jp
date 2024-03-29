---
title: 警告の概要 (ビデオを含む)
description: この記事では、 の警告に関する一般情報を提供します。 警告を使用することで、作業日に追跡したいイベントに関する情報を常に受け取ることができます。
author: RichdiMSFT
ms.date: 09/04/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: b81eb8e0be4c7d7357a6b8b7b5f0ac025b9ab8ca
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124261"
---
# <a name="alerts-overview"></a>警告の概要

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>警告について
システムの重大なイベントの通知システムは、警告によって形成されます。 警告を使用することで、作業日に追跡したいイベントに関する情報を常に受け取ることができます。 延滞した出荷、削除された注文、変更された価格、またはその他対応が必要なイベントに関する警告を受け取る独自の警告ルール セットを、簡単に作成できます。

エンタープライズ リソース プランニング (ERP) では、警告機能を使用できる、いくつかの一般的なシナリオがあります。 次にいくつか例を挙げます。

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>シナリオ 1: 新しい販売注文に対する警告ルールの作成

1. **すべての販売注文** ページを開きます。
2. **オプション** タブのアクション ウィンドウの、**共有** グループで、**カスタム警告の作成** を選択します。
3. **警告ルールの作成** ダイアログ ボックスの **警告する時期** クイック タブの **イベント** フィールドで、**レコードが作成されました** を選択します。

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>シナリオ 2: 出荷日の延期に対する警告ルールの作成

1. **すべての発注書** ページを開きます。
2. 発注書の詳細にアクセスするには、購買注文の ID を選択します。
3. **発注書ヘッダー** クイック タブを展開します。
4. **オプション** タブのアクション ウィンドウの、**共有** グループで、**カスタム警告の作成** を選択します。
5. **警告ルールの作成** ダイアログ ボックスの **警告する時期** クイック タブの **フィールド** フィールドで、**出荷日** を選択します。
6. **イベント** フィールドで、**は延期されました** を選択します。
    
**警告ルールの作成** ダイアログ ボックスを閉じた後、**警告ルールの管理** ページにルールが表示されます。 **警告ルールの管理** ページを使用して、既存の警告ルールを更新することができます。 たとえば、イベント トリガーを変更し、イベント通知を更新し、有効期限を更新することができます。 **警告ルールの管理** ページを開くために、アクション ペインの **オプション** タブにある **警告** ボタンを使用します。

## <a name="what-occurs-when-an-alert-rule-is-created"></a>警告ルール作成時の処理

警告ルールを作成すると、事前に定義したイベントを特定のフィールドに関連付けることができます。 たとえば、フィールドに指定された日付が来るか、またはフィールドの内容が変更されます。 また、イベントを特定のページのレコードに関連付けることもできます。 たとえば、レコードが作成されるか、レコードが削除されます。

選択したイベントがフィールドまたはページ上のレコードに対して発生すると、警告が自分自身に送信されます。 たとえば、特定の発注書明細行の **配送日** フィールドを、**この合計時間数より前が期限でした** イベントに関連付けるルールを作成します。 期間は 5 日に設定します。 この場合は、発注書明細行の配送日の 5 日後に警告が送信されます。

また、条件を設定して警告ルールを調整することもできます。 たとえば、特定の仕入先勘定に対して作成された新しい発注書に関する警告を受け取ることができます。

## <a name="preparing-for-an-alert"></a>警告を準備する

警告ルールを設定するには、その前に、いつどのような状況の場合に警告を受信するかを決定します。 通知が必要なイベントがわかっているときは、そのイベントを表示するデータのページを見つけます。 イベントは、到来した日付か、または発生した特定の変更のいずれかです。 したがって、日付が指定されたページ、あるいは、変更されるフィールドまたは新しく作成されたレコードを表示するページを見つける必要があります。 この情報が用意されたら、警告ルールを作成できます。

## <a name="components-of-an-alert-rule"></a>警告ルールのコンポーネント

警告ルールには、5 つのコンポーネントがあります。

- **イベント** – 警告ルールを発生するイベントは、到来した日付かまたは発生した特定の変更のいずれかです。 **警告ルールの作成** ダイアログ ボックスの **ジョブ状態変更の電子メール警告の送信** クイック タブでイベントを定義することができます。
- **条件** – **警告ルールの作成** ダイアログ ボックスの **表示する警告** クイック タブで、イベントについての警告をいつ受けるかを制御する条件の範囲を選択できます。 このルールは、現在のレコードのみに適用することも、ページ上に表示されるすべてのレコードに適用することもできます。 法人間でルールが適用される場合は、**組織全体** オプションを **はい** に設定します。
- **ルールの有効期限** – **警告ルールの作成** ダイアログ ボックスの **表示する警告** クイック タブで、警告ルールを有効にする期間を指定することができます。
- **コンテンツ** – **警告ルールの作成** ダイアログ ボックスの **表示する警告** クイック タブで、警告メッセージで使用する件名テキストとメッセージ テキストを指定できます。
- **ユーザー** – **警告ルールの作成** ダイアログ ボックスの **警告先** クイック タブで、ユーザーが警告メッセージを受け取る必要があるかを指定することができます。 既定では、自身のユーザー ID が選択されます。

    > [!NOTE]
    > このオプションは、組織の管理者に制限されています。

## <a name="videos"></a>ビデオ

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a>警告を使用してフィルタ処理されたデータを監視する方法

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

[警告を使用してフィルタ処理されたデータを監視する方法](https://youtu.be/ZYKMcv6kl9s) ビデオ (上記) を含む、[財務と運用プレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) は YouTube でご覧いただけます。

### <a name="alert-rule-options"></a>警告ルールオプション

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

[警告ルールオプション](https://youtu.be/cpzimwOjicM) ビデオ (上記) を含む、[財務と運用プレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) は、YouTube でご覧いただけます。




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

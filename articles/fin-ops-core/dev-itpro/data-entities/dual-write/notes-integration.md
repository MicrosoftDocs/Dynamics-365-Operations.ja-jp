---
title: メモ統合
description: この記事では、二重書き込みでのメモ データの統合について説明します。
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 19a1fd53f19575a16ee8d8b7391c30f0cacf26a8
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111459"
---
# <a name="note-integration"></a>メモ統合

[!include [banner](../../includes/banner.md)]



多くの場合、業務プロセス中に Microsoft Dynamics 365 ユーザーは顧客に関する情報を収集します。 この情報は、活動およびメモとして記録されます。 この記事では、二重書き込みでのメモ データの統合について説明します。

顧客情報は、次のように分類できます。

+ **顧客の代わりに Dynamics 365 ユーザーが処理する実用的な情報** - 例えば Contoso (Dynamics 365ユーザー) が Game Show を実行している場合など。 Contoso の顧客の 1 人 (顧客) が、Game Show に参加したいと思っています。 顧客は、Contoso の従業員に対し、Game Show でのスロットの予約を求める場合があります。 予約は Contoso のイベント出席者のカレンダーで発生します。
+ **Dynamics 365 ユーザーの実用的な情報** - たとえば、Surface ユニットを購入する顧客は、出荷前にデバイスを贈り物用に包装する必要があるという特別な指示を入力します。 これらの指示は、梱包を担当する Contoso の従業員が処理する必要がある、実用的な情報です。
+ **非実用的な情報** - 例えば、顧客は Contoso ストアにアクセスし、店舗スタッフとの会話の中で、*Halo* のゲームとゲーム用アクセサリに関心を示します。 店舗スタッフはこの情報をメモします。 その後、製品の推奨エンジンを使用して、顧客に対して推奨事項を作成します。

一般に、実用的な情報は、財務と運用アプリおよび Customer Engagement アプリに *活動* として記録されます。 非実用的な情報は、財務と運用アプリに *メモ*、Customer Engagement アプリに *注釈* として記録されます。

> [!TIP]
> メモは非実用的な情報を対象としていますが、メモを使用して実用的な情報を保管および処理する場合、アプリがその使用を妨げることはありません。

Microsoft は現在、メモ統合のための機能をリリースしています。 (活動統合の機能は、後でリリースされます)。メモの統合は、顧客、仕入先、販売注文、および発注書に対して使用できます。

## <a name="create-a-note-in-a-customer-engagement-app"></a>Customer Engagement アプリでのメモの作成

Customer Engagement アプリでメモを作成し、それを財務と運用アプリに同期させるには、次の手順に従います。

1. Customer Engagement アプリで、顧客の勘定レコードを開きます。
2. **タイムライン** ウィンドウでプラス記号 (**+**) を選択してから、**メモ** を選択してメモを作成します。

    ![Customer Engagement アプリでのメモの作成。](media/notes-ce-1.png)

3. タイトルおよび説明を入力し、**メモの追加** を選択します。

    ![タイトルと説明を入力する。](media/notes-ce-2.png)

    新しいメモが顧客のタイムラインに追加されます。

    ![顧客のタイムライン上の新しいメモ。](media/notes-ce-3.png)

4. 財務と運用アプリにサインインし、同じ顧客レコードを開きます。 右上隅の **添付ファイル** ボタン (クリップの記号) はレコードに添付ファイルがあることを示します。

    ![添付ファイルに関する通知。](media/notes-ce-4.png)

5. **添付ファイル** ボタンを選択して **添付ファイル** ページを開きます。 Customer Engagement アプリで作成したメモを見つける必要があります。

    ![Customer Engagement アプリからのメモ。](media/notes-ce-5.png)

メモに対する更新は、財務と運用アプリと Customer Engagement アプリ間で相互に同期されます。

## <a name="create-a-note-in-a-finance-and-operations-app"></a>財務と運用アプリでメモを作成する

財務と運用アプリでメモを作成し、Customer Engagement アプリに同期させることもできます。

財務と運用アプリでメモを作成し、それを Customer Engagement アプリに同期させるには、次の手順に従います。

1. 財務と運用アプリの **添付ファイル** ページで、**新規** \> **メモ** を選択します。

    ![財務と運用アプリでメモを作成する。](media/notes-fo-1.png)

2. タイトルと簡単な手順のセットを入力し、**保存** を選択します。

    ![タイトルと手順を入力する。](media/notes-fo-2.png)

3. Customer Engagement アプリで、レコードを更新します。 新しいメモをタイムラインで見つける必要があります。

    ![Customer Engagement アプリのタイムライン上の新しいメモ。](media/notes-fo-3.png)

メモは、内部または外部のどちらかとして分類できます。

- 財務と運用アプリの、**添付ファイル** ページ、次いで **制限** フィールドで **内部** または **外部** を選択します。

    ![制限フィールド。](media/notes-fo-4.png)

URL を作成することもできます。

1. 財務と運用アプリの **添付ファイル** ページで、**新規** \> **URL** を選択します。
2. タイトルと URL を入力します。
3. **制限** フィールドで、**内部** または **外部** を選択します。

    ![財務と運用アプリで URL を作成する。](media/notes-fo-5.png)

4. **保存** を選択します。

    Customer Engagement アプリには URL タイプはないので、URL はメモとして二重書き込み機能と統合されています。

    ![Customer Engagement アプリでのメモとして表示される URL の作成。](media/notes-ce-6.png)

> [!NOTE]
> 添付ファイルはサポートされていません。

## <a name="templates"></a>テンプレート

メモ統合には、次の表に示すように、データ操作中に連携して動作するテーブル マップのコレクションが含まれています。

| 財務と運用アプリ | Customer Engagement アプリ | Description |
|----------------------------|-------------------------|-------------|
| [顧客の添付ファイル](mapping-reference.md#230) | 注釈 | テキスト形式と URL を使用して顧客固有の (組織と人の両方の) 情報を取り込む企業。 |
| [仕入先ドキュメントの添付ファイル](mapping-reference.md#231) | 注釈 | テキスト形式と URL を使用して仕入れ先固有の (組織と人の両方の) 情報を取り込む企業。 |
| [販売注文のヘッダー ドキュメント添付](mapping-reference.md#229) | 注釈 | テキスト形式と URL を使用して販売注文固有の情報を取り込む企業。 |
| [発注書のヘッダー ドキュメントの添付ファイル](mapping-reference.md#232) | 注釈 | テキスト形式と URL を使用して発注書固有の情報を取り込む企業。 |

## <a name="limitations"></a>制限

ノート ソリューションをインストールすると、アンインストールすることはできなくなります。 

詳細については、[二重書き込みマッピングのリファレンス](mapping-reference.md) を参照してください。


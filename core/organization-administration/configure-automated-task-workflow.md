---
title: "ワークフローの自動化タスクのコンフィギュレーション"
description: "このトピックでは、自動化タスクのプロパティをコンフィギュレーションする方法について説明します。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 66f1b8e03cc0da5d21fea9b3c795d8f4097c8cfc
ms.contentlocale: ja-jp
ms.lasthandoff: 06/13/2017

---

# <a name="configure-an-automated-task-in-a-workflow"></a>ワークフローの自動化タスクのコンフィギュレーション

[!include[banner](../includes/banner.md)]


このトピックでは、自動化タスクのプロパティをコンフィギュレーションする方法について説明します。

ワークフロー エディターで自動化タスクをコンフィギュレーションするには、タスクを右クリックし、[**プロパティ**] をクリックして、[**プロパティ**] ページを開きます。 それから次の手順に従って、自動化タスクのプロパティをコンフィギュレーションします。

## <a name="name-the-task"></a>タスクに名前を付ける
自動化タスクの名前を入力するには、次の手順に従います。

1.  左ウィンドウで [**基本設定**] をクリックします。
2.  [**名前**] フィールドに、タスクの固有名を入力します。

## <a name="specify-when-notifications-are-sent"></a>いつ通知を送信するかを指定する
自動化タスクが実行されたときまたはキャンセルされたときに、ユーザーに通知を送信できます。 通知の送信条件と送信先のユーザーを指定するには、次の手順に従います。

1.  左ウィンドウで、[**通知**] をクリックします。
2.  通知の送信するイベントの横にあるチェック ボックスをオンにします。
    -   [**実行**] – タスクが実行されたときに通知が送信されます。
    -   [**キャンセル済**] – タスクがキャンセルされたときに通知が送信されます。

3.  ステップ 2 で選択したイベントの行を選択します。
4.  [**通知テキスト**] タブのテキスト ボックス内で、通知のテキストを入力します。
5.  通知を個人向けのものにするには、プレースホルダーを挿入します。 プレースホルダーは、通知がユーザーに表示されるときに、適切なデータに置き換えられます。 次の手順に従って、プレースホルダーを挿入します。
    1.  テキスト ボックス内で、プレースホルダを表示する場所をクリックします。
    2.  [**プレースホルダーの挿入**] をクリックします。
    3.  表示されるリストで、挿入するプレースホルダーを選択します。
    4.  [**挿入**] をクリックします。

6.  通知の翻訳を追加するには、次の手順に従います。
    1.  [**翻訳**] をクリックします。
    2.  表示されるページで、[**追加**] をクリックします。
    3.  表示される一覧で、テキストを入力する言語を選択します。
    4.  [**翻訳テキスト**] フィールドで、テキストを入力します。
    5.  テキストをカスタマイズする場合は、ステップ 5 の説明に従い、プレースホルダーを挿入します。
    6.  [**閉じる**] をクリックします。

7.  [**受信者**] タブで、通知の送信先ユーザーを指定します。 次の表のいずれかのオプションを選択し、オプションの追加ステップを実行してから、ステップ 8 に進みます。
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>オプション</th>
    <th>通知の受信者</th>
    <th>追加手順</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>参加者</td>
    <td>特定のグループまたはロールに割り当てられたユーザー</td>
    <td><ol>
    <li>[<strong>参加者のタイプ</strong>] 一覧の [<strong>ロール ベース</strong>] タブの、[<strong>参加者</strong>] を選択したのち、通知の送信先のグループまたはロールのタイプを選択します。</li>
    <li>[<strong>参加者</strong>] の一覧で、通知の送信先のグループまたはロールのタイプを選択します。</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>ワークフロー ユーザー</td>
    <td>現在のワークフローに参加しているユーザー</td>
    <td><ul>
    <li>[<strong>ワークフロー ユーザー</strong>] 一覧の、[<strong>ワークフロー ユーザー</strong>] タブの、[<strong>ワークフロー ユーザー</strong>] を選択したのち、ワークフローに参加するユーザーを選択します。</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>ユーザー</td>
    <td>特定の Microsoft Dynamics 365 for Finance and Operations ユーザー</td>
    <td><ol>
    <li>[<strong>ユーザー</strong>] を選択したのち、[<strong>ユーザー</strong>] タブをクリックします。</li>
    <li>[<strong>利用可能なユーザー</strong>] 一覧には、すべての Finance and Operations ユーザーが含まれます。 通知の送信先のユーザーを選択して、それらのユーザーを [<strong>選択されたユーザー</strong>] リストに移動します。</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  ステップ 2 で選択したイベントごとに、ステップ 3～7 を繰り返します。






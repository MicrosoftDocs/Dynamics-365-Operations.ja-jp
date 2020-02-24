---
title: Attract および Onboard からのデータのエクスポート
description: Dynamics 365 Talent - Attract および Onboard からデータをエクスポートします。
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: acdd93637385246f9c5c652cccdf2cbfb263cc33
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2020
ms.locfileid: "2975937"
---
# <a name="export-data-from-attract-and-onboard"></a>Attract および Onboard からのデータのエクスポート

[!include [banner](includes/banner.md)]

[Dynamics 365 Talent: Attract および Dynamics 365 Talent: Onboard アプリの廃止](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps) で発表された通り、Dynamics 365 Talent: Attract および Dynamics 365 Talent: Onboard は、2022 年 2 月 1 日に廃止されます。 別の製品への移行を支援するために、両方のアプリでデータエクスポート機能を使用できるようになりました。

## <a name="export-data-from-attract"></a>Attract からのデータのエクスポート

環境へのアクセスを制限することなく、データをエクスポートすることができます。 テスト目的で、またはデータ構造を理解するために、この操作を実行することができます。 移行する準備ができたら、この手順の後の指示に従って、Attract 環境に対するアクセスを制限します。 必ずデータを再度エクスポートしてください。 

1. [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport) に移動します。

2. **データのエクスポート**で、**データのエクスポートを要求**を選択します。

   ![[Attract からのデータ エクスポートの要求](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. **要求は処理中**メッセージボックスが表示されたら、**OK** を選択します。 エクスポートのサイズによっては、データのエクスポートに最大で 20 分かかる場合があります。

4. エクスポートが完了したら、横にある**ダウンロード** ボタンを選択します。 

   >[!NOTE]
   >すべてのデータ エクスポートは 7 日間実行でき、この時点で**ダウンロード** リンクの有効期限が切れます。</br>
   
ダウンロードには、Attract データを含む .zip ファイルが含まれており、以下のフォルダーが含まれます。

| フォルダー名 | 説明 |
| --- | --- |
| 管理者設定 | Attract 管理センターのコンフィギュレーション。 |
| 候補者 | 職務または人材プールに追加された全候補者。 |
| 電子メール テンプレート | 環境に対してコンフィギュレーションされたすべての電子メール テンプレート。 |
| ジョブ オファー パッケージ テンプレート | 作成されたすべてのジョブ オファー パッケージ テンプレートと、それに関連付けられているコンフィギュレーション。 |
| ジョブ オファー ルール セット |  オファー管理のためにアップロードされたすべてのルール セット ファイル。 |
| ジョブ オファー テンプレート | 環境に対して作成されたすべてのジョブ オファー ドキュメント テンプレート。 |
| 求人 | 作成されたすべてのジョブ。 削除されたジョブはエクスポートされません。 サブフォルダーには、候補者のアプリケーションが含まれており、候補者のアプリケーション添付ファイルのサブフォルダーと、該当する場合はオファー パッケージが含まれます。 |
| 求人テンプレート | 環境に対してコンフィギュレーションされたジョブ プロセス テンプレート。 |
| 人材プール | 作成された人材プール、貢献者リスト、および人材プールの候補者リスト。 |
| 作業者 | 環境に存在するすべての作業者のリスト、およびそのロール。 |
| (ルート フォルダー) | データ構造フィールドを説明する JSON スキーマ ファイル。 |

### <a name="restrict-access-to-attract"></a>Attract へのアクセスの制限

移行する準備ができたら、非管理者の Attract 環境へのアクセスを制限し、データをエクスポートします。

>[!IMPORTANT]
>Attract 環境へのアクセスの制限は永続的で、元に戻すことはできません。 管理者以外のユーザーが継続して環境にアクセスできるようにする場合は、この手順を省略します。

1. [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport) に移動します。

2. 非管理者による Attract 環境へのアクセスを制限するには、**このアプリへのアクセスの制限**で、**今すぐアクセスを制限**を選択します。 アクセスを制限すると、転記済の有効なジョブもすべて無転記になります。

   ![[非管理者の Attract へのアクセスの制限](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. **これは永続的な変更です**という警告が表示された場合は、**アクセスの制限**を選択して、この環境に対して管理者以外のユーザーを完全に制限します。 この手順を完了する準備ができていない場合は、**キャンセル**を選択します。

   ![[アクセス制限が永続的な変更であるという警告](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >管理者は、Attract 環境へのアクセスを制限した後に、データ エクスポート ページと個人レポート ページに継続してアクセスできます。

## <a name="export-data-from-onboard"></a>Onboard からデータをエクスポート

準備が整ったら、テンプレート、ガイド、および候補者データを Onboard からダウンロードすることができます。

1. [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport) に移動します。

2. **データのエクスポート**で、**データのエクスポートを要求**を選択します。 

   ![[Onboard からのデータ エクスポートの要求](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. **要求は処理中**メッセージボックスが表示されたら、**OK** を選択します。 エクスポートのサイズによっては、データのエクスポートに最大で 20 分かかる場合があります。

4. エクスポートが完了したら、横にある**ダウンロード** ボタンを選択します。 

   ![[Onboard からのデータ エクスポートのダウンロード](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >データ エクスポートは 7 日間使用できます。 7 日後に**ダウンロード** リンクの有効期限が切れ、データを再度ダウンロードする必要がある場合は、新しいエクスポートを要求する必要があります。 新しいデータ エクスポートを開始すると、新しいエクスポートが成功した後に既存のダウンロードが期限切れになります。

ダウンロードは、次の内容を含む .zip ファイルです。

- Word 文書形式の Onboard テンプレートを含む**テンプレート** フォルダー。

- Word 文書形式の Onboard ガイドを含む**ガイド** フォルダー。

## <a name="see-also"></a>参照

[Dynamics 365 Talent: Attract および Dynamics 365 Talent: Onboard アプリの廃止](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
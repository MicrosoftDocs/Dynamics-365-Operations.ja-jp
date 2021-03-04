---
title: 新しい環境の配置
description: このトピックでは、セルフ サービス配置エクスペリエンスを使用して新しい環境を配置する方法について説明します。
author: rashmansur
manager: AnnBe
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 24211
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 70f57dac9ca13486fc307c8ded3ac001f6dc31f1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680541"
---
# <a name="deploy-a-new-environment"></a>新しい環境の配置

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

このトピックでは、[セルフサービス配置](infrastructure-stack.md)エクスペリエンスを使用してサンドボックス (レベル 2 以上) および運用環境のプロセスの手順を詳しく説明します。 このような環境を配置する次の手順を参照してください。

1. プロジェクト ダッシュボード ページで **構成** を選択します。
2. 配置する環境の **アプリケーション** および **プラットフォーム** バージョンを選択します。 
3. 環境の **一意の名前** を指定してください。
4. この環境を配置する **地域** を選択します。 
5. 環境で **デモ データ** を読み込むかどうかや、**空のデータベース** が必要かどうかを選択します。
6. 製品で「はじめに」ライブラリとして設定される **BPM ライブラリ** を選択します。
7. カスタマイズを適用する場合は、アセット ライブラリでソフトウェア配置可能タブで、使用可能な **AOT パッケージ** (カスタマイズ パッケージ) のリストから選択します。 バージョン 8.1 以上のビルド環境から生成されたパッケージのみ選択してください。 互換性のないバージョンからパッケージを適用すると、環境に悪影響を与えるがあります。
8. この環境に関連する **通知** を受け取る **2 つのユーザー電子メール アドレス** を指定します。 これらのユーザーは、既にプロジェクト チームに所属しているユーザー (ISV またはパートナーなど) に追加されます。
9. 製品で **システム管理者** として設定される **ユーザー** の **電子メール アドレス** を選択します。
10. 構成を検証した後、**送信** をクリックして配置をトリガーします。
11. チャネルの使用を計画する場合は、[Retail Cloud Scale Unit の初期化](initialize-retail-channels.md) も必要です。

環境配置はすぐに開始され、完了までに **1 ～ 2 時間** かかることがあります。 

配置の進行状況を常時監視するには、**環境の詳細** ページを表示できます。 環境の状態は、**配置中** または **配置済み/失敗** のいずれかに変更されます。

配置が **成功した** 場合、環境の状態は **配置済み** になり、環境の管理者として設定されたユーザーは環境にログインできるようになります。

配置が **失敗した** 場合、Microsoft [サポート チケット](../lifecycle-services/lcs-support.md)を作成し、サポート チケットで **最後のアクティビティ ID** (**環境詳細** ページの **環境の管理** で確認できます) を指定します。

## <a name="delete-an-environment"></a>環境の削除

環境の詳細ページを使用して配置された状態にある環境を直接削除することができます。 環境を削除するには、環境の詳細ページに移動し、アクション バーで **削除** ボタンをクリックします。 削除する環境の名前を入力するように要求する確認ダイアログ ボックスが表示されます。 環境の名前を入力し、**はい** を選択すると、削除操作が開始されます。 削除処理が完了すると、環境を再配置する場合は、この環境の **構成** ボタンがプロジェクト ダッシュボードで有効になります。 

> [!NOTE]
> 環境を再配置するには、環境を削除し、上記の手順を使用してもう一度を配置する必要があります。 

> [!IMPORTANT]
> クラウドでチャネル機能を使用している既存の顧客の場合、業務の継続的かつ中断のないサポートを確保するには、2020 年 1 月 31 日までに [Retail Cloud Scale Unit の初期化](initialize-retail-channels.md) を行う必要があります。 Store Scale Unit を独占して使用している顧客に対しては、アクションは必要ありません。 延長が必要な場合は、Microsoft FastTrack Solution Architect までご連絡ください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: クライアント インターネット接続
description: このトピックは、オンプレミス配置で、クライアント マシンがインターネットにアクセスできない場合に何が起きるかについて説明します。
author: jasongre
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29151
ms.assetid: ''
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.openlocfilehash: 419a87506b2a0b68bc2480432f26bef5b88fdd43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752668"
---
# <a name="client-internet-connectivity"></a>クライアントのインターネット接続

[!include [banner](../includes/banner.md)]


Dynamics 365 Finance + Operations (オンプレミス) 展開用のローカル ネットワークの構成は、Web クライアントで利用可能な機能に影響を与える可能性があります。 特に、ネットワーク構成がインターネットにアクセスするクライアント マシンを許可していない場合、Web クライアントで複数のパフォーマンス低下が発生します。 コピーされるフィールドは次のとおりです。    

+ ナビゲーション バーにおける Office アプリ ランチャおよび Dynamics 365 領域はクリック可能でなくなりました。
+ ヘルプ ウィンドウにはアクセスできません。  
+ Ideas ポータルは、Web クライアントからアクセスすることはできません。 
+ ユーザー イメージではなく、ユーザーのイニシャルが表示されます。 
+ Skype 統合が使用できなくなります。  
+ ブラウザー タブに表示されるお気に入りのアイコンは、アプリケーションのアイコンではなく、ブラウザーの既定のお気に入りのアイコンになります。 
+ Excel アドインが実行されないため、Excel で開くオプションは表示されません。

クライアントがインターネットにアクセスできない場合にアクセスできない可能性があるプラットフォーム機能に加えて、開発者が非表示にするかオフにする必要がある、インターネット接続に依存したアプリケーション機能もある可能性があります。 これを容易にするために、開発者は **セッション** クラスに追加された **clientHasRestrictedInternet()** メソッドを使用できます。 このメソッドは、クライアントがインターネットにアクセスできない場合は true を返します。

## <a name="client-internet-connectivity-options"></a>クライアント インターネット接続オプション

クライアント インターネット接続オプションにより、管理者は、インターネット接続が利用可能であってもクライアントが行う外部接続を手動でオフにすることができます。 これらは、問題のトラブルシューティングや、インターネット接続が利用できない場合にクライアントがどのように見えるか確認するために使用できます。 これらのクライアント インターネット接続オプションは、プラットフォーム アップデート 16 からすぐに利用できますが、プラットフォーム アップデート 15 ([KB 4091764](https://fix.lcs.dynamics.com/Issue/Details?kb=4091764&bugId=3934774&qc=245bb2cc9839fa2a2ecf6bfffc48c3dec102a3c1047e5e755387d00148db18cb) 経由) およびプラットフォーム アップデート 12 ([KB 4091763](https://fix.lcs.dynamics.com/Issue/Details?kb=4091763&bugId=3934773&qc=19e9634da3297903a2ac51cf291a4770fd4532c9767ca7b5cefbe1bccb5d4d9f) 経由) でも利用できます。 


クライアント インターネット接続オプションは、**システム管理** > **設定** > **クライアント パフォーマンス オプション** ページにあります。 

- **インターネット接続が有効** - 管理者は、Web クライアントが外部から行う外部接続をすべてオフにすることができます。
- **Skype プレゼンスが有効** - 管理者がスカイプへの外部接続をオフにし、そうでなければWeb クライアントが行います。

## <a name="why-does-the-client-connect-to-the-skype-for-business-api-when-it-first-loads"></a>クライアントが最初に読み込まれたときに Skype for Business API に接続する理由。

クライアントの読み込み時に、インターネット接続が使用可能かどうかを確認するために、Skype for Business API へのクイック コール (ping) が実行されます。 使用できない場合は、クライアントは切断された方法で機能します。 環境では、このチェックを実行するために Skype for Business を表示するかどうかを指定する必要はありません。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
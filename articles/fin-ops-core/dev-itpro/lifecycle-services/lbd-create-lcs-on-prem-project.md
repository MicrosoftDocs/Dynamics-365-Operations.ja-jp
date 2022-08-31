---
title: Lifecycle Services (LCS) でのオンプレミス プロジェクトの設定
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) でオンプレミス プロジェクトを設定するプロセスについて説明します。
author: PeterRFriis
ms.date: 08/09/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ce4ce6bcbf2afdf5a297a5f5713fff264a8aa2c
ms.sourcegitcommit: e14648b01549bdc17998ffdef6cde273d4e78560
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/09/2022
ms.locfileid: "9242901"
---
# <a name="set-up-on-premises-projects-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) でのオンプレミス プロジェクトの設定

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) を使用して、Dynamics 365 Finance + Operations (on-premises) のインスタンスを配置し更新する必要があります。 ボリューム ライセンス フローまたは Dynamics 価格リスト フローを通じてサーバーとユーザーのライセンスを購入した後は、 [Finance + Operations (on-premises) の購入](../../fin-ops/get-started/purchase-on-premises.md)を参照して、 Azure AD アカウントを作成、または既存の Azure AD アカウントを使用して、すべてのサインアップ手順を完了します。 ユーザーは LCS へリダイレクトされ、そこでオンプレミス実装プロジェクトがプロビジョニングされます。

 [![オンプレミス実装プロジェクト。](./media/lbd-proejcts-01.png)](./media/lbd-proejcts-01.png)

オンプレミス プロジェクトには、オンプレミス ソリューションの実装、保守、および運用に必要なすべてのツールがあります。 オンプレミス プロジェクトで使用可能なツールの一部を次に示します。

- **方法** – オンプレミスの方法は、顧客がオンプレミス プロジェクトを実装および管理するのに役立つベスト プラクティスを提供しています。
- **ビジネス プロセス モデラー** - ビジネス プロセス モデラー (BPM) は、要件をキャプチャし、ギャップ分析に適合するために使用されます。
- **クラウド ホスト環境** - クラウドホスト環境は、開発者の配置とトポロジの構築、およびオンプレミス ソリューションのための Dev Application Lifecycle Management(ALM) の完成に使用されます。
- **コードのアップグレード** - これらのツールを使用して、コードを新しいバージョンにアップグレードできます。
- **問題検索** – アプリケーションとプラットフォームの問題に関連する公開済の KB を検索します。
- **ローカライズおよび翻訳** – 資産のローカライズおよび翻訳。
- **サポート** – ファイルおよびトラック がインシデントをサポートします。
- **プロジェクト ユーザー** – プロジェクトにユーザーを割り当てます。
- **プロジェクト設定** – コネクタ、プロジェクト名、組織ユーザー、ライセンス番号などのプロジェクトレベルの設定を編集します。
- **アセット ライブラリ** - アセット ライブラリは、パッケージなどのさまざまなアセットのライブラリです。
- **SharePoint のオンライン ライブラリ** – オンラインの Microsoft SharePoint ライブラリに接続します。

オンプレミス実装を開始するには、プロジェクトを正しくセットアップし、開発者とビルド環境を展開してから、サンドボックス環境と運用環境を展開する方法の手順に従う必要があります。 展開に役立つように、2 つの環境スロットがオンプレミス プロジェクトにあらかじめ割り当てられています。 一方のスロットはサンドボックス環境用で、もう一方のスロットは運用環境用です。 これらのスロットは、サービス フロー中に使用され、パッケージが運用環境で適用される前にサンドボックス環境でテストされることを保証します。

## <a name="environment-limits"></a>環境制限
顧客およびパートナーは、特定のオンサイト プロジェクトに配置できる特定の環境タイプの数に制限されます。  次のテーブルで説明します。

|組織タイプ|運用環境|サンドボックス環境|
|-----------------|-----------------------|--------------------|
| 顧客 | 1 | 1 回以上 |
| パートナー (インストール時のライセンスを含む) | 1 | 1 回以上 |
| パートナー (インストール時のライセンスを含まない) | 0 | 1 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

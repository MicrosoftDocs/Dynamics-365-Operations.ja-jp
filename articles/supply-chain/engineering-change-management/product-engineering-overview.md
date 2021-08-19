---
title: エンジニアリング変更管理の概要
description: このトピックでは、製品のバージョン管理の計画と管理を支援し、製品のライフサイクルとエンジニアリング変更を管理するエンジニアリング変更管理の概要を説明します。
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8f2d577d9e48ced9d4c516a66e4f53671417875cbfb51bd6bdc2cb0938d83c01
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714959"
---
# <a name="engineering-change-management-overview"></a>エンジニアリング変更管理の概要

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>機能の概要

今日のメーカーは、製品のライフサイクル、品質と信頼性の要件の高まり、および製品の安全性に重点をおいており、強力な製品データ管理、バージョン管理、およびエンジニアリング変更管理を必要としています。

エンジニアリング変更管理では、製品データ管理プロセスに構造と規範を提供し、ワークフローでサポートされている制御された方法で製品を定義、リリース、および改訂できるようにします。製品のライフサイクル全体にわたって、製品バージョンやエンジニアリング変更管理を通じて文書化、影響の評価、およびエンジニアリング変更の適用を行うことができます。

エンジニアリング変更管理は、製品のバージョン管理の計画と管理を支援し、製品のライフサイクルとエンジニアリング変更を管理するエンジニアリング変更管理に役立ちます。 主な機能を次に示します:

- 製品のバージョン管理
- 強化された製品リリース機能により、1 つの法人 (技術会社) で製品マスター データを管理し、すべてのリリース済製品を他の法人に公開することができます
- 製品バージョンを有効化する前に必要な情報が入力されていることを検証するためのルール (準備完了チェック)
- リリースされた製品を特定の業務プロセスで使用できる時期をきめ細かく制御することにより、製品ライフサイクル管理を強化
- ワークフローでサポートされているエンジニアリング変更要求
- ワークフローでサポートされているエンジニアリング変更指示

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

前のビデオ ([Dynamics 365 Supply Chain Management の変更管理機能](https://youtu.be/N313FqvRuBc)) は、YouTube で利用可能な [Finance and Operations 再生リスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)に含まれています。

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>システムに対するエンジニアリング変更管理およびバージョン分析コード機能の有効

エンジニアリング変更管理を使用する前に、*エンジニアリング変更管理* 機能とそのコンフィギュレーション キーの両方を有効にする必要があります。 トランザクション内の製品のバージョン分析コードも追跡する場合 (オプション)、*製品バージョン分析コード* 機能とそのコンフィギュレーション キーも有効にする必要があります。

まず、次の手順に従って機能をオンにします。

1. [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)ワークスペースに移動します。
1. 更新プログラムを確認します。
1. *エンジニアリング変更管理* という機能を有効にします。
1. それを使用する場合は、*製品分析コード バージョン* という名前の機能も有効にします。

次に、次の手順に従ってコンフィギュレーション キーをオンにします。

1. [メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、システムをメンテナンス モードにします。
1. **システム管理 \> 設定 \> ライセンス コンフィギュレーション** の順にクリックします。
1. **取引** ノードを展開します。
1. **エンジニアリング変更管理** チェック ボックスを選択して、主要機能のコンフィギュレーション キーを有効にします。
1. **エンジニアリング変更管理** ノードを展開し、必要に応じて (使用する機能に応じて)、次のチェック ボックスをオンまたはオフにします。

    - **属性検索** – [属性検索機能](engineering-attributes-and-search.md) を有効にするには、このチェック ボックスを選択します。 この機能を有効にすることをお勧めしますが、使用しない場合は、このチェック ボックスはオフにできます。
    - **プロセス製造の変更管理** – エンジニアリング変更管理機能を使用してプロセス製造のフォーミュラの変更を管理する場合は、このチェック ボックスを選択します。 フォーミュラを管理する必要がない場合は、このチェック ボックスをクリアすることができます。 詳細については、[フォーミュラとその成分の変更の管理](manage-formula-changes.md) を参照してください。

1. バージョン分析コードも使用する場合は、**製品分析コード - バージョン** チェック ボックスを選択します。 (このチェック ボックスは一覧の下の方にあり、**エンジニアリング変更管理** ノードの下に入れ子になっていません。)
1. [メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、メンテナンス モードをオフにします。

> [!IMPORTANT]
> 2022 年 4 月から、**エンジニアリング変更管理** および **製品分析コード - バージョン** の両方のライセンス キーがすべての新規インストールで既定で有効になりますが、必要に応じて無効にすることもできます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: フォーミュラとその成分の変更の管理
description: この記事では、フォーミュラ管理を実行し、プロセス製造マスター データに対する変更を管理する方法について説明します。
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8105ebc7f3698a6baaa04b6548dac18a7bf81a47
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904075"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>フォーミュラとその成分の変更の管理

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management のプロセス製造機能を使用している場合は、関連するフォーミュラ管理機能を使用して、次の変更を管理することもできます。

- **フォーミュラ品目および計画品目:** フォーミュラの成分とそれらの連産品および副産物の変更を管理します。
- **連産品と副産物:** フォーミュラ内の連産品と副産物の数量およびその他の情報を編集します。
- **CW 品目:** CW 品目の変更を管理します。

## <a name="turn-this-feature-on-or-off"></a>この機能のオン/オフの切り替え

この記事で説明する機能を使用するには、システムで *技術変更管理* と *酢式とその成分への変更を管理する* の両方をオンにする必要があります。 これらの機能のオン/オフの切り替え方法の詳細については、[エンジニアリング変更管理の概要](product-engineering-overview.md) を参照してください。

## <a name="feature-naming-conventions"></a>機能の名前付け規則

Supply Chain Management のユーザー インターフェイス (UI) およびドキュメントでは、変更管理機能は通常、*エンジニアリング変更管理* と呼ばれ、管理可能な製品は *エンジニアリング製品* と呼ばれます。 この用語は通常、プロセス製造のフォーミュラ管理には関連していませんが、エンジニアリング変更管理は単に変更管理と考え、エンジニアリング製品はバージョン管理製品と考える必要があります。

## <a name="work-with-formula-change-management-features"></a>フォーミュラ変更管理機能の使用

次の一覧に、エンジニアリング変更管理機能をフォーミュラ管理に適用する方法を示します。 また、詳細情報へのリンクも提供します。 フォーミュラ変更管理では、エンジニアリング変更管理機能を利用しているため、エンジニアリング変更管理の一般的な機能を学習し、フォーミュラとその成分を管理できるようにしておく必要があります。

- **製品データの一元管理** – 管理されたリリース プロセスを通じて、企業全体のユーザーが正確で適切な製品データを利用できる組織を設定します。 詳細については、[エンジニアリング会社とデータ所有権のルール](engineering-org-data-ownership-rules.md) を参照してください。
- **製品のバージョン管理** – 製品バージョンを通じて製品の変更を追跡し、サプライ チェーンのすべてのステージで製品を制御します。 この方法で、フォーミュレーションの変更を追跡できます。 詳細については、[エンジニアリング バージョンとエンジニアリング製品カテゴリ](engineering-versions-product-category.md)を参照してください。
- **製品ライフサイクル管理** – 組織全体の製品データの可視性を管理し、サプライ チェーンの各ステージでの製品バージョンの可用性を管理します。 特定の業務プロセスで製品バージョンがいつ使用できるかを詳細に管理し、ビジネス ニーズに合わせて独自のライフサイクルの状態を作成することができます。 詳細については、[製品ライフサイクルの状態とトランザクション](product-lifecycle-state-transactions.md) を参照してください。
- **フォーミュラ変更管理** – 組織全体のユーザーがフォーミュラへの変更を依頼できます。 変更オーダーを使用して、提案された変更の影響を評価および文書化します。 ワークフローを追加し、変更プロセスおよび製品とそのフォーミュラの新しいバージョンのリリースを管理します。 詳細については、[エンジニアリング製品に対する変更の管理](engineering-change-management.md) を参照してください。
- **準備完了コントロール** – システム チェックおよびユーザー ガイダンス (アンケートおよびチェックリスト) を使用して、製品がリリースされる前に必要なすべての製品データが入力されていることを確認します。 詳細については、[製品準備](product-readiness.md) を参照してください。
- **強化された製品リリース機能** – 製品とそのフォーミュラの完全に定義されたバージョンを組織 (法人) から他の法人にリリースします。 リリース前に製品情報を確認または編集する必要があるかどうかを判断することもできます。 詳細については、[製品構造のリリース](release-product-structure.md) を参照してください。

前の一覧でリンクされている記事のほとんどは、部品表 (BOM) に基づいた例を示しています。 ただし、フォーミュラも同様に機能します。 以下に、変更管理 (またはフォーミュラ変更管理のみ) を使用してフォーミュラと BOM を管理する際に役立ついくつかの追加の概念を示します:

- 各 [製品エンジニアリング カテゴリ](engineering-versions-product-category.md) に対して、生産タイプ (BOM、フォーミュラ、または計画品目) を指定できます。 また、そのカテゴリを使用する製品に CW サポートが必要かどうかも指定できます。
- 連産品と副産物は、エンジニアリング製品ではありません。 そのため、バージョン管理されません。 変更する必要がある場合は、新しい製品を作成します。 この方法により、メンテナンスが容易になります。
- BOM であり、子フォーミュラ品目を持つ最終品目を管理できます。 この機能は、フォーミュラを含む BOM や BOM を含むフォーミュラのあらゆる組み合わせに対応します。

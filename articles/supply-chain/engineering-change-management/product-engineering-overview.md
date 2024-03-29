---
title: エンジニアリング変更管理の概要 (動画を含む)
description: この記事では、製品のバージョン管理の計画と管理を支援し、製品のライフサイクルとエンジニアリング変更を管理するエンジニアリング変更管理の概要を説明します。
author: t-benebo
ms.date: 08/09/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a01dfd72428c75d1bb24f32c73c9c799a6c5017e
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682509"
---
# <a name="engineering-change-management-overview"></a>エンジニアリング変更管理の概要

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>機能の概要

今日の製造元は、製品ライフサイクルの短縮化、品質と信頼性に対する要求の高まり、製品の安全性への関心の高まりといった世界で成功するために、強力な製品データ管理、バージョン管理、エンジニアリング変更管理を必要としています。

エンジニアリング変更管理では、製品データ管理プロセスに構造と規範を提供し、ワークフローでサポートされている制御された方法で製品を定義、リリース、改訂できるようになります。 製品バージョンとエンジニアリング変更管理により、製品のライフサイクル全体を通して、エンジニアリング変更を文書化し、その影響を評価し、適用することができます。

エンジニアリング変更管理は、製品のバージョン管理の計画と管理を支援し、製品のライフサイクルとエンジニアリング変更を管理するエンジニアリング変更管理に役立ちます。 主な機能を次に示します:

- 製品のバージョン管理
- 強化された製品リリース機能により、1 つの法人 (技術会社) で製品マスター データを管理し、すべてのリリース済製品を他の法人に公開することができます
- 製品バージョンを有効化する前に必要な情報が入力されていることを検証するためのルール (準備完了チェック)
- リリースされた製品を特定の業務プロセスで使用できる時期をきめ細かく制御することにより、製品ライフサイクル管理を強化
- ワークフローでサポートされているエンジニアリング変更要求
- ワークフローでサポートされているエンジニアリング変更指示

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4HE6B]

前のビデオ ([Dynamics 365 Supply Chain Management の管理機能の変更](https://youtu.be/N313FqvRuBc)) は、YouTube で利用可能な [財務と運用のプレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>システムのエンジニアリング変更管理機能を有効にする

エンジニアリング変更管理を使用する前に、*エンジニアリング変更管理* 機能とそのコンフィギュレーション キーの両方を有効にする必要があります。 トランザクション内の製品のバージョン分析コードも追跡する場合 (オプション)、*製品バージョン分析コード* 機能とそのコンフィギュレーション キーの両方を有効にする必要があります。 これらの前提条件が必要に応じて設定された後、エンジニアリング変更管理のための追加のオプション機能を有効にできます。

### <a name="turn-the-basic-engineering-change-management-features-on-or-off"></a>基本のエンジニアリング変更管理機能をオンまたはオフにする

基本のエンジニアリング変更管理機能をオンまたはオフにするには、次の手順に従います。 Supply Chain Management のバージョン 10.0.25 では、*エンジニアリング変更管理* 機能は既定で有効になっています。

1. [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)ワークスペースに移動します。
1. 更新プログラムを確認します。
1. *エンジニアリング変更管理* という名前の機能を必要に応じて、オンまたはオフににします。
1. トランザクション内の製品のバージョン分析コードも追跡する場合は (オプション)、*製品分析コードバージョン* という名前の機能をオンにします。

### <a name="turn-the-required-configuration-keys-on-or-off"></a>必要な構成キーをオンまたはオフにする

次に、次の手順に従ってコンフィギュレーション キーをオンにします。 これらは規定ではオンになっていません。

1. [メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、システムをメンテナンス モードにします。
1. **システム管理 \> 設定 \> ライセンス コンフィギュレーション** の順にクリックします。
1. **取引** ノードを展開します。
1. **エンジニアリング変更管理** チェック ボックスを使用して、主要機能の構成キーを有効または無効にします。
1. **エンジニアリング変更管理** ノードを展開し、必要に応じて (使用する機能に応じて)、次のチェック ボックスをオンまたはオフにします。

    - **属性検索** – [属性検索機能](engineering-attributes-and-search.md) を有効にするには、このチェック ボックスを選択します。 この機能を有効にすることをお勧めしますが、使用しない場合は、このチェック ボックスはオフにできます。
    - **プロセス製造の変更管理** – エンジニアリング変更管理機能を使用してプロセス製造のフォーミュラの変更を管理する場合は、このチェック ボックスを選択します。 フォーミュラを管理する必要がない場合は、このチェック ボックスをクリアすることができます。 詳細については、[フォーミュラとその成分の変更の管理](manage-formula-changes.md) を参照してください。

1. バージョン分析コードも使用する場合は、**製品分析コード - バージョン** チェック ボックスを選択します。 (このチェック ボックスは、一覧の一番下にあり、**エンジニアリング変更管理** ノードにはネストされていません。) この機能が必要ない場合は、このチェック ボックスをオフにできます。
1. [メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、メンテナンス モードをオフにします。
1. データベースは同期され、構成キーが変更を反映させるために正しく更新されている必要があります。 作業する環境のタイプに応じて、次のいずれかの手順を実行します。
    - **レベル 1 (開発) 環境の場合**: Microsoft Visual Studio でプロジェクトを開き、その後 **Dynamics 365 \> データベースの同期 \> 同期** を選択します。
    - **レベル 2 (およびそれ以上) 環境の場合**: 環境をメンテナンス モードに入れた後、データベースは自動的に同期し、この手順を省略できます。

> [!NOTE]
> エンジニアリング変更管理を使用するには、**番号順序** ページで BOM 番号順序とフォーミュラ番号順序 (フォーミュラを使用している場合) の両方を *自動* に設定する必要があります。

### <a name="turn-on-additional-engineering-change-management-features"></a>追加のエンジニアリング変更管理機能を有効にする

基本のエンジニアリング変更管理機能をオンにしてコンフィギュレーション キーを有効にした後、追加およびオプションのエンジニアリング変更管理機能が機能管理に追加されます。 これらの機能は、それぞれ **エンジニアリング変更管理** モジュールの下に一覧表示されます。 次の表では、オプションの各機能について説明し、詳細についてのリンクを提供します。

| 機能管理の機能名 | Description | 機能状態 |
|---|---|---|
| 既存の製品の変更管理の有効化 | <p>この機能を使用すると、既存の製品をエンジニアリング製品に変換し、エンジニアリング変更管理を使用して管理を開始できます。</p><p>詳細については、[既存の製品の変更管理を有効にする](change-management-existing-products.md)を参照してください。</p> | バージョン 10.0.25 から既定でオン。 |
| 生産向けのエンジニアリング通知 | <p>製品がエンジニアリングで変更された場合、その変更を生産に通知することが重要な場合があります。 このようにして、生産作業者は、コンポーネントの代替、部品表 (BOM) 交換、ルート交換などの適切なアクションを実行できます。 この機能を使用すると、生産されている製品の変更を生産に通知できます。</p><p>詳細については、[エンジニアリング製品に対する変更の管理](engineering-change-management.md) を参照してください。</p> |  バージョン 10.0.25 から既定でオン。 |
| エンジニアリング変更管理の属性継承の改善 | <p>この機能により、完成品または中間品目の属性管理が簡略化されます。 この機能を有効にすると、品目に属するすべての属性を識別しやすくなり、その品目から親品目に反映する属性を選択できるようになります。 この機能は、たとえば、完成品の 1 つのコンポーネントが割れ物、有害物質、または可燃性である場合に役立ちます。割れ物、有害物質、または可燃性の属性を簡単に識別し、完成品に反映できるためです。</p><p>詳細については、[エンジニアリング属性とエンジニアリング属性の検索](engineering-attributes-and-search.md)を参照してください。</p> |  バージョン 10.0.25 から既定でオン。 |
| 製品準備完了チェック | <p>この機能を使用すると、標準 (非エンジニアリング) 製品の準備完了チェックを設定できます。 製品準備完了チェックを使用して、製品が使用可能になりトランザクションで使用される前に、各製品が完全に定義され、必要なポリシーすべてが構成されていることを確認できます。 この機能をしばらく使用した後に無効にすると、標準製品の既存の準備完了チェックがすべて削除されます。</p><p>詳細については、[製品準備](product-readiness.md) を参照してください。</p> |  バージョン 10.0.25 から既定でオン。 |
| フォーミュラとその成分に対する変更の管理 | <p>この機能を使用すると、フォーミュラ構成要素、連産品、および副産物の変更を追跡できます。</p><p>詳細については、[フォーミュラとその成分の変更の管理](manage-formula-changes.md) を参照してください。</p> |  バージョン 10.0.25 から既定でオン。 |
| エンジニアリング製品のバリアントの生成 | <p>この機能により、使用可能な分析コード値に基づいて、エンジニアリング製品のバリアントを生成できます。</p><p>詳細については、[エンジニアリング製品のバリアントの生成](engineering-variants.md)を参照してください。</p> |  バージョン 10.0.25 から既定でオン。 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


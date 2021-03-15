---
title: 生産での作業者への Mixed-reality ガイドの提供
description: このトピックでは、Dynamics 365 Guides を使用した Microsoft Dynamics 365 Supply Chain Management での生産管理モジュールを統合する方法について説明します。
author: cabeln
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 3e69f9007b6605a07c6bec189b596d36a26f6222
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007217"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>生産での作業者への Mixed-reality ガイドの提供

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

生産プロセスの作業者は、作業の流れの中で適切な時に提供される関連する指示は大きな助けになります。 *手順* は、組み立て、サービス、行程、認定、および安全など、複数の作業ドメインで適用されます。 これらのコアビジネス機能には、継続的なトレーニング手順が用意されており、作業者が労働力を向上させることができます。

## <a name="introduction"></a>はじめに

手順は、さまざまな方法で提供できます。 すぐに利用できる効率的なシステムの 1 つは、[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) を使用します。

Dynamics 365 Guides は、実践的な学習によって従業員を支援することができます。 ステップ バイ ステップの標準化されたプロセスを定義して、必要なツールや部品を従業員に紹介し、そのツールを実際の作業状況で使用する方法を示すことができます。

次のように、生産管理のさまざまな側面にガイドを付けることができます。

- [リソース](#resources)
- [リソース グループ](#resource-groups)
- [リリースされた製品](#released-products)
- [フォーミュラ](#formulas)
- [フォーミュラ バージョン](#formula-versions)
- [部品表 (BOM)](#bom)
- [BOM バージョン](#bom-versions)
- [工順](#routes)
- [工順バージョン](#route-versions)
- [工順工程関連](#route-operation-relations)

> [!NOTE]
> また、資産管理でガイドを関連付けることもできます。 このオプションの詳細については、[Dynamics 365 Guides を使用した Dynamics 365 Supply Chain Management (資産管理) の統合](../asset-management/asset-management-guides-integration.md)を参照してください。

最前線で働く作業者が Supply Chain Management を通じて作業現場の職務を選択すると、作業者はジョブカードで[関連するガイド](#logic) を参照できます。 作業者が特定のガイドを選択すると、このガイドの QR コードが画面に表示されます。 作業者は、HoloLens を使用して QR コードをスキャンします。そうすると、ガイドが起動し必要な手順が表示されます。

次のサブセクションでは、ガイドを使用して製造に関する手順を表示する場合に、業界全体の企業が最大の価値を見出すことができるいくつかのシナリオについて説明します。

### <a name="assembly"></a>組み立て

![アセンブリ タスクのガイドの使用](media/instruction-guides-hero-assembly.png "サービス タスクのガイドの使用")

組み立て操作の手順では、作業者が必要なツールとパーツ、および実際の作業状況での使用方法が示されます。

生産管理者は、たとえば、[生産工順](routes-operations.md)、[関連工程](routes-operations.md#operation-relations)、[部品表](bill-of-material-bom.md)などのガイドを作成し、割り当てることができます。 作業者には、作業現場でそれぞれの工程経験に関連する手順が表示されます。

### <a name="service"></a>サービス

![サービス タスクのガイドの使用](media/instruction-guides-hero-service.png "サービス タスクのガイドの使用")

技術者には、現場でのガイド付き指示事項が提供されるため、追加の訪問をスケジュールする必要がありません。

サービス マネージャーは、たとえば品質評価のルーチンを説明する特定の[製品](../../commerce/product.md)にガイドを割り当てることができます。

### <a name="quality"></a>品質

![品質保証タスクでのガイドの使用](media/instruction-guides-hero-quality.png "品質保証タスクのガイドの使用")

従業員の知識を反復可能なツールに変えることにより、新しいプロセスをロールアウトし、一貫性を高めることができます。

品質保証マネージャーは、たとえば品質評価のルーチンを説明する[製品](../../commerce/product.md)にガイドを割り当てることができます。

### <a name="certifications"></a>証明書

![認定に関連したタスクのガイドを使用](media/instruction-guides-hero-certification.png "認定に関連したタスクのガイドの使用")

支援を必要とする人物をすばやく特定して、すべての従業員が高い基準を満たすようにします。

### <a name="safety"></a>安全

![作業安全手順のガイドの使用](media/instruction-guides-hero-safety.png "作業安全手順のガイドの使用")

物理環境で試みる前に、危険な手順を仮想的に実行する手順を説明します。 Mixed reality アプローチでは、作業者が危険な手順を仮想的に経験できます。

生産管理者は、[製品品目](../../commerce/product.md)、[工順](routes-operations.md)、および[工程](routes-operations.md#operation-relations)に手順を割り当てることにより、有害な材料取り扱いまたは繊細な処理手順に関する専用の手順を提供できます。

## <a name="get-started-with-instructions-and-guides"></a>手順とガイドの使用開始

生産プロセスで手順を有効にするために、Supply Chain Management には、Dynamics 365 Guides にすぐ使用できる統合機能が用意されています。 Guides のライセンスおよびインストールされたアプリケーション インスタンスは、生産資産と作業に Mixed Reality の手順を作成、管理、および割り当てるために必要です。

### <a name="prerequisites"></a>必要条件

この機能を使用するには、システムに次のものが含まれている必要があります。

- Dynamics 365 Supply Chain Management バージョン 10.0.15 以降
- Supply Chain Management アプリに対する[二重書き込み](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write)。
- [Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution)バージョン 400.0.1.48、またはそれ以降

### <a name="turn-on-the-feature"></a>機能をオンにする

この機能をシステムで使用できるようにするには、その構成キーを有効にする必要があります。 これを行う必要があるのは 1 回だけです。 これを行うには、管理者が次の操作を行う必要があります。

1. [メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、システムをメンテナンス モードにします。
1. **システム管理 \> 設定 \> ライセンス コンフィギュレーション** の順にクリックします。
1. **Mixed reality** セクションを展開し、**Mixed reality ガイド** チェック ボックスをオンにします。
1. **製品管理** セクションを展開し、**生産指示** チェック ボックスをオンにします。
1. [メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、メンテナンス モードをオフにします。
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>作業現場でのガイド表示方法の構成

作業現場でのガイドの表示方法を構成するには、**Mixed Reality \> Dynamics 365 Guides \> 構成ガイドの統合** へ移動します。

![製造用構成ガイドの統合](media/instruction-guides-configure-integration.png "製造用ガイド統合の構成")

次のフィールドを設定します。

- **Microsoft Dataverse URL** - Guides を作成する Microsoft Dataverse 環境の URL を指定します。 形式は "contoso.crm4.dynamics.com" で、URL の最初の部分は、通常、組織名に関連しています ("contoso" など)。2 番目の部分は環境のデータ領域 ("crm4" など) に固有で、最後の部分はドメイン ("dynamics.com" など) です。 適切な URL を見つけるには、[home.dynamics.com](https://home.dynamics.com/) 移動して Guides アプリを開くのも 1 つの方法です。 Guides を開くと、ブラウザーのアドレス バーに URL が表示されます (前の例に似ているベース URL のみをご利用ください)。 この値は、ガイドのアドレスを作成するために使用され、QR コードにエンコードされます。
- **QR コード サイズ** - レンダリングされた QR コードのサイズを設定します。 表示画面の大部分を占めるサイズを選択することをお勧めしますが、それ以上にはしないでください。 通常、*15* が適切な値です。
- **QR コード エラー訂正レベル** - QR コードの粒度を設定します。 粒度を高くすると、コードの信頼性を高めることができますが、**QR コードのサイズ** は選択した修正レベルに必要な詳細レベルをサポートするために、十分な大きさにする必要があります。

> [!TIP]
> - QR コードのサイズが大きすぎてディスプレイに表示できない場合は、表示に時間がかかります。表示に合わせて縮小する必要があります。 これらにはメリットがありません。
> - QR コードのサイズが小さすぎると、一部の環境で HoloLens がコードを適切に読み取る能力が低下する可能性があります。
> - HoloLens ユーザー向けに、QR コードを表示する各デバイスの設定をテストすることをお勧めします。 作業現場の環境で読みやすさを確保できる設定を選択します。  

## <a name="get-an-overview-of-all-guide-assignments"></a>すべてのガイド割り当ての概要を取得する

**すべてのガイド** ページを使用すると、組織で使用可能なすべてのガイドの一覧を表示したり、生産プロセスやリソースに対するすべての割り当てを表示したりできます。 これを開くには、**Mixed reality \> ガイド \> すべてのガイド** に移動します。 上部の一覧には使用可能なすべてのガイドが表示され、ここでフィールドを使用して一覧をフィルタリングできます。 下部の一覧には、すべてのガイドの割り当てが表示され、それらを管理するためのツールバーが表示されます。

![ガイドの管理](media/instruction-guides-allguides.png "ガイドの管理")

次のセクションでは、ガイドを割り当てることができるオブジェクトのタイプについて説明します。 各割り当てガイドには、それぞれの生産ジョブに自動的に関連付けられた手順が表示され、作業現場で使用できるようになります。

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>リソースへのガイドの関連付け

[リソース](operations-resources.md)にガイドを追加して、関連する生産ジョブのコンテキストでガイドを提供します。

### <a name="typical-scenario-using-resources"></a>リソースを使用する一般的なシナリオ

たとえば、マシンの一般的なセキュリティに関するガイドや、マシン タイプのリソースへの手順を処理するガイドを関連付けることができます。 その後、このガイドはマシンで実行されるすべてのジョブで使用できるようになります。

### <a name="add-a-guide-to-a-resource"></a>リソースへのガイドの追加

リソースへガイドを追加するには:

1. **生産管理 \> 設定 \> リソース \> リソース** の順に移動します。
1. 一覧ペインから、ガイドを割り当てるリソースを選択します。
1. **関連するガイド** のクイック タブを展開します。
1. **関連するガイド** ツールバーから **追加** を選択します。 新しい行がグリッドに追加されます。
1. 新しい行の場合は、**名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。 ガイドの数が多い場合は、一覧をフィルタリングして目的のガイドを見つけることができます。
    ![ガイドの管理](media/instruction-guides-allguides.png "ガイドの管理")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>リソース グループへのガイドの関連付け

リソース グループを使用してマシンのグループ、生産ライン、または作業セルを管理する場合、[リソース グループ](tasks/define-discrete-manufacturing-resource-group.md)にガイドを追加できます。

### <a name="typical-scenarios-using-resource-groups"></a>リソース グループを使用する一般的なシナリオ

**例 1:** 同じモデルの複数のマシンに対してリソース グループを定義している場合。 マシン モデルに関連する取扱説明ガイドを関連するすべてのリソースに割り当てる代わりに、そのマシン モデルを反映するリソース グループにガイドを割り当てることができます。

**例 2:** 異なるマシンを含む作業セルにリソース グループを定義している場合、作業セルを管理するための一般的な手順を提供するガイドがあります。 このガイドは、この作業セルのすべての生産活動に適用されます。

### <a name="add-a-guide-to-a-resource-group"></a>リソース グループへのガイドの追加

リソース グループへガイドを追加するには:

1. **生産管理 \> 設定 \> リソース \> リソース グループ** の順に移動します。
1. 一覧ペインから、ガイドを割り当てるリソース グループを選択します。
1. **関連するガイド** のクイック タブを展開します。
1. **関連するガイド** ツールバーから **追加** を選択します。 新しい行がグリッドに追加されます。
1. 新しい行の場合は、**名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。 ガイドの数が多い場合は、一覧をフィルタリングして目的のガイドを見つけることができます。
    ![リソース グループへのガイドの追加](media/instruction-guides-resourcegroup.png "リソース グループへガイドを追加する")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>リリース済製品へのガイドの関連付け

[リリース済製品](../pim/tasks/create-released-product-single-company.md)にはガイドを追加できます。

### <a name="typical-scenario-using-released-products"></a>リリース済製品を使用する一般的なシナリオ

製品レベルのガイドでは、特定のリリース済製品または品目の運用または処理に関する手順が作業現場の作業者に提供されます。

### <a name="add-a-guide-to-a-released-product"></a>リリース済製品へのガイドの追加

リリース済製品へガイドを追加するには:

1. **生産情報管理 \> 製品 \> リリース済製品** の順に移動します。
1. ガイドを割り当てる製品を開きます。
1. アクション ウィンドウで、**エンジニア** タブを開き、**表示** グループから、**関連するガイド** を選択します。
1. 選択したプロダクトの **関連ガイド** ページが開きます。
1. アクション ウィンドウで **追加** を選択して、新しい行をグリッドに追加します。 
1. 新しい行の場合は、**名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。
    ![リリース済製品へガイドを追加する](media/instruction-guides-ReleasedProduct-AddGuides.png "リリース済製品へガイドを追加する")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>フォーミュラへのガイドの関連付け

[フォーミュラ](bill-of-material-bom.md#formulas-co-products-and-by-products)にはガイドを追加できます。

### <a name="typical-scenario-using-formulas"></a>フォーミュラを使用する一般的なシナリオ
  
フォーミュラ レベル ガイドは、フォーミュラまたはレシピのコンテキストでのガイド付き処理手順が作業現場の作業者に用意されています。 また、フォーミュラのバージョンにガイドを割り当てることもできます。

> [!NOTE]
> 生産プロセスに関連するガイダンスは、工順、工順バージョン、または工順工程関連に対するフォーミュラに基づいて割り当てることができます。  

> 現在、個々のフォーミュラ行にガイドを関連付けることはできません。

### <a name="add-a-guide-to-a-formula"></a>フォーミュラへのガイドの追加

フォーミュラへガイドを追加するには:

1. **生産情報管理 \> 部品表およびフォーミュラ \> フォーミュラ** の順に移動します。
1. ガイドを割り当てるフォーミュラを開きます。
1. 上部クイックタブの上にある **ヘッダー** タブを開きます。
1. **関連するガイド** のクイック タブを展開します。
1. **関連するガイド** ツールバーから **追加** を選択します。 新しい行がグリッドに追加されます。
1. 新しい行の場合は、**名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。
    ![フォーミュラへガイドを追加する](media/instruction-guides-Formula.png "フォーミュラへガイドを追加する")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>フォーミュラ バージョンへのガイドの関連付け

[フォーミュラ バージョン](bill-of-material-bom.md#bom-and-formula-versions)にはガイドを追加できます。

### <a name="typical-scenario-using-formula-versions"></a>フォーミュラ バージョンを使用する一般的なシナリオ

フォーミュラの個々のバージョンに関連付けられたガイドは、そのバージョンのフォーミュラ レシピの生産についての手順を作業現場の作業者に提供します。

> [!TIP]
> 生産プロセスに関連するガイダンスは、工順、工順バージョン、または工順工程関連に対するこのフォーミュラ バージョンに基づいて割り当てることができます。  

> [!NOTE]
> 現在、個々のフォーミュラ行にガイドを関連付けることはできません。

### <a name="add-a-guide-to-a-formula-version"></a>フォーミュラ バージョンへのガイドの追加

フォーミュラ バージョンへガイドを追加するには:

1. **生産情報管理 \> 部品表およびフォーミュラ \> フォーミュラ** の順に移動します。
1. ガイドを割り当てるバージョンを含むフォーミュラを開きます。
1. 上部クイックタブの上にある **ヘッダー** タブを開きます。
1. **フォーミュラ バージョン** クイックタブで、ガイドを割り当てるバージョンを選択します。
1. **フォーミュラ バージョン** ツールバーで、**関連するガイド** を選択します。
    ![選択したフォーミュラ バージョンに関連付けられているガイドの表示](media/instruction-guides-FormulaVersion.png "選択したフォーミュラ バージョンに関連付けられているガイドの表示")
1. フォーミュラ バージョンの **関連ガイド** ページが開きます。
1. アクション ウィンドウで **追加** を選択して、新しい行をグリッドに追加します。 
1. 新しい行の場合は、**名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。
    ![フォーミュラ バージョンへガイドを追加する](media/instruction-guides-FormulaVersionAddGuide.png "フォーミュラ バージョンへガイドを追加する")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>部品表へのガイドの関連付け

すべての[部品表](bill-of-material-bom.md) (BOM) にガイドを追加できます。

### <a name="typical-scenario-using-bills-of-materials"></a>部品表を使用する一般的なシナリオ

BOM に関連付けられているガイドには、BOM から材料を準備および処理する方法を説明する手順が作業現場の作業者に用意されています。 また、BOM のバージョンにガイドを割り当てることもできます。

> [!NOTE]
> 現在、個々の BOM 行にガイドを関連付けることはできません。

### <a name="add-a-guide-to-a-bill-of-materials"></a>部品表へのガイドの追加

部品表へガイドを追加するには:

1. **生産情報管理 \> 部品表およびフォーミュラ \> 部品表** の順に移動します。
1. ガイドを割り当てる部品表を開きます。
1. 上部クイックタブの上にある **ヘッダー** タブを開きます。
1. **関連するガイド** のクイック タブを展開します。
1. **関連するガイド** ツールバーから **追加** を選択します。 新しい行がグリッドに追加されます。
1. 新しい行の場合は、**名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。
    ![BOM へガイドを追加する](media/instruction-guides-BOM.png "BOM へガイドを追加する")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>部品表バージョンへのガイドの関連付け

すべての[部品表バージョン](bill-of-material-bom.md#bom-and-formula-versions)にガイドを追加できます。

### <a name="typical-scenario-using-bill-of-materials-versions"></a>部品表バージョンを使用する一般的なシナリオ

個々の BOM バージョンに関連付けられたガイドでは、ジェネリック BOM またはその他のバージョンとは異なるバージョンの BOM の材料を準備および処理する方法を説明する手順が作業現場の作業者に用意されています。

> [!NOTE]
> 現在、個々の BOM 行にガイドを関連付けることはできません。

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>部品表バージョンへのガイドの追加

部品表バージョンへガイドを追加するには:

1. **生産情報管理 \> 部品表およびフォーミュラ \> 部品表** の順に移動します。
1. ガイドを割り当てるバージョンを含む BOM を開きます。
1. 上部クイックタブの上にある **ヘッダー** タブを開きます。
1. **BOM バージョン** クイックタブで、ガイドを割り当てるバージョンを選択します。
1. **BOM バージョン** ツールバーで、**関連するガイド** を選択します。
    ![選択した BOM バージョンに関連付けられているガイドの表示](media/instruction-guides-BOMVersion.png "選択した BOM バージョンに関連付けられているガイドの表示")
1. BOM バージョンの **関連ガイド** ページが開きます。
1. アクション ウィンドウで **追加** を選択して、新しい行をグリッドに追加します。
1. 新しい行の場合は、**名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。
    ![BOM バージョンへガイドを追加する](media/instruction-guides-BOMVersionAddGuide.png "BOM バージョンへガイドを追加する")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>工順へのガイドの関連付け

[工順](routes-operations.md)にはガイドを追加できます。

### <a name="typical-scenario-using-routes"></a>工順を使用する一般的なシナリオ

通常、工順は、BOM または BOM バージョンに基づいて、一連のリソースまたはリソース グループを使用して、特定のリリース製品をどのように生産するかを指定するために使用されます。

工順にガイドを割り当てることにより、それぞれの生産プロセスに関する手順を説明します。

### <a name="add-a-guide-to-a-route"></a>工順へのガイドの追加

工順へガイドを追加するには:

1. **生産管理 \> すべての工順** に移動します。
1. ガイドを割り当てる工順を開きます。
1. **関連するガイド** のクイック タブを展開します。
1. **関連するガイド** ツールバーから **追加** を選択します。 新しい行がグリッドに追加されます。
1. 新しい行の場合は、**名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。
    ![工順へガイドを追加する](media/instruction-guides-Route.png "工順へガイドを追加する")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>工順バージョンへのガイドの関連付け

[工順バージョン](routes-operations.md#route-versions)にはガイドを追加できます。

### <a name="typical-scenario-using-route-versions"></a>工順バージョンを使用する一般的なシナリオ

工順バージョンは、通常、既存の工順に基づいて生産プロセスのバリアントを指定するために使用されます。 各工順バージョンには、さまざまなガイドを割り当てることができます。

### <a name="add-a-guide-to-a-route-version"></a>工順バージョンへのガイドの追加

工順バージョンへガイドを追加するには:

1. **生産管理 \> すべての工順** に移動します。
1. ガイドを割り当てる工順を開きます。
1. **バージョン** クイック タブで、ガイドを割り当てるバージョンを選択します。
1. **バージョン** ツールバーで、**関連するガイド** を選択します。
    ![選択した工順バージョンに関連付けられているガイドの表示](media/instruction-guides-RouteVersion.png "選択した工順バージョンに関連付けられているガイドの表示")
1. BOM バージョンの **関連ガイド** ページが開きます。
1. アクション ウィンドウで **追加** を選択して、新しい行をグリッドに追加します。
1. 新しい行の場合は、**名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。
    ![工順バージョンへガイドを追加する](media/instruction-guides-RouteVersionAddGuide.png "工順バージョンへガイドを追加する")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>工順工程関連へのガイドの関連付け

[工順工程関連](routes-operations.md#operation-relations)にはガイドを追加できます。

### <a name="typical-scenario-using-route-operation-relations"></a>工順工程関連を使用する一般的なシナリオ

関連する工程は、製品プロセスや関連工程に対してガイダンスを追加するための最も具体的な方法です。 工順の各工程についてのガイダンスを指定したり、特定の品目や構成など工順に指定された関係コンテキストのタイプに対してさまざまなガイダンスを指定したりできます。 また、ガイダンスが適用される工程のステージ (設定、キュー、プロセス、配送など) を指定することもできます。

> [!NOTE]
> このようなガイドで、工順の複数の工程に関連するガイドを指定した場合、生成されたジョブの作業現場には、最も具体的な関係のあるガイドのみが表示されます。

### <a name="add-a-guide-to-a-route-operation-relation"></a>工順工程関連へのガイドの追加

工順工程関連へガイドを追加するには:

1. **生産管理 \> すべての工順** に移動します。
1. ガイドを割り当てる工順を開きます。
1. アクション ウィンドウで、**工順** タブを開き、**管理** グループから、**工順の詳細** を選択します。
1. 選択した工順の **工順の詳細** ページが開きます。
1. 上部グリッドで、ガイダンスを提供する工程を選択します。
1. 下部グリッドで、特定の関係 (汎用的な **すべて** の関係) を選択します。
    ![工程を選択してから、関係を選択](media/instruction-guides-RouteOperationRelation.png "工程を選択してから、関係を選択")
1. 下段の上にある **関連するガイド** タブを開きます。![関連するガイド タブ](media/instruction-guides-RouteOperationRelation-AddGuide.png "関連するガイド タブ")
1. 下部のグリッドの一番上にあるツールバーの **追加** を選択して、グリッドに新しい行を追加します。
1. 新しい行の場合は、**名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。 行の残りの部分で、選択したガイドを使用できるようにする各コンテキストのチェックボックスをオンにします。

> [!NOTE]
> 各工程のステージごとに 1 つ以上のガイドを追加できます。

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>作業現場の実行インターフェイスからのガイドの選択

作業者が作業現場の実行インターフェイスでジョブリストを開くと、Supply Chain Management によって表示されているジョブに関連するガイドが検出されます。 **ガイド** ボタンを使用して、関連するガイドを表示します。

![作業現場の実行インターフェイスでのガイド ボタン](media/instruction-guides-Shopfloor1.png "作業現場の実行インターフェイスでのガイド ボタン")

次に、HoloLens を装着し、QR コードを確認してそれぞれのガイドを有効化することによりガイドにアクセスします。

![QR コードで HoloLens を使用してガイドにアクセスする](media/instruction-guides-Shopfloor2.png "QR コードで HoloLens を使用してガイドにアクセスする")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>ガイドを選択するためのロジックを解決する

次の生産データにガイドを追加できます。

- [リソース](#resources)
- [リソース グループ](#resource-groups)
- [リリースされた製品](#released-products)
- [フォーミュラ](#formulas)
- [フォーミュラ バージョン](#formula-versions)
- [部品表 (BOM)](#bom)
- [BOM バージョン](#bom-versions)
- [工順](#routes)
- [工順バージョン](#route-versions)
- [工順工程関連](#route-operation-relations)

Supply Chain Management では、生産フロアのジョブを生成すると、それらのソースから関連するガイドが収集されます。 次の重要なルールに注意してください。

- BOM バージョンまたはフォーミュラ バージョンを工順または製造オーダーに関連付けた場合、そのバージョンに関連付けられているすべてのガイドと、そのバージョンの親 BOM またはフォーミュラに関連付けられているガイドもジョブに表示されます。
- 工順 バージョンを製造オーダーに関連付けた場合、そのバージョンに関連付けられているすべてのガイドと、そのバージョンの親工順に関連付けられているガイドもジョブに表示されます。
- *すべて* の関係を含む工順工程関係を定義し、それらの関係にガイドを割り当てると、ジョブには最も具体的な関係のあるガイドのみが表示されます。  

![関連するガイドを解決する図](media/instruction-guides-Resolve.png "関連するガイドを解決する図")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]